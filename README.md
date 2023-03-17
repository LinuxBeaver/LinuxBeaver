Beaver's third party GEGL Plugins for Gimp
=========
Welcome, I make third party GEGL filter plugins for Gimp by chaining GEGL nodes inside c file templates. This allows Gimp to have access to all sorts of cool text styling effects. It will turn your boring bland text into fancy text easy. Please view each filters individual Git page for more info on what each filter can do.


![image preview](text.png  )

## Windows
.dll file Filter binaries go in `C:\Users<YOUR NAME>\AppData\Local\gegl-0.4\plug-ins` then restart Gimp and open GEGL Operations.
https://cdn.discordapp.com/attachments/402851569692966914/1083815754383769711/GEGL_Binaries_For_Windows.zip
  
## Linux 
.so file Filter binaries go in `/home/(USERNAME)/.local/share/gegl-0.4/plug-ins` then restart Gimp and open GEGL Operations. 

[Linux Plugins and Source Code](https://cdn.discordapp.com/attachments/402851569692966914/1083815754752864366/GEGL_Linux_plugins.zip)


Includes Linux binaries, Windows Binaries and Source Code 

## FLATPAK Linux
  Filter binaries goes in `/home/(USERNAME)/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins` then restart Gimp and open GEGL Operations. 
  
  
  ## The five most recommended filters are in this particular order 
    This is incase you prefer downloading filters manually instead of grabbing all of them as binaries. 
  
  
### 1. GEGL Effects (The layer effects counter part)
https://github.com/LinuxBeaver/GEGL-Effects---Layer-Effects-in-Gimp-using-GEGL/
  ![image preview](effects4.png )  
  
  This filter also ships with GEGL Inner Glow and GEGL Bevel which are useful operations on their own.
  
## 2. Custom Bevel
https://github.com/LinuxBeaver/GEGL-Custom-Bevel
  ![image preview](framed_GEGL3.png )
 
 This is a dedicated Bevel filter for Gimp that goes far beyond what my basic gegl:bevel can do.
  
## 3. SSG
https://github.com/LinuxBeaver/GEGL-SSG-Stroke-Shadow-Glow-/

A imrpoved version of Gimp's Drop Shadow filter but it starts as a outline and knocks out the original image unless set to normal blend mode. It even has an image file overlay mode. It will be far more useful in Gimp 3.2
  
  
## 4. Extrusion 2 
https://github.com/LinuxBeaver/GEGL-Extrusion-2----Fork-of-GEGL-Long-Shadow
 
   Just like the long shadow filter but it uses pixel data

  
## 5. Glossy Balloon
https://github.com/LinuxBeaver/GEGL-glossy-balloon-text-styling
  ![image preview]( yellow_ballon.jpg )
  
  
  A glossy bevelish effect that looks like glossy paste.
  

  
  Enjoy!
  

