Beaver's third party GEGL Gimp Plugins for Gimp
=========
Welcome, I make third party GEGL filter plugins for Gimp by chaining GEGL nodes inside c file templates. This allows Gimp to have access to all sorts of cool text styling effects. It will turn your boring bland text into fancy text easy. Please view each filters individual Git page for more info on what each Gimp plugin can do. You have the option to download twenty something of my best filters in one place on the front page, but it may be better if you download each filter manually from my Github release sections as the list can get crowded and you may not need all my filters. I have over 70 filters in total. Please remember, unless you use Gimp 2.99.16 or up, all my filters are located in **the GEGL Operation section** for Gimp 2.10. On 2.99.16+ they are there but also exist in Filters>Text Styling and various other places like Filters>Render>Fun and more. Please note, my text styling filters are meant to be applied on text layers or raster copies of text layers and they are NOT capable of real time updates on text layers. However in the future this may be possible. In general most of my text styling plugins REQUIRE using white text and selecting "**layer to image size**" on a text layer before applying. It is even smart to make a back up layer of original text.

![image preview](text.png  )


![image preview](styles.png  )

![image](https://github.com/LinuxBeaver/LinuxBeaver/assets/78667207/2fe6a8ed-e903-432d-ac7c-872200b3eeb8)

All plugins have source code and compile instructions on their Github page and Github page release section and can be compiled with Ninja and Meson but Windows, Linux and Chromebook users can use preconfigured binaries. Mac users have to compile no matter what as I can't support Mac. If you look at the source code of my GEGL plugins you will also find GEGL syntax listed before the code begins. If you put this GEGL syntax inside Gimp's "GEGL Graph" filter you can test a plugin of mine in a static position without installing. The syntax provided in the source code roughly recreates the plugin. It is true transparency, every aspect of what I do is open source so others can learn and create GEGL plugins themselves if they want.

## Windows
.dll file filter binaries go in `C:\Users\USERNAME\AppData\Local\gegl-0.4\plug-ins` or perhaps `C:\Users\AppData\Local\gegl-0.4\plug-ins` then restart Gimp and open "GEGL Operation".
You may need to create the folder 'plug-ins` if it does not exist. 
There is a very low chance Windows users will need to reinstall Gimp for plugins to work. This low chance is probably caused by having a old version of Gimp or GEGL as a dependency. (before 2019)


#### download for Windows here
[Top twenty something GEGL Plugins for Windows](https://github.com/LinuxBeaver/LinuxBeaver/releases/download/Gimp_GEGL_Plugins_download_page/windows_top_gimp_gegl_plugins.zip) 

If you choose to not use binaries this is how you compile my plugins on Windows. When compiling run the `build_linux.sh ` files with MySys2.

http://gimpchat.com/viewtopic.php?f=8&t=20038&hilit=windows+compile#p275148
)
  
## Linux 
.so file filter binaries go in `/home/(USERNAME)/.local/share/gegl-0.4/plug-ins` then restart Gimp and open GEGL Operation. 
#### download for Linux here
[Top twenty something GEGL Plugins for Linux and Source Code](https://github.com/LinuxBeaver/LinuxBeaver/releases/download/Gimp_GEGL_Plugins_download_page/linux_top_gimp_gegl_plugins.zip) 

 The only packages needed to compile on Linux are `ninja`, `meson` and `gegl`. On most distros you should be able to press the build_linux.sh and go.

Includes Linux binaries and Source Code 

## FLATPAK Linux (INCLUDES CHROMEBOOK GIMP AS FLATPAK) 
  so. file filter binaries go in `/home/(USERNAME)/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins` then restart Gimp and open GEGL Operation. 
  
  ## SNAP Linux (NUMBER 393 VARIES)
  .so file filter binaries go `/home/USERNAME/snap/gimp/393/.local/share/gegl-0.4/plug-ins` NOTE - the number 393 may vary so read http://gimpchat.com/viewtopic.php?f=9&t=20336 
  for finding the right directory. Simply go back to `/home/USERNAME/snap/gimp/` and look for the correct number directory.  Once restart Gimp and open GEGL Operation.
  
## Mac OS (untested and no binaries) IF I GET HELP I MIGHT BE ABLE TO SUPPORT MAC.

.dylib file filter binaries go in `/Library/Application Support/gegl/0.4/plug-ins/`
or perhaps `/home/(USERNAME)/.local/share/gegl-0.4/plug-ins`

You may need to create `plug-ins` folder if it doesn't exist.

--Instructions to compile on Mac due to lack of binaries  --

https://brew.sh/

http://gimpchat.com/viewtopic.php?f=8&t=20357

Install Homebrew with `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
then

https://formulae.brew.sh/formula/meson#default
`brew install meson`

https://formulae.brew.sh/formula/ninja#default
`brew install ninja`

https://formulae.brew.sh/formula/gegl#default
 `brew install gegl`
  
  Then Compile every C file as you would on Linux using Meson and Ninja. Perhaps even my build.sh script will work.
Then right-click on each individual .dylib file and then select open (in the finder), and it asks if you really want to open it. After that restart Gimp
go to GEGL Operation. The plugin('s) *should work.  Each .dylib file needs to be manually approved. So running this in a folder to do exactly the same thing 
may be a good idea. `cd ~/Library/Application Support/gegl/0.4/plug-ins/ # assuming it was installed here
sudo xattr -rd com.apple.quarantine *`
  
  ## The five most recommended filters are in this particular order 
  
### 1. GEGL Effects (The layer effects counter part)
**Stable**
https://github.com/LinuxBeaver/GEGL-Effects---Layer-Effects-in-Gimp-using-GEGL/ 

or test its experimental update....
https://github.com/LinuxBeaver/GEGL-Effects---Layer-Effects-in-Gimp-using-GEGL/tree/GEGL-Effects-Continual-Experimental-update
  ![image preview](effects4.png )  
  
  This filter also ships with GEGL Inner Glow and GEGL Bevel and Glass on Text which are useful operations on their own.
  
## 2. Custom Bevel
A dedicated bevel designer plugin that goes far beyond what my basic gegl:bevel can do.
BECAUSE OF YOUR CARE AND SUPPORT A SPECIAL BRANCH OF CUSTOM BEVEL IS NOW ACCEPTED IN GIMP 3 AND IS CALLED CHAMFER.

https://github.com/LinuxBeaver/GEGL-Custom-Bevel
  ![image preview](framed_GEGL3.png )
 

  
## 3. SSG
A improved version of Gimp's Drop Shadow filter but it starts as a outline and knocks out the original image unless set to normal blend mode. Then it will behave like a normal outline and shadow. It even has an image file overlay mode. 
 What makes it better then dropshadow is that it applies the effect on its own layer. 
https://github.com/LinuxBeaver/GEGL-SSG-Stroke-Shadow-Glow-/
![image](https://github.com/LinuxBeaver/LinuxBeaver/assets/78667207/498d25f9-7702-40d6-beeb-540833b3ee12)

## 4. Extrusion 2  
   Just like the long shadow filter but it uses pixel data
https://github.com/LinuxBeaver/GEGL-Extrusion-2----Fork-of-GEGL-Long-Shadow

   
![image preview](extrusion2.png  )

  
## 5. Glossy Balloon
  A glossy bevelish effect that looks like glossy paste.
https://github.com/LinuxBeaver/GEGL-glossy-balloon-text-styling
  ![image preview]( yellow_ballon.jpg )

  



## Avoid SubFolders and non binary content in GEGL Plugins directory
Some people are having issues with my GEGL/Gimp plugins because they are making sub folders for each GEGL plugin of mine. All GEGL plugins should be in the same folder with no subfolders or any other file type. Folder should only contain binaries (.dll or .so) for your OS. Subfolders of binaries can lead to scenarios where users have two copies of a dependency and GEGL defaults to using an older version thus breaking plugins that need a newer dependency. Other file types could lead to Gimp not starting up.

  
## BTW, CHECK OUT THIS TEXT STYLE COLLECTION PLUGIN 
This is a filter I made that has dozens of unique fancy text style presets, but they all have very little editability. Meaning you can't do much with their sliders but they are off the charts amazing such as things like "cake text".
This filter ships with MANY other plugins of mine, so expect a surprise of bonuses. If you already have those plugins overwrite all of them with the latest version

https://github.com/LinuxBeaver/Gimp-Text-Style-Collection-Plugin

![image](https://github.com/LinuxBeaver/LinuxBeaver/assets/78667207/d9ea38e4-7c73-4a88-b2f1-66e05fd8f6b5)





## Lastly, (common complaint), If GEGL Effects breaks after downloading a new plugin of mine that is because the new plugin has a more recent dependency GEGL Effects needed, this can easily be fixed  by updating to the latest version of GEGL Effects.
  
  Enjoy!

