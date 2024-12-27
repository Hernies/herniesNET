---
layout: post
date: 2024-12-17
tags:
  - "#obsidian"
  - "#nixos"
  - "#jekyll"
---
So, to build this website I used [samasaur's website](https://github.com/Samasaur1/samasaur1.github.io/tree/main) as a template (thank you so much!!). Let us go over the steps that led to this site existing.
#### Before we begin
I am a NixOS user, currently not a very experienced user (as of this post's redaction), but a user nonetheless. If you would like to replicate anything seen here this project has the following requirements:
- Nix :P

The project-specific requirements are already handled by the project, which is the magic of Nix (and NixOS).

---
## The project
### Nix develop
The site is firstly built locally using `nix develop` this is a tool offered by Nix, which makes it not exclusive of a nixos enviroment, but still requires the use of . To learn more about the .nix files built for this project, see [this post by samasaur](https://samasaur1.github.io/blog/building-my-site-with-nix)where he explains how he came to write them.

To use the build, simply clone and run on the root of the project the `nix develop` command. this will provide a console where you can run `jekyll serve` or any other command you deem necessary. Maybe something to debug your sass code (for example). 
### Theme
I quite hastily built the theme, reusing a color palette I designed myself. 
![[output (1).png]]
I also have a code theme, based on [this file](https://github.com/Samasaur1/samasaur1.github.io/blob/09e557fabd412607c7da8e5919b5015e12f3a1c6/assets/css/github.css#L4). I'm no designer but the aim is a solarized palette that is easy on the eyes; without it being the usual dark theme which anyone can make. 
### Github Actions
Github actions only required some work because I am using a custom domain. 
Just configure four A records to point to Github Actions servers, and a CNAME that points to your `[username].github.io`  


### Obsidian streamlining
To streamline the process and to encourage myself to write posts, I installed the plugins:
- Git
- Periodic Notes

Clone the project inside obsidian, build a template for the Daily Notes from the periodic notes plugin. Each Periodic note option can be then used to template the markdown for each type of post. Posts should hold a date in their title before the title itself. So it basically is a lazy man's automation. 

I will do some updates about this system in some time, probably february next year. 
