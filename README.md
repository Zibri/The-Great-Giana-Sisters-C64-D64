# The-Great-Giana-Sisters-C64-D64
100% Crack of The Great Giana Sisters C64 D64. Protection removed. Scores reset. Only one byte changed :D

<img src="https://github.com/Zibri/The-Great-Giana-Sisters-C64-D64/blob/master/gianna1.png">
<img src="https://github.com/Zibri/The-Great-Giana-Sisters-C64-D64/blob/master/gianna2.png">

# Original file with modified High Scores
<a href="https://github.com/Zibri/The-Great-Giana-Sisters-C64-D64/raw/master/The%20Great%20Gianna%20Sisters.d64">Click here to download</a>

# Original file with the original default High Scores
<a href="https://github.com/Zibri/The-Great-Giana-Sisters-C64-D64/raw/master/The%20Great%20Gianna%20Sisters%20-%20Original%20Hiscores.d64">Click here to download</a>

<img src="https://github.com/Zibri/The-Great-Giana-Sisters-C64-D64/blob/master/gianna3.png">

# To rebuild the original protected disk (and obtain a clean master)

Copy this D64 on a floppy disk on drive #8
<a href="https://github.com/Zibri/The-Great-Giana-Sisters-C64-D64/raw/master/The%20Great%20Giana%20Sisters%20ORIGINAL.d64">Original protected D64</a>

Then RUN
<a href="https://github.com/Zibri/The-Great-Giana-Sisters-C64-D64/raw/master/WP.PRG">WP.PRG</a>

WP.PRG will write the protection track on track #36  
The protection consists of an empty track containing only a SYNC of a length between 110 and 113 bytes.  
Therefore the best length for maximum compatibility is 111 byte and a half.  

# Result

The result is a perfect master of The Great Giana Sisters.   
Mission accomplished.

<a href="https://github.com/Zibri/The-Great-Giana-Sisters-C64-D64/raw/master/TheGreatGianaSistersMaster.g64">TheGreatGianaSistersMaster.g64</a>

# Important note:  

This game will load only if only one drive is present on the IEC BUS.


# Addendum

The original disk of Giana Sisters can be copied with any quickcopy.
To remove the protection just run once this basic program:
```
10 open1,8,0,"1"                        
20 open15,8,15                          
30 print#15,"m-w"chr$(4)chr$(4)chr$(1)chr$(44)                                  
40 print#15,"m-w"chr$(1)chr$(0)chr$(1)chr$(144)                                 
50 close15:close1
```

Alternatively you can do:  
```
LOAD"2",8
POKE14776,35
RUN
```
Or you can save "2" after the POKE.  
This causes the loader to jump at $823 instead than $820.  
