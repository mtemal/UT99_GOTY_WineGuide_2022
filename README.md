# UT99_GOTY_WineGuide_2022
How to install Unreal Tournament GOTY using Wine


Download UT99 and Patch 469b:

Download UT99 from Archive.org:
https://ia902800.us.archive.org/15/items/UnrealTournamentGOTYUSA/Unreal%20Tournament%20%28USA%29%20%28Disc%201%29%20%28Game%20of%20the%20Year%20Edition%29%20%28Rerelease%29.zip

Download UT 469b Patch
https://github.com/OldUnreal/UnrealTournamentPatches/releases

Install wine, winetricks, and iat:

sudo apt install wine32
sudo apt install winetricks
winetricks orm=backbuffer glsl=disable sudo apt install iat

Use iat to turn the .bin to a .iso:

cd Downloads/

extract the .zip file so that the .bin and .cue files are present in the Downloads/ folder.

iat 'Unreal Tournament (USA) (Disc 1) (Game of the Year Edition) (Rerelease).bin' > UT.iso

Mount and Install UT99 and Patch 469b:

sudo mount -o loop UT.iso /mnt
cd /mnt
wine Setup.exe
cd ~
cd Downloads/
wine OldUnreal-UTPatch469b-Windows.exe
