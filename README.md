# Partial string modification tool of global-metadata.dat In **ENGLISH**
## For Android games exported from the backend of the Unity-il2cpp script, the strings appearing in the code will be compiled into the assets\bin\Data\Managed\Metadata\global-metadata.dat file. As a part of the localization work, a simple tool is used Modify the string in it.

 * ## Reference
 * ## il2cppdumper

### The understanding of the content of this file is learned from the source code of this tool. The tool itself is used to export class definitions from the compiled libil2cpp.so file and global-metadata.dat file. The export format includes IDA available Rename scripts, DLLs available in UABE and AssetStudio, etc., is a very useful tool.
Modify content
In global-metadata.dat, the way to save the strings in the code is that there is a list in the header to put the offset, length and other information of each string, and then there is an area in the data area to directly put all the strings compactly String, there is a list of heads, so there is no need to end with.
Because the number of strings is unchanged before and after the modification, the modification to the list is directly overwritten on the original area. The length of the data area may change. If the length of the data area is less than or equal to the original length after modification, it will be overwritten and written directly. If it is too long, it will be written to the end of the file.

## THIS ONLY OPEN "global-metadata.dat files!"

