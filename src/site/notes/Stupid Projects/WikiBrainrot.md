---
{"dg-publish":true,"permalink":"/stupid-projects/wiki-brainrot/"}
---


## What?
This little pipeline pulls a random Wikipedia article and creates a text to speech dictation of it using coqui-tts.
It then loads a long video, chops it to the length of the audio file, adds the text of the speech (at correct timestamps) to the video, and saves the corresponding video file.

TLDR: Free TikTok Brainrot Generator

|![Pasted image 20250722154817.png|150](/img/user/Pasted%20image%2020250722154817.png)|![Pasted image 20250722154911.png|150](/img/user/Pasted%20image%2020250722154911.png)|![Pasted image 20250722155031.png|150](/img/user/Pasted%20image%2020250722155031.png)

--- 
## ToDo

- [ ] Web-based GUI - maybe with streamlit?
- [x] Fix word highlight timestamps
- [ ] Different TTS models
- [ ] Multiple BG music options
- [ ] Multiple video options
- [ ] Parallel batch processing?
- [ ] AI bg video generation? (overkill imo)
- [ ] AI bg music generation? (overkill imo)
- [ ] Auto-upload draft to TikTok
- [ ] Auto-upload draft to other social media?
- [ ] Auto-publish?
- [ ] Auto collect money?
- [ ] Auto spend money on games and beer
- [ ] Auto write passive income pipeline because this one is spent on games and beer
---
## Dependencies
You will need:
- Windows Subsystem for Linux (WSL)
- A video file longer than your TTS generation (or several, will add options to choose (randomly or not))
- Crop the video for mobile aspect ratio:
```bash
ffmpeg -i /path/video.mp4 -vf "crop=in_h*9/16:in_h,scale=1080:1920" /path/video_cropped.mp4
```
- An ambient music file longer than your TTS generation (or several, will add options to choose (randomly or not))

---
## Setup
### Social Media Accounts
#### Branding - identity

**General idea:** 
- Brainrot content using Wikipedia articles
- Potential for theme days/weeks
- My Wikipedia journeys as brainrot videos
- Accompanied music?
- 


**Candidate names:**
- WikiBrainrot
- WikiTok
- WikiRot
- BrainrotWiki
- 

**Candidate slogans:** 
- The Free Brainrot
- 
#### Host E-Mail

**email:** `wikirotbrain@gmail.com`
**password:** `rotwithknowledge`
#### TikTok
**username:**
**password:**
#### Instagram
**username:**
**password:**
#### YT Shorts
**username:**
**password:**

### Content Planning

- The week of the firsts
- 
### Pipeline

- Step1: Open WSL
```bash
# Create folder for the project
mkdir WikiTTS
# Move to the directory
cd WikiTTS
```
- Step 2: Install dependencies
```bash
sudo apt update
sudo apt install -y python3 python3-pip ffmpeg espeak
sudo apt install imagemagick
```
- Sub-step: Edit the ImageMagick security policy file:
```bash 
sudo nano /etc/ImageMagick-6/policy.xml
```
change <policy domain="path" rights="none" pattern="@*"/> `none` to `read|write`
```xml
<policy domain="path" rights="none" pattern="@*"/>
<policy domain="coder" rights="none" pattern="PDF" />
```
- Step 3: Create virtual environment
```bash
python3 -m venv tts_env
source tts_env/bin/activate
```
- Step 4: Install packages
```bash
pip install numpy
pip install coqui-tts
pip install moviepy==1.0.3
pip install openai-whisper
pip install wikipedia
pip install wikipedia-api
```
---
## Usage
- Step 1: Open WSL from the terminal app
- Step 2: Move to the project path and activate the virtual environment
``` bash
# Move to the directory
cd WikiTTS
# activate environment
source tts_env/bin/activate
```
- Step 3: Make sure the python script is at this directory
- Step 4: Set the paths of your resources (video and bg music) in the python script
- Step 5: Run python script
```bash
# run python script
python3 wikitts.py
# latest version!!
python3 movietts_v2.py
```

## Wiki Journeys
### Bard of Avon
https://en.wikipedia.org/wiki/William_Shakespeare

https://en.wikipedia.org/wiki/Hamlet

https://en.wikipedia.org/wiki/Ninety-five_Theses

https://en.wikipedia.org/wiki/2_B_R_0_2_B

https://en.wikipedia.org/wiki/Kurt_Vonnegut

https://en.wikipedia.org/wiki/On_the_Bondage_of_the_Will

https://en.wikipedia.org/wiki/The_Sirens_of_Titan

https://en.wikipedia.org/wiki/Cybernetics:_Or_Control_and_Communication_in_the_Animal_and_the_Machine

https://en.wikipedia.org/wiki/Norbert_Wiener

### Awaiting Title...



Prince Hamlet of Denmark is the son of the recently deceased King Hamlet, and nephew of King Claudius, his father's brother and successor. Claudius hastily married King Hamlet's widow, Gertrude, Hamlet's mother, and took the throne for himself. Denmark has a long-standing feud with neighbouring Norway, in which King Hamlet slew King Fortinbras of Norway in a battle some years ago. Although Denmark defeated Norway and the Norwegian throne fell to King Fortinbras's infirm brother, Denmark fears that an invasion led by the dead Norwegian king's son, Prince Fortinbras, is imminent.
On a cold night on the ramparts of Elsinore, the Danish royal castle, the sentries Bernardo and Marcellus discuss a ghost resembling the late King Hamlet which they have recently seen, and bring Prince Hamlet's friend Horatio as a witness. After the ghost appears again, the three vow to tell Prince Hamlet what they have witnessed.
The court gathers the next day, and King Claudius and Queen Gertrude discuss affairs of state with their elderly adviser Polonius. Claudius grants permission for Polonius's son Laertes to return to school in France, and he sends envoys to inform the King of Norway about Fortinbras. Claudius also questions Hamlet regarding his continuing to grieve for his father, and forbids him to return to his university in Wittenberg. After the court exits, Hamlet despairs of his father's death and his mother's hasty remarriage. Learning of the ghost from Horatio, Hamlet resolves to see it himself.
As Polonius's son Laertes prepares to depart for France, Polonius offers him advice that culminates in the maxim "to thine own self be true."[6] Polonius's daughter, Ophelia, admits her interest in Hamlet, but Laertes warns her against seeking the prince's attention, and Polonius orders her to reject his advances. That night on the rampart, the ghost appears to Hamlet, tells the prince that he was murdered by Claudius (by pouring poison into his ear as he slept), and demands that Hamlet avenge the murder. Hamlet agrees, and the ghost vanishes. The prince confides to Horatio and the sentries that from now on he plans to "put an antic disposition on", or act as though he has gone mad. Hamlet forces them to swear to keep his plans for revenge secret; however, he remains uncertain of the ghost's reliability.
Ophelia rushes to her father, telling him that Hamlet arrived at her door the prior night half-undressed and behaving erratically. Polonius blames love for Hamlet's madness and resolves to inform Claudius and Gertrude. As he enters to do so, the king and queen are welcoming Rosencrantz and Guildenstern, two student acquaintances of Hamlet, to Elsinore. The royal couple has requested that the two students investigate the cause of Hamlet's mood and behaviour. Additional news requires that Polonius wait to be heard: messengers from Norway inform Claudius that the king of Norway has rebuked Prince Fortinbras for attempting to re-fight his father's battles. The forces that Fortinbras had conscripted to march against Denmark will instead be sent against Poland, though they will pass through Danish territory to get there.
Polonius tells Claudius and Gertrude his theory regarding Hamlet's behaviour, and then speaks to Hamlet in a hall of the castle to try to learn more. Hamlet feigns madness and subtly insults Polonius all the while. When Rosencrantz and Guildenstern arrive, Hamlet greets his "friends" warmly but quickly discerns that they are there to spy on him for Claudius. Hamlet admits that he is upset at his situation but refuses to give the true reason, instead remarking "What a piece of work is a man". Rosencrantz and Guildenstern tell Hamlet that they have brought along a troupe of actors that they met while travelling to Elsinore. Hamlet, after welcoming the actors and dismissing his friends-turned-spies, asks them to deliver a soliloquy about the death of King Priam, as witnessed by Queen Hecuba, at the climax of the Trojan War. Hamlet then asks the actors to stage The Murder of Gonzago, a play featuring a death in the style of his father's murder. Hamlet intends to study Claudius's reaction to the play, and thereby determine the truth of the ghost's story of Claudius's guilt.
Polonius forces Ophelia to return Hamlet's love letters to the prince while he and Claudius secretly watch in order to evaluate Hamlet's reaction. Hamlet is walking alone in the hall as the King and Polonius await Ophelia's entrance. Hamlet muses on thoughts of life versus death. When Ophelia enters and tries to return Hamlet's things, Hamlet accuses her of immodesty and cries "get thee to a nunnery", though it is unclear whether this, too, is a show of madness or genuine distress. His reaction convinces Claudius that Hamlet is not mad for love. Shortly thereafter, the court assembles to watch the play Hamlet has commissioned. After seeing the Player King murdered by his rival pouring poison in his ear, Claudius abruptly rises and runs from the room; for Hamlet, this is proof of his uncle's guilt.
Hamlet mistakenly stabs Polonius (Artist: Coke Smyth, 19th century).
Gertrude summons Hamlet to her chamber to demand an explanation. Meanwhile, Claudius talks to himself about the impossibility of repenting, since he still has possession of his ill-gotten goods: his brother's crown and wife. He sinks to his knees. Hamlet, on his way to visit his mother, sneaks up behind him but does not kill him, reasoning that killing Claudius while he is praying will send him straight to heaven while his father's ghost is stuck in purgatory. In the queen's bedchamber, Hamlet and Gertrude fight bitterly. Polonius, spying on the conversation from behind a tapestry, calls for help as Gertrude, believing Hamlet wants to kill her, calls out for help herself.
Hamlet, believing it is Claudius, stabs wildly, killing Polonius, but he pulls aside the curtain and sees his mistake. In a rage, Hamlet brutally insults his mother for her apparent ignorance of Claudius's villainy, but the ghost enters and reprimands Hamlet for his inaction and harsh words. Unable to see or hear the ghost herself, Gertrude takes Hamlet's conversation with it as further evidence of madness. After begging the queen to stop sleeping with Claudius, Hamlet leaves, dragging Polonius's corpse away.
Hamlet jokes with Claudius about where he has hidden Polonius's body, and the king, fearing for his life, sends Rosencrantz and Guildenstern to accompany Hamlet to England with a sealed letter to the English king requesting that Hamlet be executed immediately.
Unhinged by grief at Polonius's death, Ophelia wanders Elsinore. Laertes arrives back from France, enraged by his father's death and his sister's madness. Claudius convinces Laertes that Hamlet is solely responsible, but a letter soon arrives indicating that Hamlet has returned to Denmark, foiling Claudius's plan. Claudius switches tactics, proposing a fencing match between Laertes and Hamlet to settle their differences. Laertes will be given a poison-tipped foil, and, if that fails, Claudius will offer Hamlet poisoned wine as a congratulation. Gertrude interrupts to report that Ophelia has drowned, though it is unclear whether it was suicide or an accident caused by her madness.
Horatio has received a letter from Hamlet, explaining that the prince escaped by negotiating with pirates who attempted to attack his England-bound ship, and the friends reunite offstage. Two gravediggers discuss Ophelia's apparent suicide while digging her grave. Hamlet arrives with Horatio and banters with one of the gravediggers, who unearths the skull of a jester from Hamlet's childhood, Yorick. Hamlet picks up the skull, saying "Alas, poor Yorick" as he contemplates mortality. Ophelia's funeral procession approaches, led by Laertes. Hamlet and Horatio initially hide, but when Hamlet realizes that Ophelia is the one being buried, he reveals himself, proclaiming his love for her. Laertes and Hamlet fight by Ophelia's graveside, but the brawl is broken up.
Back at Elsinore, Hamlet explains to Horatio that he had discovered Claudius's letter among Rosencrantz and Guildenstern's belongings and replaced it with a forged copy indicating that his former friends should be killed instead. A foppish courtier, Osric, interrupts the conversation to deliver the fencing challenge to Hamlet from Laertes. Hamlet, despite Horatio's pleas, accepts it. Hamlet does well at first, leading the match by two hits to none, and Gertrude raises a toast to him using the poisoned glass of wine Claudius had set aside for Hamlet. Claudius tries to stop her but is too late: she drinks, and Laertes realizes the plot will be revealed. Laertes slashes Hamlet with his poisoned blade. In the ensuing scuffle, they switch weapons, and Hamlet wounds Laertes with his own poisoned sword. Gertrude collapses and, claiming she has been poisoned, dies. In his dying moments, Laertes reconciles with Hamlet and reveals Claudius's plan. Hamlet rushes at Claudius and kills him. As the poison takes effect, Hamlet, hearing that Fortinbras is marching through the area, names the Norwegian prince as his successor. Horatio, distraught at the thought of being the last survivor and living whilst Hamlet does not, says he will commit suicide by drinking the dregs of Gertrude's poisoned wine, but Hamlet begs him to live on and tell his story. Hamlet dies in Horatio's arms, proclaiming "the rest is silence". Fortinbras, who was ostensibly marching towards Poland with his army, arrives at the palace, along with an English ambassador bringing news of Rosencrantz and Guildenstern's deaths. Horatio promises to recount the full story of what happened, and Fortinbras, seeing the entire Danish royal family dead, takes the crown for himself and orders a military funeral to honour Hamlet.