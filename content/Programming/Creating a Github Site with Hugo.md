---
description: (OLD) A little guide/story of how I made this site
date: 2025-02-24
title: Creating a Github Site with Hugo
draft: false
---
> *This page is sort of outdated, it was the original way I was developing and deploying the website. It was originally called "This Website" and I was discussing how I built this website. I now use Obsidian to publish this site: [[Using Obsidian, Quartz, and Github Pages to Setup a Simple Static Website]].* Here is the [link](https://jcorrell35.github.io/life-repository) to my old website if you are curious.

This website is built with [Hugo](https://gohugo.io), using the [Terminal](https://github.com/panr/hugo-theme-terminal/) theme.

Hugo takes [Markdown](https://www.markdownguide.org/) files and turns them into static web pages. It was written in Go and it’s a great way to develop a great personal website that has simple navigation, tagging features, and easy to use themes.

For my site I went with the Terminal theme. I also decided to use the yaml format for the syntax files. For that, I renamed the default hugo.toml file to hugo.yaml and [changed the syntax to the yaml format](https://he3.app/en/blogs/yaml-to-toml-a-comprehensive-guide-for-developers/).

#### Usual setup for a project looks something like this:
----------
```shell=
hugo new site quickstart && cd quickstart
git init
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
echo "theme = 'ananke'" >> hugo.yaml
```


I ran into some issues using this method when it came to deploying the site to GitHub. Therefore I decided to go with a different method for implementing the theme. Which was copying the files from the theme folder into the base directory:  
![Files](images/filesystem.png)  
> [!warning] 
> This method does work, however if you want to change the theme at some point it becomes more difficult than just changing it in the hugo.yaml file.

The next step was to implement a simple menu system for the website's navigation:  
```yaml=
menu:
  main:
    - name: Home
      url: "/"
      weight: 1
    - name: Traveling
      url: "/traveling/"
      weight: 2
    - name: Music
      url: "/music/"
      weight: 3
    - name: Cooking
      url: "/cooking/"
      weight: 4
    - name: Programming
      url: "/programming/"
      weight: 5
    - name: Outdoors
      url: "/outdoors/"
      weight: 6
    - name: Places
      url: "/places/"
      weight: 7
```  

I applied the following code to the hugo.yaml file to center the page on the screen:  
```yaml=
centerTheme = "true"
```

The last thing I added was a taxonomy called places to be able to organize my posts by location/state. This is also done inside the hugo.yaml file:
```yaml=
taxonomies:
	category: categories
	place: places
	tag: tags
```
  
Finally, to run the website locally on your machine you can run the following code:  
```shell=
hugo server --buildDrafts
```

> [!note]
> I used the option --buildDrafts to build all blog posts no matter what the status of the draft property is in the file.*

Also, you can set the draft property to true so your post isn't live until you change the value. 
```yaml=
draft: true
```

