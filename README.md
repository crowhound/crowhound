# Hi there, I am Jonathan Westfall. 

Currently working as a Unity community dev that enjoys working on physics systems and custom tool editors.
At the moment I am also working on tutorials for the community for Unity 6.5 and newer versions to help showcase how to use new features and help migrate over from older obsoleted features.

Starting in June 2026 I will be working on the UI Toolkit and Physics Core 2D Module tutorials and features.
Link to a new repo where I will be starting to add example demos that go along the videos I release to teach and help share information about new Unity features.

https://github.com/crowhound/UI-Toolkit-Tutorials

----



### Readme Legend
If you see the black arrow below it is a Collapsible section that opens up to show more stuff
<details>
  <summary>Collapsible example</summary>
  Sections are being formatted into Collapsible sections to make it easer for people to read only what they are interested in. 
</details>


### Languages and Tools:
These are the main tools and coding languages I work with. 
Currently I am moving stuff to .net 10 and learning the changes for it.

For my free tools I make for Unity I already have branches with 6.5 and 6.6 support.
Unity 6.6 is still in alpha as of current moment I typed this line of text, but will be entering beta soon.
I also already have CoreCLR ready API in my Unity packages via the new lifecycle management API Unity introduced in 
6.5 with entityID being used instead of instanceID.

Note I have years of expierence with React and Angular, but currently am not using them for work right now.
Switched to Blazor and Razor pages for the most part for web dev.

<div>
 <img src="https://github.com/devicons/devicon/blob/master/icons/csharp/csharp-original.svg" title="C#" **alt="C#" width="40" height="40"/>
 <img src="https://github.com/devicons/devicon/blob/master/icons/dotnetcore/dotnetcore-original.svg" title="Dot Net Core" **alt="Dot Net Core" width="40" height="40" />
 <img src="https://github.com/devicons/devicon/blob/master/icons/blazor/blazor-original.svg" title="Blazor" **alt="Blazor" width="40" height="40" />
 <img src="https://github.com/devicons/devicon/blob/master/icons/github/github-original.svg" title="Github" **alt="Github" width="40" height="40" />
 <img src="https://github.com/devicons/devicon/blob/master/icons/githubactions/githubactions-original.svg" title="Github Actions" **alt="Github Actions" width="40" height="40"/>
</div>


----

## Tutorial Repos

Note these repos are new as of June 2026 and being updated daily for the most part.
There are more than linked below already, but are set to private till I finish initial set up.

Unity UI Toolkit 6.5+ Tutorials

https://github.com/crowhound/UI-Toolkit-Tutorials


## Fan Remakes

![Screen shot of Oracle of Seasons wip](/assets/images/oos/oos-remake-01.PNG)

Whenever Unity adds a new feature or I want to learn something new I do small or fan-remake projects where I try to 
recreate game mechanic or entire games. This link goes to the ones I am doing right now.
Note I just recently started making pages for them and download links. At the moment only a small amount is there.

The current build is actually really outdated because I just did a month of major updates and doing QA tests before uploading it.

[Fan Remakes - Self Learning](pages/fan-remakes.md)


## Multithreaded Mesh Generation 

> [!TIP]
> The image below is a clickable link to a YouTube video.

[![Project Update Vieo Link](https://github.com/user-attachments/assets/2ee82c99-f9fe-4223-8c20-18411ac34b9b)](https://www.youtube.com/watch?v=ryP10BY_mN0)

<details>
  <summary>Multithreaded Procedural Mesh Generation</summary>
  
### Mesh Generation Overvieww
> Credit to CatLikeCoding for helping provide vast amount of resources for mesh generation math.

Created a series of Mesh Jobs that implement an IMeshGenerator interface to procedurally generate different shapes.

IMeshGenerator defines the base implementation for executing a C# job that generates shapes procedurally.
It includes fields for Vertex and Index count for the generated mesh.

IMeshStream is used to initialize the C# Job for procedural data creation used in meshes like defining the Triangles, SetVertex positions and calculating the bounds.

MeshJob is used to schedule jobs defined in the IMeshGenerator being implemented by the chosen ProceduralMeshs and to also pass in the IMeshStream.

### Usecase
This is being used in the ocean generator I am working on.
Also useful for a work in progress sprite mesh generation tool I am working on for a custom 2D navmesh and 
raymarching system. For 2D navmesh I use the Low Level Physics 2D API introduced in Unity 6.3. Note in 6.5 this was 
renamed to Physics Core 2D. 


### Credit to Unity URP Team
This Water Shader was done by learning from Unity's Boat Attack demo and creating a custom version of the Water HLSL files.
</details>


## Current Project Video Link

Currently using Unity's new Low Level Physics 2D API added in Unity 6.3 to create a Metroidvania game with interactble enviorments with good performance.
The new API is burst and job friendly allowing while making use of no memory allocation API calls to create a extednable physics system meant for performance
from the ground up.

Currently working on creating a custom TileMapShape using the low level physic 2D API for high performant collisions.
Note the videos for Physics Core 2D module, (formerly called Low Level Physics 2D) was before the SIMD code optimizations.
In Unity 6.6 some SIMD optimizations for CPU cycles was introduced by Unity. Some Physics scenes in my projects gained a 50% performance boost.
This was thanks to the introduction of multithreaded memory allocation support for some stuff and also introduction of some SIMD-accelerated type support in .Net.

[Unity Physics Core 2D Dynamic Particle Simulation - Test One](https://www.youtube.com/watch?v=AMQSOS6vLHM)


[Unity 2D Low Level Physics - Custom Tilemap Shape Demonstration](https://www.youtube.com/watch?v=8rAHIgDUw7U)

## Reminder for the SF Unity packages:
The packages are just preparing for early Alpha releases. Somethings will have code updates from alpha release to alpha release that might cause breaking API changes.
The goal is to get the first stable release with support for Unity 6.5 as minimum whilke having support for newer API when using Unity 6.6+.
One example is the UniqueStyleString introduced in 6.6 to improve UI Toolkit initialization performance which also vastly lowered memory allocations from UI Elements.

[UniqueStyleString Manual Page For Those Interested](https://docs.unity3d.com/6000.6/Documentation/ScriptReference/UIElements.UniqueStyleString.html)

## Updates to community repos
As of May 2026 The SF Metroidvania package and the SF Top Down Package are the main focus for development.
Both of them have had the SF Core and SF Utilities packaged embedded allowing for installing one package and that is it.
No dependencies or anything at all.

[SF Metroidvania Package](https://github.com/Shatter-Fantasy/SF-Metroidvania)

## Self Learning Repos
<!--
Special thanks to Andre McGrail (Verasl) and Brendan Duncan for providing a great learning resource to start with for Gerstner Waves in Unity's Boat-Attack demo project. 

-->


The RTS and X Ray Visor demos are now outdated and are being prepped to move to Unity 6.5 API.
Note the X Ray Visor is already finished and updated, but a couple other files in the project needs updated.
Mainly thanks to Unity adding improved depth texture support during the transparency Render Graph Pass.
This lowered the complexity of code and improved performance a lot.


First one was a short Multithreading learning project for Unity DOTS to implement multithreaded enemy movement and stratgey game selection.
This one is small because I moved over to the ocean generator for multithreading. 

[Multithreading RTS Demo](https://github.com/crowhound/Multithreaded-RTS-DOTS-Demo)

Second one is a First Person Metroidvania. I will release the source code after cleaning up the SF Utilities stuff I have been working on for shaders.
The shader and rendering stuff hasn't been passed to the public repo yet for SF Utilities. Need to clean up the ocean light data structs used by shaders.
This one has a combat visor system for scanning objects and adding the scan data to a log and also an x-ray visor system. Both inspired by Metroid Prime 1.

> Early work in progress x-ray visor that can see through certain walls and objects.

![X Ray Visor](https://github.com/user-attachments/assets/4755f6a3-e9da-4136-86b5-125bea7a1684)


### Other SF Unity community packages
Note the SF Utilities and SF UI Elements are now just part of the SF Core package.

[Shatter Fantasy GitHub Organization Page](https://github.com/Shatter-Fantasy)


> [!WARNING]
> The SF Sprite Tools package are currently in very experimental testing.
> I had to wait for some Unity 6.5 and Unity 6.6 API changes to go public first before making it a stable release.
> The new Sprite Editor and RenderSprite API is out in Unity 6.6 alpha already and Unity 6.5 also has it out now. Just need to implement it.
> 
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

This tells GitHub to read the yaml files in the Documentation folder and generate a website for manual and api documentation and deploy it online.
It auto updates on every merge into the alpha-release-pages branch.

[GitHub Action Code](https://github.com/Shatter-Fantasy/SF-Metroidvania/blob/alpha-release-pages/.github/workflows/documentation.yml)

<!--
### Want To Support Future Community Tools.
For anyone wanting to support me, when I release the first set of public tools for the community you can donate on Ko-Fi.
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/I2I4XDBZE)


-->
