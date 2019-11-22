# Radiologik Log Assembler
 This is a piece of Applescript I built which took a selection from the Music App and inserted it around my imaging in Radiologik



# Code overview:
It takes the selection, parses the locations of the individual items into a list that AppleScript can understand, and stores that as pathList

It then asks the user for the "Show Prefix" to find all the imaging. I have hard-coded in my folder locations, but the basic file structure is in my Documents folder there's a folder called 'Radio' and under that is all my Beds, Markers & Hooks plus all the individual imaging for each show I work.

From that input it figures out where each of the files are and stores each of them in lists.

Now it's time for the fun bit, actually putting all those into Radiologik.

The basic gist is it has counters for each of the things it needs to put in (TOHs, sweeps, songs, beds) and works it way through each of the lists until it reaches the end, when it loops back. The repeat loop is broken when all of the songs in the initial selection are inserted.

If you want to read the full code without downloading it, check out log-builder.txt which is exactly what the .scpt file is but in text. GitHub doesn't like AppleScript (It's almost as if it's a stupid language that I learnt before I realised this could be done in .js)