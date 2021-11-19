---
locpath: C:\me\ACTIVE\bsPUB\github.com\realB12\monster-gen\07_EXP\8_TEC\THEMES\Delta\a\DeltaThemeExplore_a\README.md

previewWebRootPath: C:\me\ACTIVE\bsPUB\github.com\realB12\monster-gen\07_EXP\8_TEC\THEMES\Delta\a\DeltaThemeExplore_a\

author: rene.baron@baronsolutions.ch
created: 16.11.2021 13:12:02
version: draft v0.0.1
draft: true
private: false
disqid: DiscussID
tags: ["aktiv", "***", "bré"]
categories: ["Hugo", "Intern"]
---

# DeltaThemeExplore_a's README file
`rene.baron@govy.swiss | bré | Nov 16, 2021 | draft work in progress v0.0.1 | updated Nov 16, 2021`


---

<div style="background-color:#DFFF00; border-style:solid; border-color:#DFFF00; border-width:20px;">
<span style="font-weight:bold">Links</span>

* [HugoRelLinks.md](../../../../../../../../../../../REPO/work/TOOLS/H/HUGO/GUIDE/HugoRelLinks.md): Internal Research Paper about HUGO's Hyperlink Management


* [MarkDownMonster Docs on "Configuring Site Relative Base Paths"](https://markdownmonster.west-wind.com/docs/_5fz0ozkln.htm)

* [HTTP5: Lektion über die generelle Verwendung von Relativen Hyperlinks](https://wiki.selfhtml.org/wiki/HTML/Tutorials/Links/Referenzieren_in_HTML#Mit_protokoll-relativen_URIs_referenzieren)
</div>

---

* **Owner**: rene.baron@baronsolutions.ch :: **Start**: 2021-08-21 :: **Status**: ongoing

* **Credentials**: -> [_underscore file](../_DeltaThemeExplore.md) (outside this project)

 ![](xPIC/DeltaHomepage.png)

* [Official Documentation](documentation.html)


## Purpose and Goals to be achieved by this Theme Exploration project

Goal of this Exploration project is to **understand** 

a) how the Theme is **setup** in general in terms of templates, archetypes, etc.

b) its **components** like for instancen the Disqus component

c) how this theme **integrates wie existing content files** (can we put on top, or do we have to copy/past content into the themes folder)  

d) **hosting**: How to push this Example project on a Hosting Environment (Netlify, AWS)

e) Testint the Hyperlink issues for referencing *.md files   

Focus is on technology with a focus on architecture and ongoing operationabiltiy. 

### Out of Scope

## Issues
The following Issues have been found: 

## Hyperlink Issue

> The Power of the Internet is not its files, but how their contained information is (hyper)linked. 

### The Problem
Relative `[go to myfile](myfile.md)`-style hyperlinks, as we are using them in the MonsterGen editor, work fine in the MonterGen Preview as well as when being uploaded to GitHub and being clicked but normally fail for HUGO generated Websites, because the Hugo compiler does not resolve them by default, resp. does not convert the `*.md` filetype-extension into `*.html` to point to the tranformed HTML-page.  
  
However, this is a general issue that is not specific to this Delta Theme, but is neither solved by it. 

Neither can the problem be solved within the Monster-Editor because Hyperlinks in Markdown have to be defined like this to keep navigation in the Monster-Preview an on GitHub working. 

### Solution
As descibed by the general [Research Document about Hugo Hyperlinks]() I will have to test so called **Hugo Link-RenderHooks** where we can manually program the way that hyperlinks in *.md files are translated under special conditions such as the Hyperlink being in a file, a header, footer, navigation elements or the href property of a picture. 

## Testcases
Sobald ein Hugo Projekt lokal läuft, mit einem GitHub-Repo synchronisiert und über Netlify- und AWS-Hosting funktioniert und in Forestry editiert werden kann sollen Test für alle [Navigationsarten](#navigationsarten) und alle möglichen Beriebsvarianten durchgeführt werden. 
Bei den Beriebsvariante unterschieden wir 
a) die Navigation auf der Basis der [nativen `*.md`-Dateien](#1-markdown-navigation) und 
b) die Navigation in den [HUGO generierten `*.html`-Dateien](#2-html-navigation)

### Test Data

Have added cross-referencing Hyperlinks between  [content/english/blog/post-1.md](content/english/blog/post-1.md) and [content/english/blog/post-2.md](content/english/blog/post-2.md)
as follows

1. [post-2.md](post-2.md)
2. [../post-2.md](../blog/post-2.md)
3. [../../../README.md](../../../README.md)



### 1. Markdown Navigation
Hier geht es darum, dass mit den verwendeten Links im `[my Doc](../mydoc.md)` Format auch im nativen Markdown Format (ohne Hugo Generierung) mittels Mausklick vernünftig navigiert werden kann. 

#### Test01: MarkdownMonsters Preview Navigation
Navigating the *.md-links in MarkdownMonsters Preview: 

#### Test02: GitHub Navigation
Once the HugoPoject is uploaded to GitHub and opening those files in the GitHub Editor in View-Mode, link-click-naviating to other *.md linked Markdown-Files must be possible. 

### 2. HTML-Navigation
Hier geht es darum die Navigation für alle [Navigationsarten](#navigationsarten) für die mit Hugo generierten *.html-Dateien zu testen. 

#### Test11: local InMemory Server
When generating the HugoSite with the `hugo server`-command that does not generate the *.html files physically in the /public output folder, but keeps them in memory, all [types of web-navigation](#navigationsarten) must work. 

#### Test12: local http Server  
This about the hugo generated `/public`-folder running on a local http-server such as httpsrv

#### Test13: Netlify  
When the generated *.html files are published via Netlify

#### Test14: Forestry  
When the generated *.html files appear in the Forestry Editor's Website-Preview

#### Test15: AWS  
When the generated *.html files are published on an AWS Server


## Navigationsarten
In den zu generierenden Webseiten kommen Hyperlinks an verschiedenen Orten vor:

1. Im Dokumenten-text
2. Im Menu
3. In Selektionsleisten (Treeview)
4. Im Header
5. Im Footer
6. Im Logo
7. in Bildern 
8. in PopUps

Eine funktionierende Lösung muss immer alle Arten abdecken!

### Setup

### OutOfTheBox Outcome



## Roadmap
See the open issues for a list of proposed features (and known issues).

## Installation
-> Project Setup for Hugo, Theme, GitHub, Netlify and Forestry see this folder's [_underscore file](../_DeltaThemeExplore_a.md)


## Usage
Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

For more examples, please refer to the Documentation

## Technical Stuff 
`(for Developers and Contributors`)

### Architecture
This section should list any major frameworks that you built your project using. Leave any add-ons/plugins for the acknowledgements section. Here are a few examples.

* Bootstrap
* GoLang
* HUGO
* Node
* NPM
* Webpack
* HTML 5.0

### Contributing
Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are greatly appreciated.

1. Fork the Project
2. Create your Feature Branch (git checkout -b feature/AmazingFeature)
3. Commit your Changes (git commit -m 'Add some AmazingFeature')
4. Push to the Branch (git push origin feature/AmazingFeature)
5. Open a Pull Request

## Getting Started
  
This is an example of how you may give instructions on setting up your project locally. To get a local copy up and running follow these simple example steps.
### Purpose

### Scope

### Documentation and Links

## Contacts

### Owner 
**René Baron, Zurich**
- [LinkedIn](https://www.linkedin.com/in/rene-baron/)
- [github](https://github.com/realB12 "Rene Baron on github")
- [Email](mailto:rene.baron@baronsolutions.ch?subject=Hi% "Hi!")
- [Website](https://myrasis.com "Welcome")

Project Link: https://github.com/your_username/repo_name

## Acknowledgements

## License
Distributed under the MIT License. See [LICENSE](LICENCE.md) for more information.