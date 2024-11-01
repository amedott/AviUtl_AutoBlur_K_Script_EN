# AviUtl_AutoBlur_K_Script

A script to automatically do direction, radial and rotation blur.

~~[Download](https://github.com/korarei/AviUtl_AutoBlur_K_Script/releases)~~
Download it from the [script] folder yourself.


## Starting

Download

- T_RotateBlur (Tim)

    ~~[Download](https://tim3.web.fc2.com/sidx.htm)~~ Probably included in your Extra Pack AviUtl install or something.

- RotBlur_M (Mr-Ojii氏)

    [Download](https://github.com/Mr-Ojii/AviUtl-RotBlur_M-Script/releases) 
    Open a notepad program, edit `RotBlur_M.lua`, save.  
        - Line 25, replace `obj.effect("領域拡張", "上", addY, "下", addY, "右", addX, "左", addX)` with `obj.effect("Region expansion", "Top", addY, "Bottom", addY, "Left", addX, "Right", addX)`  

Script itself should auto-detect `T_RotateBlur.dll` and `RotBlur_M.lua` if you have it in the same folder. If not, use "Mod Path".

- Same directory as exedit.auf  
- In `script` folder 
- Same folder as `AutoBlur_K.anm`

## Trackbars
- sAngle (Shutter Angle)

    Length of blur.

- sPhase (Shutter Phase)

    Position of blur.

## Other
1. Display Original

    Displays object un-blurred.

2. Consider Script

    Consider scripted changes.

3. Types of Blur

    - Dir Blur : Direction blur
    - Rad Blur : Radial blur
    - Rot Blur : Rotational blur
4. Relative Path

    Specifies path for the roational blur. Detects if it's ini the same place as AutoBlur_K.

5. Mod Path

    Specifies a specific path for rotational blur.

    e.g.
   
    - ..\\T_RotBlur\\?.dll
   
      Means that this is in the folder above AutoBlur_K.
   
    - ..\\rotblur_m\\?.lua
   
      Means that this is in the folder above AutoBlur_K.

7. Param

    Parameters

    1 Module type
   
      Specifies module. 1 for T_RotateBlur and 2 for RotBlur_M.

    - If you're using T_RotateBlur

        2 Angle resolution down.
      
        3 High-precision display.
      
        4 High-precision output.

    - If RotBlur_M

        2 quality
      
        3 reload

9. Keep Size

    Specifies whether to fix the size.

10. Amount

    Adjust the amount of blurring.

11. v0

    Specifies initial speed. If set well, blur is applied at frame 0.

    1. Enable/disable auto-calculation
       
        true to turn on、false to turn off.
        
        Can be used even if Consider Script is checked off.

        The acceleration is calculated based on the data from frames 0, 1, and 2, from which the displacement between frame -1 and frame 0 is calculated.
    
    2. Initial velocity in x direction [px/s]
    3. Initial velocity in y direction [px/s]
    4.　Initial velocity in zoom direction [%/s] (In the z direction, s1 = s0 * 1024 / (1024 + z), which is the change in apparent size using perspective.)
    5. Initial velocity in rz direction [deg/s]

## LICENSE
LICENSEファイルに記載
-- COPYRIGHT GOES TO korarei, I ONLY TRANSLATED THIS FOR MY OWN USE. -ame。
  - コードの整理

- **v1.0.0**
  - release
