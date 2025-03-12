---
title: Using Obsidian, Quartz, and Github Pages to Setup a Simple Static Website
description: A little guide/story of how I made this site
date: 2025-02-28
draft: false
---
> This is the current way I am building this site. If you are interested in a different method, this was the old way that I built this site: [[Creating a Github Site with Hugo]]

Here is a [great resource for setting up a website with Obsidian](https://notes.nicolevanderhoeven.com/How+to+publish+Obsidian+notes+with+Quartz+on+GitHub+Pages). for setting up a website with Obsidian. Quartz is a static-site generator that turns markdown files (Obsidian notes) and turns them into a static website. I deployed the site using Github Pages.

I had one issue with the guide as for some reason my changes were not publishing.

After running this command to publish my changes:

```shell=
npx quartz sync
```

I also had to add the following two lines afterwards: 

```shell=
git push -u origin main
git push -u origin v4
```

For some reason when i would run `npx quartz sync` nothing would happen to my website. After 2 hours of trying to figure it out I just had to run the two git push commands afterwards for it to finally work... I might have to look at some of the code that sync runs to see if it runs those two commands correctly.

> [!note]
> To run the server locally just run `npx quartz build --serve`.
### Current Setup
- Obsidian with Obsidian Sync
- Quartz for static-site generation.
- Set excluded folders in Obsidian Sync for images, asnode_modules, and quartz to save space in the Remote Vault (Obsidian Sync only allows up to 1 GB). I do this so that I can change the content of my website from my phone. I am not able to add pictures permanently but I can add pictures temporarily on my phone and transfer them into the unsynced images folder afterwards.
- Push to the web with Github and Github Pages.
- .gitignore any private notes that I have.


