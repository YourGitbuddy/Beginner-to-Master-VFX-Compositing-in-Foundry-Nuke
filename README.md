Perfect 💪 — here’s your copy-paste ready Markdown version with Shields.io badges, clean formatting, and bold sectioning for your Nuke Compositing tutorial.
You can paste this directly into GitHub, Notion, or any Markdown viewer — it will render beautifully.


---

# 🎬 **From Beginner to Master: The Complete Nuke Compositing Tutorial**

> *A structured learning guide for aspiring VFX compositors — master Foundry Nuke from fundamentals to film-level production.*

---

## 🧠 Table of Contents  
[![](https://img.shields.io/badge/Level-Beginner-green?style=flat-square)]()  
[![](https://img.shields.io/badge/Level-Intermediate-yellow?style=flat-square)]()  
[![](https://img.shields.io/badge/Level-Advanced-blue?style=flat-square)]()  
[![](https://img.shields.io/badge/Level-Master-red?style=flat-square)]()

1. [Introduction](https://github.com/YourGitbuddy/Beginner-to-Master-VFX-Compositing-in-Foundry-Nuke/edit/main/README.md#-introduction)  
2. [What is Compositing?](#what-is-compositing)  
3. [Getting Started with Nuke](#getting-started-with-nuke)  
4. [Beginner Level](#beginner-level)  
5. [Intermediate Level](#intermediate-level)  
6. [Advanced Level](#advanced-level)  
7. [Master Level](#master-level)  
8. [Pipeline & Workflow](#pipeline--workflow)  
9. [Compositing Examples](#compositing-examples)  
10. [Project Example](#project-example)  
11. [Final Notes](#final-notes)

---

## 🎥 Introduction  
![](https://img.shields.io/badge/Software-Nuke-orange?style=for-the-badge&logo=thefoundry&logoColor=white)
![](https://img.shields.io/badge/Skill-VFX_Compositing-blue?style=for-the-badge)
![](https://img.shields.io/badge/Format-Tutorial-lightgrey?style=for-the-badge)

Welcome to **From Beginner to Master: The Complete Nuke Compositing Tutorial** —  
a project designed for artists who want to **learn, understand, and master** the art of digital compositing in **The Foundry Nuke**.

### 🧩 Why Learn Nuke?
- Industry standard for VFX compositing  
- Used by studios like MPC, Framestore, Weta, and ILM  
- Non-destructive **node-based workflow**  
- Perfect for **film, OTT, ads, and cinematics**

---

## 🧩 What is Compositing?  
![](https://img.shields.io/badge/Concept-Visual_Integration-success?style=flat-square)
![](https://img.shields.io/badge/Core-Skill-yellow?style=flat-square)

Compositing is the process of **combining multiple visual elements** (live-action, CG, matte paintings, FX passes, etc.) into a single seamless shot that looks like it was captured in-camera.

### 🧱 Core Idea
Each visual layer contributes to the final look — color, light, shadows, and motion must all match.

---

## 💻 Getting Started with Nuke  
![](https://img.shields.io/badge/Step-Setup-important?style=flat-square)
![](https://img.shields.io/badge/Version-NukeX_15.0+-brightgreen?style=flat-square)

### 🔧 Installation
- Download from [Foundry’s official website](https://www.foundry.com/products/nuke)
- *Nuke Non-Commercial* is free for learning.

### 🧭 Interface Overview
**Key Areas:**
- Viewer — see your final result  
- Node Graph — connect all nodes  
- Properties Panel — control node parameters  
- Toolbar — add tools like Merge, Grade, Blur  

---

## 🟢 Beginner Level  
![](https://img.shields.io/badge/Focus-Fundamentals-green?style=for-the-badge)
![](https://img.shields.io/badge/Progress-25%25-brightgreen?style=for-the-badge)

### 🎯 Objective
Learn **foundational compositing techniques** and understand **how Nuke nodes work**.

---

### 🧩 Node Basics  
![](https://img.shields.io/badge/Node-Read-blue)
![](https://img.shields.io/badge/Node-Merge-orange)
![](https://img.shields.io/badge/Node-Grade-yellow)

Nodes are building blocks in Nuke.  
Each performs an operation — reading, merging, grading, transforming, or blurring.

[Read] → [Grade] → [Blur] → [Merge] → [Viewer]

---

### 🎬 Basic Keying  
![](https://img.shields.io/badge/Technique-Keying-blue)
![](https://img.shields.io/badge/Node-Keylight-lightgrey)
![](https://img.shields.io/badge/Node-IBKGizmo-orange)

Steps:
1. Import footage (`Read`)  
2. Add `Keylight` node  
3. Pick screen color  
4. Adjust clip black/white  
5. Merge keyed footage over background  

---

### 🎨 Color Correction  
**Nodes:** `Grade`, `HueCorrect`, `ColorLookup`

Example Flow:

[CG Render] → [Grade] → [Merge BG] → [Viewer]

---

### 🎯 Tracking Basics  
**Node:** `Tracker`  
Used for stabilization or screen insert work.

[Plate] + [Tracker] → [Stabilized Output]

---

## 🟡 Intermediate Level  
![](https://img.shields.io/badge/Focus-Production_Work-yellow?style=for-the-badge)
![](https://img.shields.io/badge/Progress-50%25-yellow?style=for-the-badge)

Learn **Rotoscoping, Cleanup, and AOV Management.**

---

### ✂️ Rotoscoping & Masks  
![](https://img.shields.io/badge/Tool-Roto-blue)
![](https://img.shields.io/badge/Tool-RotoPaint-red)

Example:

[Read Plate] → [Roto Mask] → [Merge Background]

---

### ⚙️ Working with AOVs (Render Passes)  
![](https://img.shields.io/badge/AOVs-Diffuse_•_Specular_•_Z--Depth-informational?style=flat-square)

[Read EXR] → [Shuffle Diffuse] + [Shuffle Specular] → [Merge Add]

---

### 🧹 Cleanup Techniques  
Use:
- `RotoPaint` (Clone Tool)  
- `FrameHold + Transform`  
- `SmartVector + VectorDistort`

[Plate] + [RotoPaint Patch] → [Clean Plate]

---

### 🎥 Camera Tracking  
**Node:** `CameraTracker`  
Reconstructs 3D camera motion to attach CG.

---

## 🔵 Advanced Level  
![](https://img.shields.io/badge/Focus-3D_Compositing-blue?style=for-the-badge)
![](https://img.shields.io/badge/Progress-75%25-blue?style=for-the-badge)

---

### 🌐 3D Compositing in Nuke  
**Nodes:** `ScanlineRender`, `Camera`, `Card`, `Scene`

[Read Plate] → [Card + Texture] → [Scene] → [ScanlineRender]

Used for matte projections or set extensions.

---

### 🌊 Deep Compositing  
**Nodes:** `DeepMerge`, `DeepRecolor`, `DeepToImage`

[Deep Render 1] + [Deep Render 2] → [DeepMerge] → [DeepToImage]

---

### 💡 Relighting  
Use Normal & Position passes:

[CG Render + Normal Pass + Position Pass] → [Relight]

---

### 🎨 Color Management (ACES)  
Set OCIO Config → Match input/output spaces

[ACEScg Render] → [OCIO Config] → [sRGB Output]

---

## 🔴 Master Level  
![](https://img.shields.io/badge/Focus-Film_Integration-red?style=for-the-badge)
![](https://img.shields.io/badge/Progress-100%25-red?style=for-the-badge)

---

### ⚡ Shot Integration  
Blend **live-action + CG** using:
- Grain matching  
- Defocus  
- Lens distortion  
- Light wrap  

---

### 🧽 Advanced Cleanup  
**Nodes:** `PlanarTracker`, `SplineWarp`, `GridWarp`, `VectorDistort`

---

### 🐍 Pipeline Automation (Python in Nuke)  
![](https://img.shields.io/badge/Automation-Python_3.9+-yellow?style=flat-square)
![](https://img.shields.io/badge/API-Nuke_Scripting-blue?style=flat-square)

```python
import nuke

def auto_read(filepath):
    node = nuke.createNode("Read")
    node["file"].setValue(filepath)
    return node

auto_read("/shots/seq01/plate_v001.exr")

```


---

🔁 Pipeline & Workflow

 

[Modeling] → [Texturing] → [Lighting] → [Rendering] → [Compositing] → [Final Output]

Compositor’s Role:

Final visual integration

Ensure realism and continuity

Collaborate with Lighting/FX teams



---

🎨 Compositing Examples

Example	Breakdown

Sci-Fi Portal	[Actor Plate] + [Energy FX] + [Light Wrap] + [Lens Flare]
Invisible Man	[Plate] + [Clean BG] + [Roto Body] + [Refraction FX]
Time Freeze	[Plate] + [Static BG] + [Speed Ramp]
Magic Energy	[Plate] + [Emissive FX] + [Shockwave]
Car Chase Dust	[Car Plate] + [Dust FX] + [Motion Blur]



---

🎬 Project Example — Spaceship Landing Sequence

Inputs:

Desert Plate

CG Spaceship Renders

Dust FX Simulation

Sky Matte Painting


Goal: Seamlessly integrate all into a cinematic landing shot.

[Read Plate]
[CG Renders (Diffuse, Specular)]
[Dust FX]
[Sky Matte]
 → [Merge]
 → [Color Grade]
 → [Lens Distortion]
 → [Output]


---

✨ Final Notes

 

> “A compositor is a visual storyteller — crafting illusion through light, depth, and emotion.”



🎓 After completing this tutorial, you’ll be able to:

Work confidently in Foundry Nuke

Create production-level composites

Build professional demo reels

Apply for junior to mid-level compositor roles



---

🖌️ Designed with ❤️ using Markdown + Shields.io

---

Would you like me to make a **PDF-ready version** of this Markdown (with logo headers, color blocks, and proper page layout) next?  
It’ll look cinematic like a real course brochure.
