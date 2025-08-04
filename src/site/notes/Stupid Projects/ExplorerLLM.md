---
{"dg-publish":true,"permalink":"/stupid-projects/explorer-llm/"}
---


## What?

I need to host my own LLMs.
I've been complaining about closed systems having too much information on and off me. and have been talking big about how universities and teaching institutions need to take things in their own hands; so I'm starting to put my money where my mouth is.

There are 2 main use cases I currently have in mind:
- Personal
- Educational

Especially educationally, it would be important to have student queries and histories + some analytics. Would be cool to build the base year by year, so course LLMs get better and better. Could implement RLFH. It's also important to have control over what the model is and what it knows etc. This will surely involve fine-tuning models.

Could also lead to agent architecture explorations...

## How?

- Ollama + OpenWebUI
- Web server first, local later (if I come by any money)?
- bought `explorerllm.com` until 01/08/2027

## Instructions and Finetuning

### Personal
Could be useful to create multiple customized models for personal use. *In any case*, its not financially sustainable to host my own models online or locally, so I will come back to this later...

### Educational
Instruction texts and finetuning/knowledge base materials would change course by course. 
Would be nice to prepare some finetuning routines and RAG or other knowledge management systems.
*In any case* cannot be deployed before actually starting a course (and paying for it through the money earned), but I can experiment with cheaper routines every once in a while
## Setup Demo

**Local WSL, tiny model for demo**

Install docker

```bash
# Update system
sudo apt update && sudo apt upgrade -y

# Install Docker
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker $USER

# Install Docker Compose
sudo apt install docker-compose -y

# Logout and back in for Docker permissions to take effect
```

Create deployment directory and docker compose

```bash
# Create project directory
mkdir ollama-chat && cd ollama-chat

# Create docker-compose.yml
cat > docker-compose.yml << 'EOF'
version: '3.8'

services:
  ollama:
    image: ollama/ollama:latest
    container_name: ollama
    ports:
      - "11434:11434"
    volumes:
      - ollama_data:/root/.ollama
    restart: unless-stopped
    # Uncomment if you have GPU
    # deploy:
    #   resources:
    #     reservations:
    #       devices:
    #         - driver: nvidia
    #           count: 1
    #           capabilities: [gpu]

  ollama-webui:
    image: ghcr.io/open-webui/open-webui:main
    container_name: ollama-webui
    ports:
      - "3000:8080"
    environment:
      - OLLAMA_BASE_URL=http://ollama:11434
      - WEBUI_SECRET_KEY=your-secret-key-change-this
    volumes:
      - ollama_webui_data:/app/backend/data
    depends_on:
      - ollama
    restart: unless-stopped

volumes:
  ollama_data:
  ollama_webui_data:
EOF
```

Start things up

```bash
# Start services
docker-compose up -d

# Check if running
docker-compose ps

# View logs if needed
docker-compose logs -f ollama-webui
```

Download models

```bash
# Download base model
docker exec ollama ollama pull qwen3:0.6b 

# Check available models
docker exec ollama ollama list
```

Login and begin

```bash
# Open in browser
http://localhost:3000
```

Shutdown

```bash
# Safe daily shutdown:
docker-compose stop

# Restart next day:
docker-compose start
```

Volumes are at 

```bash
/var/lib/docker/volumes/ollama-chat_ollama_data/
/var/lib/docker/volumes/ollama-chat_ollama_webui_data/

docker volume ls
docker volume inspect ollama-chat_ollama_data
```

Save

```bash
# Backup volumes:

# WebUI (users, history, etc)
docker run -v ollama-chat_ollama_webui_data:/data -v $(pwd)/backups:/backup ubuntu tar czf /backup/webui-data.tar.gz /data
# Models
docker run -v ollama-chat_ollama_data:/data -v $(pwd):/backup ubuntu tar czf /backup/models.tar.gz /data

# Check the backup was created
ls -lh backups/

# Manually remove the temporary container later
#docker ps -a  # Find the container ID
#docker rm <container-id>

```

Send

```bash
scp webui-data.tar.gz user@new-server-ip:/home/user/ 
scp ollama-models.tar.gz user@new-server-ip:/home/user/ 
scp docker-compose.yml user@new-server-ip:/home/user/
```

[[WebUIOllamaMigrationScript\|Here]] is a complete migration script. Use like:
```bash
chmod +x migrate-ollama.sh
./migrate-ollama.sh old-server-ip new-server-ip
```