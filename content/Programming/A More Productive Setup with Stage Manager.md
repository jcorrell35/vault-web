---
title: A More Productive Setup with Stage Manager
description: Using Better Touch Tool to increase productivity
date: 2025-02-25
draft: false
---
>[!NOTE]
> [[#Update (4-9-2025)]] is the most up-to-date version of how I solved my productivity issues with Mac OS. The other methods are also viable methods as well.
# Stage Manager
I often like to have two sets/groups of window screens. One for the development environment with my Notes/VS Code and one for the “end-user environment” with Chrome and Terminal for running Hugo’s local server and viewing my website.
I use stage manager for this and it works really well, however, there is no native way to switch between the stages using a keyboard shortcut. There is only a shortcut for enabling/disabling stage manager.
# Better Touch Tool
While I was looking for how to do this I found a stack overflow post that suggested the [Better Touch Tool](https://folivora.ai/). It has a 45-day trial to start and has a very fair price point of $24 for a lifetime license (much less than I thought it was going to be). The tool allows you to assign custom keyboard shortcuts to perform custom actions. I set my keyboard shortcut to be **Alt** + **Tab** and I set the action to move forward through Stage Manager. If you use more than two groups you might want to consider making a shortcut to move backwards through Stage Manager as well.

The tool has a lot more actions and other types of triggers besides just keyboard shortcuts but I have only used it for this one scenario so far. I will update this after my 45-day trial to discuss my experience with it and if it was worth the $24 price point for one trigger/action. If you are interested in what other capabilities Better Touch Tool has check out [their website](https://folivora.ai/). Also [here is a great reddit post that touches more on the value of Better Touch Tool](https://www.reddit.com/r/MacOS/comments/nke8g6/bettertouchtool_is_one_of_the_most_worthit/).
# Update (3-31-2025)
After almost 45-days, I decided against using this tool. Not because of the tool itself, the tool is fantastic and is very customizable. Stage Manager is just not it... After switching from using Hugo to develop my website to Obsidian and Quartz my workflow changed for developing this site and the stage manager seemed to become more of a nuisance than anything. Even during development with Hugo it would take up unnecessary space and didn't work well with the "window snapping" tool I use called [Rectangle](https://rectangleapp.com/). I suppose Rectangle's "window-snapping" could of been the problem and something like [Magnet](https://apps.apple.com/us/app/magnet/id441258766?mt=12) could work better but I did not do any tests on that. That said, Better Touch Tool has nothing to do with Stage Manager and if I had other use cases for it I would of purchased the lifetime license for only $24.
# Update (4-9-2025)
There is one issue with using **Command** + **Tab** on Mac OS and that is hidden/minimized windows do not appear when selecting the application's icon. This can be very frustrating so finally after all these years of using Mac I decided to look up a solution. I ran across this [StackExchange post](https://apple.stackexchange.com/questions/112350/cmdtab-does-not-work-on-hidden-or-minimized-windows) explaining my exact issue. 

The solution is not very intuitive as you have to do the following (as explained in the post):
- press ⌘ Cmd + ⇥ Tab to show your running apps. Keep holding ⌘ Cmd.
- press ⇥ Tab until you've selected the app
- press the ⌥ Option, and let go of the ⌘ Cmd.  
    ( You must release ⌘ Cmd **after pressing** ⌥ Option ! )
    ( You must release ⌘ Cmd **before release** ⌥ Option ! )

Instead of doing this every time I found an application that actually uses the key combination **Alt** + **Tab** and when you select the window it pop ups just as it does on Windows. The application is called [AltTab](https://alt-tab-macos.netlify.app/) and at the time of writing this you can install it very easily with the brew package manager:
```
brew install --cask alt-tab
```
After installing you just have to run the program, give the programs some permissions in your Mac's settings, and you're ready to start switching windows just as you would on Windows.