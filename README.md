# HDR-TE

To use this mod, here are the key steps and a few tips on customizing it with the additional files provided in the hdrTE_images folder.
The hdr-te folder goes into the [root:\ultimate\mods] folder of your SD card with the rest of the base hdr folders.

Additionally, delete the following files from the hdr mod folders to prevent conflicts:

[mods\hdr\ui\param\database]
- ui_stage_db.prcxml

[mods\hdr-stages\ui\layout\menu\stage_select\stage_select]*
- layout.arc

[mods\hdr-stages\ui\layout\patch\stage_select2\stage_select2]*
- layout.arc

[mods\hdr-stages\ui\replace\stage\stage_1]**
- stage_1_battlefield.bntx
- stage_1_end.bntx
- stage_1_ff_midgar.btnx
- stage_1_mario_paper.bntx
- stage_1_poke_stadium2.bntx
- stage_1_streetpass.bntx
- stage_1_zelda_gerudo.bntx

*You can safely delete the [hdr-stages\ui\layout] folder as it only contains those 2 seperated layout.arc files

**THESE FILES CHANGE DEPENDING ON YOUR RULESET
If you modify the ui_stage_db.prcxml the stages that show up on the SSS will of course change as well.

## Changing the number of stages displayed on the SSS

Starting from v1.3 another optional folder (stage_num options) is available that'll make adjusting the number of icons displayed on the stage select screen a bit easier.  You will need a program capable of opening
the layout.arc files, I recommend Switch-Toolbox: https://github.com/KillzXGaming/Switch-Toolbox

The layout.arc files can be found in [hdr-te\ui\layout\...]. For ease of changing between rulesets later on, I recommend copying this whole folder and adding it to the [stage_num options\xx stage] you plan on using.
For the sake of this guide we'll be using the 11 Stage folder.

Using Switch-Toolbox, open each layout.arc file and navigate to and expand the blyt folder. Locate the stage_select2.bflyt file, right click on it and select "Replace Raw Data".  It should open to the most recent
directory the toolbox was in, and if you are editing the copied over files you should already be somewhere within [stage_num options\11 stage\layout\...]. Move back to [stage_num options\11 stage] and open the 
stage_select2.bflyt. Congrats, your SSS has been modified, but make sure to save or else you'll have to do this all over again (if you try to close the program before saving it'll warn you).

You'll need to add the modified [stage_num options\11 stage\layout] folder to your SD Card. If you already have hdr-te placed on your SD Card: 

**!--MAKE SURE YOU DELETE THE LAYOUT FOLDER ON THE SD CARD FIRST WITHIN THE HDR-TE FOLDER. DO NOT COPY PASTE OVER IT--!**

Pro tip for working with SD Cards, they love to corrupt when making changes to files on them. Especially with copy/paste for files that are already on it. To safely proceed, just open up to the [mods\hdr-te\ui]
folder on your SD Card and delete the layout folder within it before pasting your newly modified layout folder. Again, I can't say this enough, do not copy paste without deleting that folder first. Your SD Card
probably has valuable save data/games on it, you don't want it corrupting.

If you don't have hdr-te already on your card, you can simply paste the modified layout folder into the [hdr-te\ui] folder, confirming the action to replace the conflicting files, and then add the hdr-te pack to
your SD Cards mods folder. It's a safe practice to delete the folder first though and not paste over it, you could forget which directory you're in and accidentally do this to your SD Card.  Better not to risk it.

This is actually way easier to do than it reads, I promise you. Enjoy your TE build with something other than a 10 stage ruleset if that's what your event is looking for.


========================================================

For customizing your stagelists, I've included a modified Stage Icons (Stage_1).psd from JoBen's vanilla TE mod with a large amount of new HQ icons for the modified HDR stages.
Not every stage is included, but you should be able to find most stages one would look for in a competitive enviroment. Provided I could work with the in game camera.

Additionally, I've included a com_mode_bg00_melee_06^s.psd. This texture is what's used in the background of the SSS in the layout.arc files, specifically p99_melee_com_btn0_00.bflyt within them.
If you ever want or need to adjust the version text I've provided it's very simple, although you will need the Lemon Milk font. You could also just change the background to whatevery you want.

Modifying the above files will also necessitate the use of Switch-Toolbox.  You can find the link above in the directions for changing the number of legal stages displayed on the SSS.

A major thanks to JoBen for creating the original vanilla TE mod which I referenced to figure out how and create this mod. And to all of the stage modders who created the stages which I
made HQ Stage Icons for.

**!--A WARNING TO ALL WHO USE RANDOM STAGES--!**

HDR has a bug that removes the first stage on your SSS from the random stage selectcion when creating rules. This unfortunately makes Wario Ware in the provided for build impossible to turn
off when creating new rulesets. You either have to boot to vanilla and turn it off there or be okay with it appearing on occasion. Old rulesets that had it turned on or off will continue to do so though.
So before installing it might also be a good time to turn WW off of whatever doubles rulesets you have. If you've modified your ui_stage_db.prcxml to have a different stage on "disp_order">0, that will
be the stage that is missing from the random stage select, please keep that in mind.
