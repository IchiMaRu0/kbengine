# KBEngine- An Open Source MMOG Server    Engine

![kbelogo1](https://github.com/IchiMaRu0/kbengine/blob/master/%E7%AC%AC%E4%BA%94%E7%BB%84-%E8%BF%9B%E5%BA%A6%E6%97%A5%E5%BF%97/pics/kbelogo1.png)





## Abstract

An open source MMOG server engine. 

Just use Python scripting to be able to complete any game logic simply and efficiently (supports hotfixing).

Various KBEngine plugins can be quickly combined with (Unity3D, OGRE, Cocos2d-x, HTML5, etc.) technology to form a complete game client.

The engine is written in C++, and saves developers from having to re-implement common server-side technology, allowing them to concentrate on game logic development, to quickly create a variety of games.





## Table of Contents

* Introduction
* Stakeholders
* Context View
* ...






## Introduction





## Stakeholders  

Stakeholders are the people that have interest in this Kbengine project and this organization. A stakeholder is a member of the "groups without whose support the organization would cease to exist". Stakeholders can obviously have their effect on the project's policy as well as the objective. In this section, we will firstly provide an overview of the different stakeholders identified by the project such as developers, maintainers, assessors users and so on. Hereafter, we will discuss how the issues and integrations are handled. <a href="#fig1">Figure 1</a> will show the summary of identified stakeholders of Kbengine based on the classification proposed by Nick Rozanski and Eoin Woods<sup><a href="#1">[1]</a></sup>.  



### Overview  

**Acquirers:**&nbsp;[YOLO Technology](https://www.comblockengine.com/aboutUs.html) is managing and growing the company and its assets.  


**Suppliers:**&nbsp;The development of Kbengine is coordinated via [Github](https://github.com), which can be safely classified as a supplier. Also, as Python is the scripting language for the engine, [Python](https://www.python.org/) is also regarded as a supplier.


**Developers:**&nbsp;Kbengine is supported by an open source [community](https://github.com/kbengine/kbengine/graphs/contributors) and by YOLO's engineers. In total, there are 25 Git contributors, among whom the top three recent contributors are:  

1. @[kbengine](https://github.com/kbengine/kbengine/commits?author=kbengine) 3,707 commits 
2. @[kebiao](https://github.com/kbengine/kbengine/commits?author=kebiao)  367 commits
3. @[basesrv](https://github.com/kbengine/kbengine/commits?author=basesrv) 89 commits. 

Developers deploy the Kbengine software and try to polish it.  

**Communicators:**&nbsp;There is a large [community](https://bbs.comblockengine.com/) for this highly-regarded open source project. More than four thousand active communicators are now in the community, continuing explaining the system to other stakeholders via documentation and other materials like demos.  


**System adminstrators:**&nbsp;Due to the features of the open source project, it is relatively difficult to draw a conclusion on who the adminstrator is, but there is no denying that [YOLO Technology](https://www.comblockengine.com/aboutUs.html) works as a regular adminstrator.

**Testers:**&nbsp;Testers test the project to ensure that it is suitable for game development. Users as well as developers all serve as the testers for this project.  

**Users:**&nbsp;This group include both big companies like [Electronic Soul](https://www.dianhun.cn/) and average users who are attempting developing their own games.  

**Competitors:**&nbsp;Undoubtedly, competitors are interested in the development of Kbengine since they are willing to provide a competing service. [Unreal](https://www.unrealengine.com/zh-CN/what-is-unreal-engine-4) and [Unity3D](https://unity3d.com/cn) are two big names with the most users worldwide. The former one is widely viewed as one of the most powerful engine for  and the latter one is suitable for beginners around the world. Nevertheless, when it comes to the game server engine or framework, [POMELO](http://pomelo.netease.com/) and [SKYNET](https://github.com/korialuo/skynet) are two that win most reputation.


<a name="fig1"><div align=center>![Figure 1](https://github.com/IchiMaRu0/kbengine/blob/master/%E7%AC%AC%E4%BA%94%E7%BB%84-%E8%BF%9B%E5%BA%A6%E6%97%A5%E5%BF%97/pics/figure1.jpeg)</div></a>

### Power-Interest Grid  

The power-interest grid contains the main stakeholder categories, as shown in <a href="#fig2">Figure 2</a>. There is no doubt that the core developer team takes the leading position in the figure. Suppliers like Github are also significant because the open source project highly depends on these third-party dependencies. Whereas, they apparently have little interest in this project. On the contrary, it is the users that have the highest interest while possess the lowest power.   

<a name="fig2"><div align=center>![Figure 2](https://github.com/IchiMaRu0/kbengine/blob/master/%E7%AC%AC%E4%BA%94%E7%BB%84-%E8%BF%9B%E5%BA%A6%E6%97%A5%E5%BF%97/pics/figure2.jpeg)</div></a>



## Context View

A context view describes the relationships, dependencies, and the interactions between the system and its environment. This view is relevant for the system's architecture and defines the boundaries of the system and how it interacts with external entities across these boundaries. [Figure 3]() shows the context view of KBEngine.



### System Scope

KBEngine is an open source game server engine. The client can communicate with the server through a simple protocol.  It saves developers from having to re-implement common server-side technology, allowing them to concentrate on game logic development, to quickly create a variety of games. It can be applied in:

* Game server
  * Chess
  * arpg
  * mmorpg
  * moba

* Non-game server
  * H5 check in server
  * H5 multiplayer app server
  * Communication relay server

* Any other aspects that need server communication



### Client

KBEngine is a server engine, but it can be combined with some client engines to form a complete game client. It is aimed at client development. By using its SDK, what the client developer needs to do is just receiving event data and completing the rendering. Now it supports several of the most popular client engines on the market, including:

* Ogre    [https://www.ogre3d.org/](https://www.ogre3d.org/)
* Unity3d    [https://unity3d.com](https://unity3d.com)
* UnrealEngine    https://www.unrealengine.com
* Cocos2dx    [http://www.cocos.com](http://www.cocos.com)
* HTML5-based engines or HTML5 pages



### Build-in Tools

KBEngine has many build-in tools to help developers to work easier. They are not dependencies in the sense that KBEngine cannot work without them, but can be thought of as additional features of  this project:

* `Installer Installation Assistant`:  A simple Python scripting tool that can install, uninstall, update and review versions, etc.
* Excel Tool - `pyxlsx`:  It provides the artifacts for planning, you can output the excel file, which is produced in a certain format, into the .py file used by the server and the .json file used by the client.
* Debug Tools
  * GUIConsole
  * WebConsole
  * PyCluster
  * bots



### Other External Entities

* **Developing languages:**

  * The server's underlying framework is written in C++

  * The game logic layer uses Python(supports hotfixing)

* **Platforms:**  
  * PS4
  * X-BOX ONE
  * NINTENDO SWITCH
  * macOS 
  * Windows 
  * Linux 
  * HTML5 
  * iOS
  * Android
* **IDE for programming:**  Visual Studio for Windows
* **Communication tools:**  Github
* **Dependencies:**
  * MySQL
  * Python （When you wants to use the tools provided by the engine）
  * Office 2010 or above (When you wants to use the build-in tool `pyxlsx`)
* **Testing:**  Most of the tests can be run on the client servers, using C++ or python
