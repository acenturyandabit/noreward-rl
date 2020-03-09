# My personal journey through curiosity-driven RL, over 42 minutes.

# Please see the original repository. Most of this is NOT MY WORK. I'm just making it run.

0. Watched this video: https://youtu.be/J3FHOyhUn3A

1. Tried installing with the commands provided in the paper. Replaced libav-tools with ffmpeg.

2. followed rest of the commands, up to and including `python curiosity/src/go-vncdriver/build.py`

3. Eeek scary red errors. Tried to resolve by running `sudo apt-get install -y python-numpy cmake zlib1g-dev libjpeg-dev libboost-all-dev gcc libsdl2-dev wget unzip`. Had those already.

4. Tried running `python curiosity/src/go-vncdriver/build.py` again.

5. seemed to work (no output or anything)

6. Downloaded models
`bash models/download_models.sh`

7. followed instructions in doomfiles/readme.md

8. stuff failed (cp couldnt find directory)

9. investigated. turns out installing doom-py failed. Tried `pip install doom-py`

10. same error message as in 3. Went searching on the internet. Found this page:

https://github.com/mwydmuch/ViZDoom/blob/master/doc/Building.md#-linux

and ran this: 

```
sudo apt-get install build-essential zlib1g-dev libsdl2-dev libjpeg-dev \
nasm tar libbz2-dev libgtk2.0-dev cmake git libfluidsynth-dev libgme-dev \
libopenal-dev timidity libwildmidi-dev unzip
```
11. Tried `pip install doom-py` again. still failure.

12. it seemed like python was erroring rather than c; so ran `pip3 install doom-py`  instead of pip install.

13. my bad, they were c warnings. I found 'could not find boost' in error messages so am installing boost.

14. apt says i already have boost. Tried following remaining steps in building.md above.

15. tried getting julia from apt, didn't work. Went here instead:

https://askubuntu.com/questions/842042/problems-installing-julia-language

16. that didn't work (`julia` at terminal didnt work) so I used `sudo snap install julia --classic` instead.

17. julia apparently doesn't like my platform. I think this rabbit hole has gone too deep. RIP.

I will inspect the source code later.
