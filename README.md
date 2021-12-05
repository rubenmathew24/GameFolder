# GameFolder
A way to make Folders for the GameHub 2 Rainmeter skin

This skin assumes you already have Rainmeter, GameHub 2 by not-Finch, its required plugins installed

Create A GameHub Folder Skin:
  - Simply duplicate the GameHub 2 skin directory in your Rainmeter folder or use the provided .rmskin file
  - Rename the copy to "GameHUB - Folder"
    - I'll refer to this as the folder directory

Steps to set up a Folder:

  - Go to /@Resources/User in the folder directory
  - Make a copy of list_Example.inc and rename it to list_\<FolderName\>.inc
  - Put at least one game in list_\<FolderName\>.inc (at least an icon)
    - This isn't neccessary but it lets you see visually if it worked when you are done
  - Make a copy of page_Example.inc and rename it to page_\<FolderName\>.inc
    - If you want a different layout than the one I chose, go to /@Resources/Include/Default and copy one of the presets
  - Open page_\<FolderName\>.inc in a text editor and rename both Lists (there should be two) to list_\<FolderName\>.inc
  
How to Link your folder to GameHub:

  - Launch GameHub 2
  - Create a "Game" to open the folder 
      - You can add the name, icon, and/or background but don't touch the directory yet
  - Right Click the "Game" and press "List file.inc"
  - Within this file, find the "Game" with the name you gave it
  - Set its directory to [!WriteKeyValue "Variables" filelayout page_\<FolderName\>.inc "\<Path to Rainmeter\>\Rainmeter\Skins\\GameHUB - Folder\@Resources\Settings.inc"][!ActivateConfig "GameHUB - Folder" "GameFolder.ini"]
    - Make sure to replace \<Path to Rainmeter\> with the actual path and \<FolderName\> with your actual folder name
    
All Done!
Now when you click on the "Game" it should close the current GameHub skin, and open a new one where you can add Games to your folder.
If you click the close button on the folder, it will bring you back to the original GameHub 2
