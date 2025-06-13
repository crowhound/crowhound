# Important to anyone reading this in June 2025.
I am currently updating the repos read me, adding images, manuals, and videos for tutorials. 
If you see some sections that don't look completed, I might be currently working on it.

## Hi there, I am Jonathan Westfall. 👋
----
### :hammer_and_wrench: Languages and Tools:

<div>
 <img src="https://github.com/devicons/devicon/blob/master/icons/csharp/csharp-original.svg" title="C#" **alt="C#" width="40" height="40" align="left"/>
 <img src="https://github.com/devicons/devicon/blob/master/icons/dotnetcore/dotnetcore-original.svg" title="Dot Net Core" **alt="Dot Net Core" width="40" height="40" align="left"/>
 <img src="https://github.com/devicons/devicon/blob/master/icons/blazor/blazor-original.svg" title="Blazor" **alt="Blazor" width="40" height="40" align="left"/>
</div>
<div>
 <img src="https://github.com/devicons/devicon/blob/master/icons/github/github-original.svg" title="Github" **alt="Github" width="40" height="40" align="left"/>
 <img src="https://github.com/devicons/devicon/blob/master/icons/githubactions/githubactions-original.svg" title="Github Actions" **alt="Github Actions" width="40" height="40" align="left"/>
</div>
<div>
 <img src="https://github.com/devicons/devicon/blob/master/icons/javascript/javascript-original.svg" title="Javascript" **alt="Javascript" width="40" height="40" align="left"/>
 <img src="https://github.com/devicons/devicon/blob/master/icons/react/react-original.svg" title="React" **alt="React" width="40" height="40"/>
</div>

## Readme Legend 
If you see the black arrow below it is a Collapsible section that opens up to show more stuff
<details>
  <summary>Collapsible example</summary>
  Sections are being formatted into Collapsible sections to make it easer for people to read only what they are interested in. 
</details>


## Multithreaded Mesh Generation 

> [!TIP]
> The image below is a clickable link to a YouTube video.

[![Project Update Vieo Link](https://github.com/user-attachments/assets/2ee82c99-f9fe-4223-8c20-18411ac34b9b)](https://www.youtube.com/watch?v=ryP10BY_mN0)

<details>
  <summary>Multithreaded Procedural Mesh Generation</summary>
  
### Mesh Generation Overvieww
> Credit to CatLikeCoding for helping provide vast amount of resources for mesh generation math.

Created a series of Mesh Jobs that implement an IMeshGenerator to procedurally generate different shapes.

IMeshGenerator defines the base implementation for executing a C# job that generates shapes procedurally.
It includes fields for Vertex and Index count for the generated mesh.

IMeshStream is used to initialize the C# Job for procedural data creation used in meshes like defining the Triangles, SetVertex positions and calculating the bounds.

MeshJob is used to schedule jobs defined in the IMeshGenerator being implemented by the chosen ProceduralMeshs and to also pass in the IMeshStream.

### Usecase
This is being used in the ocean generator I am working on.
Also useful for a work in progress sprite mesh generation tool I am working on for a custom 2D navmesh and raymarhcing system.
</details>

## Current Project Video Link


TODO: I am grabbing a screen shot for the video link below.

[Metroidvania Room System First Test](https://www.youtube.com/watch?v=7L397Th6BX4)

## Reminder for the SF Unity packages:
The packages are just preparing for early Alpha releases. Somethings will have code updates from alpha release to alpha release that might cause breaking API changes.
There are a couple bugs we know about and some of them are related to a Unity Engine bug that a lead dev at Unity has already found a fix for and is going already through QA in early June.


## Updates to community repos
The SF Platformer package is being updated in the Shatter Fantasy organization's SF-Metroidvania repo at the moment.
After the SF Metroidvania reaches the next major milestone the updates for the SF PLatformer will be merged into the SF Platformer repo as a standalone tool.

The SF Metroidvania package has a lot more than just the SF Platformer features. It has been heavily updated with a lot of features. 
The feature list will be added to the SF Metroidvania readme and manual pages little over time. Currently the recordings for video documentation is my priority. 
There is a lot more medium and small features in it, but will mention them on the dedicated page for it located at the following link.

[SF Metroidvania Package](https://github.com/Shatter-Fantasy/SF-Metroidvania)

## Self Learning Repos
<!--
Special thanks to Andre McGrail (Verasl) and Brendan Duncan for providing a great learning resource to start with for Gerstner Waves in Unity's Boat-Attack demo project. 

-->

First one was a short Multithreading learning project for Unity DOTS to implement multithreaded enemy movement and stratgey game selection.
This one is small because I moved over to the ocean generator for multithreading. 

[Multithreading RTS Demo](https://github.com/crowhound/Multithreaded-RTS-DOTS-Demo)

Second one is a First Person Metroidvania. I will release the source code after cleaning up the SF Utilities stuff I have been working on for shaders.
The shader and rendering stuff hasn't been passed to the public repo yet for SF Utilities. Need to clean up the ocean light data structs used by shaders.
This one has a combat visor system for scanning objects and adding the scan data to a log and also an x-ray visor system. Both inspired by Metroid Prime 1.

> Early work in progress x-ray visor that can see through certain walls and objects.

![X Ray Visor](https://github.com/user-attachments/assets/4755f6a3-e9da-4136-86b5-125bea7a1684)


### SF Platformer Unity community package
Development was shifted to the SF-Metroidvania package.
After the next major release the updates will be merged into the SF-Platformer package, but right now the SF-Metrdoivania package is where a lot of the development is.
It has a vast amount of improvements for physics, camera systems, and a lot more.

### Other SF Unity community packages

[Shatter Fantasy GitHub Organization Page](https://github.com/Shatter-Fantasy)

[Shatter Fantasy UI Elements Tools](https://github.com/Shatter-Fantasy/SF-UI-Elements)

[Shatter Fantasy Utilities](https://github.com/Shatter-Fantasy/SF-Utilities)

> [!WARNING]
> The SF Sprite Tools package are currently in very experimental testing. 
> It is in early pre-alpha currently and can throw errors in rare cases  when using the multi sprite editing tool for creating animations. <br/>
> Test the SF Sprite Tools in a new project. Do not use the pre-alpha package in a project that already exists till it is more stable.
> Read the install instructions carefully that are located in the read me at the following link.
> There is no documentation on it yet. To open the SF Sprite Editor look for the top menu bar menu for SF/2D/Sprite Editor.

[Shatter Fantasy Sprite Tools](https://github.com/crowhound/SF-Sprite-Tools)


### Other Recent Self-Learning 
Last self learning projects were aimed at combining the things I already knew about DocFX and GitHub Actions to auto generate C# and .net documentation for projects and tools API for users to read through.
DocFX is used to generate YAML, markdown, and HTML files from a set of C# and .net files. 
GitHub Actions is used to auomatically publish the documentation to a website for people to visit and learn from. 

Example link for the current SF Metroidvania API documentation. Do note that I haven't set up the manual for the documentation or the home page yet. At the moment the home page mirrors the default read me file for packages.
Second link is to the GitHub Action code that I used to generate the documentation. I will make an example page on how to set up the config file later for people wanting to generate documentation themselves.

[SF Metroidvania Early WIP Documentation ](https://shatter-fantasy.github.io/SF-Metroidvania/api/SF.Characters.Controllers.html)

[GitHub Action Code](https://github.com/Shatter-Fantasy/SF-Metroidvania/blob/alpha-release-pages/.github/workflows/documentation.yml)

<!--
### Want To Support Future Community Tools.
For anyone wanting to support me, when I release the first set of public tools for the community you can donate on Ko-Fi.
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/I2I4XDBZE)


-->
