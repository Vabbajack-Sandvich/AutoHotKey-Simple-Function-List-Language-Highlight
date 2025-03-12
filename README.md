#Autohotkey Notepad++ custom language highlight and function list files


This highlights syntax and finds function and hotkey definitions, and lists them in Notepad++ the function list window. 

This is intended to be simple and non-exhaustive.

This uses this regex pattern to make the function list in Notepad++ find the 2 things below:

^[*\t*A-Z*a-z*\d*]*\({1}[\,*[*A-Z*a-z*\d*\s*]*]*\){1}\r\n\t*\{+|^[*\t\$\^\!\+*A-Z*a-z*\d]*\:\:\r\n\t*\{+



#A function definition:


blah(blah1, blah2, blah3)
{
	blahblah()
}



#A hot key definition:


$^+f::
{
	blah(1,2,3)
	return
}

Sorting by A-z# in the Notepad++ function list or not means you can see where the function or hotkey falls in the code or not.

Trying to see all the variations of the hotkeys won't work alphanumerically, and they will be scattered, but if you group them alphanumerically in the code and switch the function list to display as it finds stuff in the code, it makes it easy to see all the functions and hotkeys relative to each other.

#Windows Install For Notepad++

This is just both of the readme files for both the Custom Language Highlight Section and the Function List Section.


#Custom Language Highlight


Complete both sections, the overrideMap.xml and Language Highlight Sections

Both sections have to be completed for the language highlight and the function list to work.



#WINDOWS:


Copy and paste ahk.xml into this directory.

C:\Users\USERNAME\AppData\Roaming\Notepad++\userDefineLangs

Then restart Notepad++.

Open your .ahk file.

Select the ahk language from the bottom of the language menu.

Open the function list by going to view, then ticking the function list at the bottom of the view menu.

You might have to click on and off the ahk file, or click refresh on the functional, to see if everything worked properly.

But if it did work, you should see all your functions and all the hot keys with:: in the name.



#Function List and overrideMap.xml


<!--


========
Follow the directions for the custom language highlight and function list files.

Both sections have to be completed for the language highlight and the function list to work.
========


This goes at the end of the association section of the overrideMap.xml 

WINDOWS:

DIRECTORY:

C:\Users\USERNAME\AppData\Roaming\Notepad++\functionlist

FILENAME:

overrideMap.xml

Copy and paste the ahk-fl.xml file into the same functionlist directory.

Complete both sections, the overrideMap.xml and Language Highlight Sections

Then restart Notepad++

Open your .ahk file

Select the ahk language from the bottom of the language menu.

Open the function list by going to view, then ticking the function list at the bottom of the view menu.

You might have to click on and off the ahk file or refresh the function list to see if everything worked properly. But if it did work, you should see all your functions and all the hot keys with :: in the name.

-->

<association id= "ahk-fl.xml"	userDefinedLangName="ahk"/>


