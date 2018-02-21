---
layout: post
title:  "Bugfix Assignment"
date:   2018-02-21 00:00:02 -0500
categories: hfoss
---
I'm currently the designer for RITLUG's (RIT Linux User's Group) project [TigerOS](https://github.com/RITlug/TigerOS). The project is a Fedora remix aimed at making it easier for RIT students getting into Linux. I had already created the mascot, our tiger penguin, and wallpapers to go with it. After making some adjustments to the wallpapers, the team alerted me that because the font I used for the wallpapers is not default installed on most machines so trying to open the source file for the wallpaper without the font would cause horrible things to happen. Whoops. We decided to add that you needed to install the font to be able to work with the wallpapers to the design documentation. We were also missing documentation on how to export the new assets in the file structure so they would be included in the OS on install. So I added that [documentation to our wiki](https://github.com/RITlug/TigerOS/wiki/TigerOS-Design). The wiki is through GitHub's native wiki so there was no pull request but you can see [my edits in revisions](https://github.com/RITlug/TigerOS/wiki/TigerOS-Design/_history) and it was ultimately approved through [closing the associated issue](https://github.com/RITlug/TigerOS/issues/96). A lot of our discussions were through in person meetings but there were also some slack conversations reproduced below:

    Regina Locicero [3:08 PM]
    @ctmartin did you want me to change the font? that's the only thing we're iffy about, I'm pretty sure you guys said just to export it to .jpg and 1080p
    and it would be fine
    
    Christian Martin [3:08 PM]
    @gen1e the font is perfectly ok, the issues with it were to do with needing the font installed nativey in order to properly render
    
    Regina Locicero [3:09 PM]
    Then everything is resolved with that issue
    
    Tim Zabel [3:09 PM]
    @ctmartin In order to fully remove this issue, it seems we are using Roboto font. We should probably install Roboto font on the default install if it isn't already
    
    Christian Martin [3:10 PM]
    @Tjzabel21 Install not needed on TigerOS, we should just have a wiki page for the design and notate it in there
    
    Tim Zabel [3:11 PM]
    Sounds good. I'll reopen the issue, and add a note that we should have documentation that states we use the Roboto font.
    
    Christian Martin [3:11 PM]
    @Tjzabel21 make a new issue and tag it with docs
  
As for actually creating the documentation for the bugfix it wasn't too difficult. The hardest part was making the export documentation. Because of how Fedora works, we have to replace some of the assets used in the system with our own logo through putting them with specific names, in specific sizes, in a specific file structure. Going back through that structure and figuring out what would need to be replaced when the logo was updated was a bit of a pain but necessary. I feel better knowing that any potential designers know what they need to do when a design is approved and it's time to implement. 
