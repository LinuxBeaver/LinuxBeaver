
### Download code and binaries for all plugins on their latest versions here

https://github.com/LinuxBeaver/LinuxBeaver/releases/tag/Gimp_GEGL_Plugin_download_page

### NEWS 

**A recent crash** 
[Text Style Collection (Food Edition)](https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_Text_style_collection/releases/)  is crashing GIMP 3.0.6 - Update my plugins to solve it 

**GIMP 3.0.6 and 3.2 has slow boot times with GEGL plugins + Windows users need to compile**

**Regaring GIMP 3.2 - Windows binaries will not work on GIMP 3.2 requiring Windows users to recompile**

Linux works just fine though

On September 1st 2025 All my plugins updated so they no longer have crash warnings in GIMP 3.14 - GIMP's team also fixed the bug in 3.1.5 two days later - Read more here -> https://github.com/LinuxBeaver/LinuxBeaver/issues/16 Put simply, if you are using the latest versions of my plugins on GIMP 3.0.4 or 3.1.5 you will have no issue. But expect things to be slow on startup only in GIMP 3.0.6 no matter what. 

**Isolated download for AI plugins (April 2025 to present)**
The download page now contains a section with links to "vibe coded" GEGL plugins. They are seperate from my normal plugins because technically **I didn't make them** AI Grok did, and somewhat AI Deep Seek, These plugins use actual pixel math unlike my natural plugins that depend on chaining existing GEGL nodes. Most of them do pattern design and gradients. All non-destructive of course. They will always be a seperate download from my natural plugins due to AI controversy.

**GIMP 3 release and known appimage problem** 
GIMP 3 is released and it is highly recommended to use my plugins on 3 as opposed to GIMP 2.10. Though they will work on both. Make sure to try out native GIMP 3 filters (Styles, Bevel and Inner Glow) which are plugins of mine officially in GIMP 3. NOTE, my plugins currently don't work with the official GIMP 3 appimage but GIMPs team has acknowledged this and may fix it soon in a future release.

Beaver's third party GEGL GIMP Plugins 
=========
Welcome, I make third party GEGL filter plugins for GIMP by chaining GEGL nodes inside c file templates. This allows GIMP to have access to all sorts of cool text styling effects. It will turn your plain text into fancy graphical text styles. Please view each filters individual Git page for more info on what each GIMP plugin can do. You have the option to download fifty something of my best filters in one place on the front page, but it may be better if you download each filter manually from my Github release sections as the GEGL operation list can get crowded and you may not need all my filters.  I have over 120 filters in total. Please remember, unless you use GIMP 2.99.16 or up, all my filters are located in **the GEGL Operation section** for GIMP 2.10. On 2.99.16+ they are there but also exist in Filters>Text Styling and various other places like Filters>Render>Fun and more.

![image](https://github.com/user-attachments/assets/38946b16-7c7e-4ccb-9d1e-a9fc628400c7)

## In GIMP 2.10 
It is recommended to apply my filters on raster duplicates of text layers in GIMP 2.10. So you have to go through a manual step of making a text layer, rasterizing it then applying a filter.

## In GIMP 3
In GIMP 3 (what I use) just type text, press escape  and apply the filter (thats it! a lot less work) The reason we press escape key is so we can escape the text editing and access the search menu to search for a plugin of mine. Text layers in GIMP 3 are capable of real time updates due to NDE. 

Both GIMP 2.10 and GIMP 3 share a common theme where white text allows some plugins to recolor the text to anything

![image](https://github.com/LinuxBeaver/LinuxBeaver/assets/78667207/2fe6a8ed-e903-432d-ac7c-872200b3eeb8)

All plugins have source code and compile instructions on their Github page and Github page release section and can be compiled with Ninja and Meson but Windows, Linux and Chromebook users can use preconfigured binaries. Mac users have to compile no matter what as I don't know how to support Mac. If you look at the source code of my GEGL plugins you will also find GEGL syntax listed before the code begins. If you put this GEGL syntax inside GIMP's "GEGL Graph" filter you can test a plugin of mine in a static position without installing. The syntax provided in the source code roughly recreates the plugin. It is total transparency, every aspect of what I do is open source so others can learn and create GEGL plugins themselves if they want.

## Windows
.dll file filter binaries go in `C:\Users\USERNAME\AppData\Local\gegl-0.4\plug-ins` or perhaps `C:\Users\AppData\Local\gegl-0.4\plug-ins` then restart GIMP and open "GEGL Operation".
You may need to create the folder 'plug-ins` if it does not exist. 

There is a very low chance Windows users will need to reinstall GIMP for plugins to work. This low chance is probably caused by having a old version of GIMP or GEGL as a dependency. 

## Windows (portable apps)
Search for **gegl-0.4** make a plug-ins folder and put the binaries there or see if `drive:\GIMPPortable\App\gimp\lib\gegl-0.4\plug-ins` exist and put the binaries there.
 
#### download for Windows here
[Download all plugins for Windows](https://github.com/LinuxBeaver/LinuxBeaver/releases/download/Gimp_GEGL_Plugin_download_page/WindowsBinaries_all_plugins.zip) 

If compiling run the `build_plugin_windows.sh ` files with MySys2.

http://gimpchat.com/viewtopic.php?f=8&t=20038&hilit=windows+compile#p275148
)
  
## Linux 
.so file filter binaries go in `~/.local/share/gegl-0.4/plug-ins` then restart GIMP and open GEGL Operation. 
#### download for Linux here
[Download all plugins for Linux here](https://github.com/LinuxBeaver/LinuxBeaver/releases/download/Gimp_GEGL_Plugin_download_page/LinuxBinaries_all_plugins.zip) 

Includes Linux binaries and Source Code 

## FLATPAK Linux (INCLUDES CHROMEBOOK GIMP AS FLATPAK) 
  so. file filter binaries go in `~/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins` then restart Gimp and open GEGL Operation. 
  
  ## SNAP Linux (NUMBER 393 VARIES)
  .so file filter binaries go `~/snap/gimp/393/.local/share/gegl-0.4/plug-ins` NOTE - the number 393 may vary so read http://gimpchat.com/viewtopic.php?f=9&t=20336 
  for finding the right directory. Simply go back to `/home/USERNAME/snap/gimp/` and look for the correct number directory.  Once number is found restart GIMP and open GEGL Operation.

## Source Code only of all 120+ GEGL plugins

[https://github.com/LinuxBeaver/LinuxBeaver/releases/download/Gimp_GEGL_Plugin_download_page/source_code_of_all_GEGL_plugins.zip](https://github.com/LinuxBeaver/LinuxBeaver/releases/download/Gimp_GEGL_Plugin_download_page/source_code_of_all_GEGL_plugins.zip)

Source Code of all plugins contains a collection of over 120 GEGL/GIMP plugins 

##  How to compile an individual GEGL plugins

Running the script **build_plugin_linux.sh** will compile an invidiual plugin with all its dependency binaries if needed inside a folder named "LinuxBinaries" or "WindowsBinaries" depending on your OS.


##  How to compile all 120+ GEGL plugins
Running **build_everything_linux.sh / build_everything_windows** will compile everything in a folder named "LinuxBinaries" or "WindowsBinaries" depending on your OS.


## FAQ: I UPDATED YOUR PLUGINS AND MOST PLUGINS DON'T SHOW UP ANYMORE 
If you are using Ubuntu 20.04, 22.04, (Debian 10-12)  without Flatpak GIMP 2.10.36 and up you will **NOT** be able to use plugins of mine updated after March 11 2024.

### Why do these plugins not work anymore after updating?

In 2025-2026 GEGL deprecated all plugins of mine that use **gegl_node_connect_from** It requires a new **gegl_node_connect** that early GIMP can't read. This applies to the majority of my plugins. 
Below is a download for the original plugins before the break happened.

**Plugin and Code download for Debian 10,11,12, Ubuntu 20.04 and 22.04 is here, this branch does not ever update**

https://github.com/LinuxBeaver/LinuxBeaver/releases/download/Gimp_GEGL_Plugin_download_page/pre_446_plugins_code_and_top_binaries.zip

GEGL 0.446 can read both **gegl_node_connect_from** and **gegl_node_connect** plugins but earlier versions can only read **gegl_node_connect_from** Every official plugin of mine now uses **gegl_node_connect**

### Why do I have GIMP Fatal Error after updating your plugins?
This bug may happen on Windows  because you mixed new plugins compiled with GEGL 0.4.46+ with old ones compiled with GEGL 0.4.30-ish - Don't do that.


## Technical compile Guide for Linux 

**build_plugin_linux.sh** and **build_everything_linux.sh** is the easy way to compile everything but this is guide goes over all requirements

### 1. Downloading the Plugins

First, you need to download the GEGL plugins. The front page contains a link to download all of them. 

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

### 3. Compiling the Plugins 

- If you've downloaded the source code and wish to compile the plugins, follow these steps:
- Extract the Source Code: If the source code comes in a compressed file (like .zip or .tar.gz), extract it first.
- Navigate to the Source Directory: Use the terminal to navigate to the directory where you've extracted the source code.
- Run the Build Script: Execute the build_plugin_linux.sh script. This script should automate the compilation process. You can run it by typing:

```
./build_plugin_linux.sh

```
Ensure that this script is executable. If not, make it executable by running chmod +x build_plugin_linux.sh.

### 4. Installing the Compiled Plugins

- Locate the Compiled .so Files: After compilation, look for .so files in the build directory.
- Copy the .so Files to the GEGL Plugins Directory: Use the command:

```
Linux 
cp [source_path]/*.so /home/$(whoami)/.local/share/gegl-0.4/plug-ins/

Linux  (Flatpak)
cp [source_path]/*.so /home/$(whoami)/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins



```
Do NOT have multiple copies of the binaries or put binaries in separate folders

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
Then right-click on each individual .dylib file and then select open (in the finder), and it asks if you really want to open it. After that restart GIMP
go to GEGL Operation. The plugin('s) *should work.  Each .dylib file needs to be manually approved. So running this in a folder to do exactly the same thing 
may be a good idea. `cd ~/Library/Application Support/gegl/0.4/plug-ins/ # assuming it was installed here
sudo xattr -rd com.apple.quarantine *`
  
  ## Recommended plugins
  
### 1. GEGL Effects CE (The layer fx counter part)

This one filter can make 1000s of text styles.  This filter also ships with other plugins GEGL Inner Glow and GEGL Bevel and GEGL Glass on Text which are useful operations on their own in stand alone mode.

https://github.com/LinuxBeaver/GEGL-Effects---Layer-Effects-in-Gimp-using-GEGL/ 
![image](https://github.com/user-attachments/assets/02b50c3c-e481-4ca3-a8fe-abd511391ee3)

![image](https://github.com/user-attachments/assets/3fda13f4-87d2-435b-879a-c5d5c249ca5d)


## 2. The Bevels (Bump, Chamfer, Ring, Edge)

https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_custom_bevel/ (bump)

https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_Sharp_bevel/ (chamfer)

https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_Edge_Bevel/

https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_Ringed_Bevel/

![image](https://github.com/user-attachments/assets/6d154a06-1328-4b70-b1ce-a7ffd5172952)

 
## 3. Extrusion Long Shadow
https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_Extrusion_2

Just like the long shadow filter but it uses pixel data
   
![image preview](extrusion2.png  )


## 4. Outline Deluxe 

https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_Outline_Deluxe/

![image](https://github.com/user-attachments/assets/0dd6e7e1-b78d-4685-b5c8-79110accc837)

![image](https://github.com/user-attachments/assets/4e890791-6446-4ec1-bc95-9c88beba460f)

![image](https://github.com/user-attachments/assets/3561009d-2e73-4811-8f41-3bb282260c24)


## 5. Sparkle 

https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_sparkle/

Add a sparkle effect to images

![image](https://github.com/user-attachments/assets/4c2c8456-8f81-48c1-b419-d7e246d6564d)

## 6. The background design plugins

These plugins render background designs. Listed horizontally by three their names are  

https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_Oceans_Surface

https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_Marble

https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_starburst

https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_star_background

https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_starfield

https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_clouds

https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_Stripes

https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_Polygons

https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_rock_surface

![image](https://github.com/user-attachments/assets/827667d9-f62a-4ecb-b795-8a5327c1ea1e)

## 7. Shapes (GIMP 3 recommended for quality use)
https://github.com/LinuxBeaver/Vector_Layers_in_GIMP_via_vignette/
![image](https://github.com/user-attachments/assets/c7f42289-a2df-400f-b790-55ac208d5d81)
Draw circles, squares, ovals, recentangles and dividers amd control them with a non-destructive vignette filter. Make sure to uncheck the internal vignette checkbox on GIMP 3. On 2.10 keep internet vignette checked.

## Avoid SubFolders and non binary files in GEGL Plugins directory
Some people are having issues with my GEGL/GIMP plugins because they are making sub folders for each GEGL plugin of mine. All GEGL plugins should be in the same folder with no subfolders or any other file type. Folder should only contain binaries (.dll or .so) for your OS. Subfolders of binaries can lead to scenarios where users have two copies of a dependency and GEGL defaults to using an older version thus breaking plugins that need a newer dependency. Other file types could lead to GIMP not starting up.

![image](https://github.com/user-attachments/assets/3939ff98-f4f0-47fb-9163-63fd3eb8c581)


## Lastly, (possible complaint), If GEGL Effects breaks after downloading a new plugin of mine that is because the new plugin has a more recent dependency GEGL Effects needed, this can easily be fixed  by updating to the latest version of GEGL Effects. However, this complaint is mostly mute now and will only happen if you are using versions of GEGL Effects before 2024.
  
  Enjoy!

