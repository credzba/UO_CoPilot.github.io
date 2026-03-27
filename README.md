# UO_Copilot.github.io

This is a derivative of Razor (https://github.com/markdwags/Razor) and RazorEnhanced (https://github.com/RazorEnhanced/RazorEnhanced)

RazorEnhanced is an awesome project originally developed by  AlexDan. It was a really cool idea in that it used the old Razor code, but added the ironpython interfaces so that the scripting language became a true language instead of a scripting language coded by hand for UO. 

Currently uo_copilot is under development and is working, but not usable. 

The improvements I am making are things I couldn't do within the existing player base of RazorEnhanced.

1. It changes the json storage to better model the flow of UO. 

   Some of the frustrating things in RE were:

   Save passwords. They are stored in the profile, but the profile is not loaded until the character is logged in, long after the password was needed.  To get around this was some ugly code that used the last profile, hoping it was what was correct.  Without drastically changing the storage model I couldn't fix it correctly.

2. The UI is implemented using GTK 3.24 instead of windows forms. 

   Windows forms was discontinued on all .net after 4, current version is .net 10. 

   RazorEnhanced is stuck on a soon to be discontinued version of .net (true of Razor as well). The only hope to be able to move to future .net is to get to a UI that supports current .net implementations. I had many choices Gtk (3 or 4) , QT, Avalonia, some of Microsoft's later versions, but 1 requirement I need is a graphic UI tool because I am UI disabled. 

   After prototyping many of these tools, I settled on Gtk 4, about 20% into moving to it I found that Gtk 4 was incompatible with .net 4 .. I was so frustrated!  Windows Forms will ONLY do .net 4, Gtk 4 will NOT do .net 4. I walked away for months. 

   Finally, even though Gtk 3 is old, it is still supported, supports .net from 4 - 10 and has a UI builder named Glade. 

   So, here we are. 

   I want to especially mention my co-author on a lot of this code Anthropic's Claude ai. This would have taken 5 or 10 times as long without ai coding assistance. Some days I still hate ai, including Claude. One day I told him he was to stupid to work with, and deleted him from my system... but I forgave him, gave a 6 month later version another chance and it is much improved.  I still have to watch, and if he goes off on some tangent drag him back, but for most things he is great.  I assigned him a big refactor the other day and went on a walk with my wife. Came back, and all the code was done, and done well.  

   