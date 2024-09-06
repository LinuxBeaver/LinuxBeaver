# NEWS 

### March 11 2024 - my plugins require Gimp 2.10.34 and up and no longer clip in Gimp 2.99.19

### August 28th 2024 news (bunker repo may be deprecated)  

1. Gimp 3 plugins still have a special repo but it may not be needed anymore as the problem my plugins have in GIMP 3 also exist with native GIMP filters such as gegl:dropshadow. As of 8-28-2024 GIMP's team hay have officially solved the problem; http://gimpchat.com/viewtopic.php?f=7&t=20876&p=291276#p291276.  The GIMP 3 bunker repo will be removed in under two weeks if no more crashes are found.

2. No new features were added to my plugins, but it has never been easier to compile my GEGL plugins. One click now compiles all 80+ plugins of mine. The code base is now extremely well organized before it was a mess.

### Sept 3 2024 2.99.19 GEGL Effects has a rare crash
line 1567 of GEGL effects was fixed to only contain `"operation", "lb:bevel",` and not the additional `"th", 0.100,` Please update GEGL Effects continual to Sept 3 2024 version to solve the rare crash

## 
Beaver's third party GEGL Gimp Plugins for Gimp
=========
Welcome, I make third party GEGL filter plugins for Gimp by chaining GEGL nodes inside c file templates. This allows Gimp to have access to all sorts of cool text styling effects. It will turn your boring bland text into fancy text easy. Please view each filters individual Git page for more info on what each Gimp plugin can do. You have the option to download thirty something of my best filters in one place on the front page, but it may be better if you download each filter manually from my Github release sections as the list can get crowded and you may not need all my filters. 

I have over 80 filters in total. Please remember, unless you use Gimp 2.99.16 or up, all my filters are located in **the GEGL Operation section** for Gimp 2.10. On 2.99.16+ they are there but also exist in Filters>Text Styling and various other places like Filters>Render>Fun and more. Please note, my text styling filters are meant to be applied on text layers or raster copies of text layers in Gimp 2.10, but in 2.99.19+ they are capable of real time updates on text layers due to NDE.  In general most of my text styling plugins benefit from using white text and selecting "**layer to image size**" on a text layer before applying in Gimp 2.10, but on Gimp 2.99.19+ users can enjoy non-destructive editing. 

So once again if you are on Gimp 2.10 the workflow is make 1. white text,  2.layer to image size, 3. apply filter. Where as 2.99.19+ is far simpler. If you notice text clipping in Gimp 2.99.19 it is because you do not have the latest version of my plugins.

![image preview](text.png  )


![image preview](styles.png  )

![image](https://github.com/LinuxBeaver/LinuxBeaver/assets/78667207/2fe6a8ed-e903-432d-ac7c-872200b3eeb8)

All plugins have source code and compile instructions on their Github page and Github page release section and can be compiled with Ninja and Meson but Windows, Linux and Chromebook users can use preconfigured binaries. Mac users have to compile no matter what as I can't support Mac. If you look at the source code of my GEGL plugins you will also find GEGL syntax listed before the code begins. If you put this GEGL syntax inside Gimp's "GEGL Graph" filter you can test a plugin of mine in a static position without installing. The syntax provided in the source code roughly recreates the plugin. It is true transparency, every aspect of what I do is open source so others can learn and create GEGL plugins themselves if they want.

## Windows
.dll file filter binaries go in `C:\Users\USERNAME\AppData\Local\gegl-0.4\plug-ins` or perhaps `C:\Users\AppData\Local\gegl-0.4\plug-ins` then restart Gimp and open "GEGL Operation".
You may need to create the folder 'plug-ins` if it does not exist. 
There is a very low chance Windows users will need to reinstall Gimp for plugins to work. This low chance is probably caused by having a old version of Gimp or GEGL as a dependency. (before 2019)

## Windows (portable apps)
Search for **gegl-0.4** make a plug-ins folder and put the binaries there or see if `drive:\GIMPPortable\App\gimp\lib\gegl-0.4\plug-ins` exist and put the binaries there.
 
#### download for Windows here
[Top thirty something GEGL Plugins for Windows](https://github.com/LinuxBeaver/LinuxBeaver/releases/download/Gimp_GEGL_Plugins_download_page/windows_top_gimp_gegl_plugins.zip) 

If you choose to not use binaries this is how you compile my plugins on Windows. When compiling run the `build_linux.sh ` files with MySys2.

http://gimpchat.com/viewtopic.php?f=8&t=20038&hilit=windows+compile#p275148
)
  
## Linux 
.so file filter binaries go in `/home/(USERNAME)/.local/share/gegl-0.4/plug-ins` then restart Gimp and open GEGL Operation. 
#### download for Linux here
[Top thirty something GEGL Plugins for Linux and Source Code](https://github.com/LinuxBeaver/LinuxBeaver/releases/download/Gimp_GEGL_Plugins_download_page/linux_top_gimp_gegl_plugins.zip) 

 The only packages needed to compile on Linux are `ninja`, `meson` and `gegl`. On most distros you should be able to press the build_linux.sh and go.

Includes Linux binaries and Source Code 

## FLATPAK Linux (INCLUDES CHROMEBOOK GIMP AS FLATPAK) 
  so. file filter binaries go in `/home/(USERNAME)/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins` then restart Gimp and open GEGL Operation. 
  
  ## SNAP Linux (NUMBER 393 VARIES)
  .so file filter binaries go `/home/USERNAME/snap/gimp/393/.local/share/gegl-0.4/plug-ins` NOTE - the number 393 may vary so read http://gimpchat.com/viewtopic.php?f=9&t=20336 
  for finding the right directory. Simply go back to `/home/USERNAME/snap/gimp/` and look for the correct number directory.  Once restart Gimp and open GEGL Operation.

## Source Code only of all 80+ GEGL plugins

https://github.com/LinuxBeaver/LinuxBeaver/releases/download/Gimp_GEGL_Plugins_download_page/source_code_of_all_GEGL_plugins.zip

## FAQ: I UPDATED YOUR PLUGINS AND MOST PLUGINS DON'T SHOW UP ANYMORE 
If you are using Ubuntu 20.04, 22.04, (Debian 10-12)  without Flatpak Gimp 2.10.34 and up you will **NOT** be able to use plugins of mine updated after March 11 2024.

### Why do these plugins not work anymore after updating?

In 2025-2026 GEGL will break all plugins of mine that use **gegl_node_connect_from** It requires a new **gegl_node_connect** that early Gimp can't read. This applies to the majority of my plugins. 
Below is a download for the original plugins before the break happened.

**Plugin and Code download for Debian 10,11,12, Ubuntu 20.04 and 22.04 is here, this branch does not ever update**

https://github.com/LinuxBeaver/LinuxBeaver/releases/download/Gimp_GEGL_Plugins_download_page/pre_446_plugins_code_and_top_binaries.zip

GEGL 0.446 can read both **gegl_node_connect_from** and **gegl_node_connect** plugins but earlier versions can only read **gegl_node_connect_from** Every official plugin of mine now uses **gegl_node_connect**

### Why do I have Gimp Fatal Error after updating your plugins?
This bug may happen on Windows  because you mixed new plugins compiled with GEGL 0.4.46 with old ones compiled with GEGL 0.4.30 - Don't do that.


## Compile Guide for Linux 


### 1. Downloading the Plugins

First, you need to download the GEGL plugins. from the link "Top thirty something GEGL Plugins for Linux and Source Code" which contains over 30 plugins as binaries ready for use but all 70+ plugins as source code only.

### 2. Installing Required Packages
Before you can use or compile the plugins, you need to have certain packages installed on your Linux system:

- Ninja: A small build system with a focus on speed.
- Meson: An open-source build system meant to be both extremely fast and user-friendly.
- GEGL: The underlying graphics library used by GIMP.

These can typically be installed via your distribution's package manager. For example, on Ubuntu, you can open a terminal and run:

```
sudo apt-get update
sudo apt-get install ninja-build meson libgegl-dev
```

### 3. Compiling the Plugins (If Required)

- If you've downloaded the source code and wish to compile the plugins, follow these steps:
- Extract the Source Code: If the source code comes in a compressed file (like .zip or .tar.gz), extract it first.
- Navigate to the Source Directory: Use the terminal to navigate to the directory where you've extracted the source code.
- Run the Build Script: Execute the build_linux.sh script. This script should automate the compilation process. You can run it by typing:

```
./build_linux.sh

```
Ensure that this script is executable. If not, make it executable by running chmod +x build_linux.sh.

### 4. Installing the Compiled Plugins

- Locate the Compiled .so Files: After compilation, look for .so files in the build directory.
- Copy the .so Files to the GEGL Plugins Directory: Use the command:

```
Linux 
cp [source_path]/*.so /home/$(whoami)/.local/share/gegl-0.4/plug-ins/

Linux  (Flatpak)
cp [source_path]/*.so /home/$(whoami)/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins

Do NOT have multiple copies of the binaries or put binaries in separate folders.

```

### 5. Restart GIMP
After copying the files, restart GIMP. The new GEGL operations should now be available in GIMP.

If pre-compiled binaries (.so files) are provided, you can skip the compilation steps. Just copy these .so files directly to the /home/$(whoami)/.local/share/gegl-0.4/plug-ins/ directory and restart GIMP.


  
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
  
  ## The seven most recommended filters are in this particular order 
  
### 1. GEGL Effects (The layer effects counter part)
https://github.com/LinuxBeaver/GEGL-Effects---Layer-Effects-in-Gimp-using-GEGL/ 
  ![image preview](effects4.png )  
  
  This filter also ships with GEGL Inner Glow and GEGL Bevel and GEGL Glass on Text which are useful operations on their own; especailly bevel and inner glow which have many unique options.
  
## 2. Custom Bevel
https://github.com/LinuxBeaver/GEGL-Custom-Bevel
  ![image preview](framed_GEGL3.png )

  A classic bevel effect by combining gaussian blur and emboss
 
## 3. SSG
https://github.com/LinuxBeaver/GEGL-SSG-Stroke-Shadow-Glow-/
![image](https://github.com/LinuxBeaver/LinuxBeaver/assets/78667207/498d25f9-7702-40d6-beeb-540833b3ee12)
A improved version of Gimp's Drop Shadow filter but it starts as a outline and knocks out the original image unless set to normal blend mode. Then it will behave like a normal outline and shadow. It even has an image file overlay mode. 
 What makes it better then dropshadow is that it applies the effect on its own layer. 


## 4. Extrusion 2 
https://github.com/LinuxBeaver/GEGL-Extrusion-2----Fork-of-GEGL-Long-Shadow  
![image preview](extrusion2.png  )

   Just like the long shadow filter but it uses pixel data

## 5. Glossy Balloon
https://github.com/LinuxBeaver/GEGL-glossy-balloon-text-styling
  ![image preview]( yellow_ballon.jpg )
  
  A glossy bevelish effect that looks like inflated glossy paste.

## 6. Shapes (GIMP 2.99.19/3 recommended for quality use)
https://github.com/LinuxBeaver/Vector_Layers_in_GIMP_via_vignette/
![image](https://github.com/user-attachments/assets/c7f42289-a2df-400f-b790-55ac208d5d81)
Draw circles, squares, ovals, recentangles and dividers amd control them with a non-destructive vignette filter. Make sure to uncheck the internal vignette checkbox on GIMP 3. On 2.10 keep internet vignette checked.

## 7. Sharp Bevel
https://github.com/LinuxBeaver/GEGL_sharp_bevel_gimp_plugin/
![image](https://github.com/user-attachments/assets/ace23382-e28c-4edf-a35c-0839ba79f4e3)

Custom Bevel has a cousin called Sharp Bevel which is made using distance transform and emboss as opposed to gaussian/box blur then emboss. As stated earlier a simple version of this plugin is in GIMP 3 that combines both sharp bevel and custom bevel's functionality. This plugin is far more advance with more technical features then the one that is in GIMP 3.

## Avoid SubFolders and non binary content in GEGL Plugins directory
Some people are having issues with my GEGL/Gimp plugins because they are making sub folders for each GEGL plugin of mine. All GEGL plugins should be in the same folder with no subfolders or any other file type. Folder should only contain binaries (.dll or .so) for your OS. Subfolders of binaries can lead to scenarios where users have two copies of a dependency and GEGL defaults to using an older version thus breaking plugins that need a newer dependency. Other file types could lead to Gimp not starting up.







## Lastly, (common complaint), If GEGL Effects breaks after downloading a new plugin of mine that is because the new plugin has a more recent dependency GEGL Effects needed, this can easily be fixed  by updating to the latest version of GEGL Effects.
  
  Enjoy!

