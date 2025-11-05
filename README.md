
# 🎬 **From Beginner to Master: The Complete Nuke Compositing Tutorial**

> *A structured learning guide for aspiring VFX compositors — master Foundry Nuke from fundamentals to film-level production.*

---

## 🧠 Table of Contents
1. [Introduction](#introduction)
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

Welcome to **From Beginner to Master: The Complete Nuke Compositing Tutorial** —  
a project designed for artists who want to **learn, understand, and master** the art of digital compositing in **The Foundry Nuke**.

### 🧩 Why Learn Nuke?
- Industry standard for VFX compositing  
- Used by studios like MPC, Framestore, Weta, and ILM  
- Non-destructive **node-based workflow**  
- Perfect for **film, OTT, ads, and cinematics**

---

## 🧩 What is Compositing?

Compositing is the process of **combining multiple visual elements** (live-action, CG, matte paintings, FX passes, etc.) into a single seamless shot that looks like it was captured in-camera.

### 🧱 Core Idea
Each visual layer contributes to the final look — color, light, shadows, and motion must all match.

---

### 🎨 Basic Compositing Flow

[Live Action Plate] + [CG Element] + [Smoke FX] + [Color Correction] → [Final Shot]

---

### 🧩 More Compositing Examples

**1. Sky Replacement**

[Original Plate] + [Roto Sky Area] + [New Sky Matte] + [Color Balance] → [Final Composite]

**2. Day to Night Conversion**

[Day Plate] + [Color Grade (Cool Tone)] + [Light Glow FX] + [Streetlight Pass] → [Night Look]

**3. Rain or Weather FX**

[Clean Plate] + [Rain FX Layer] + [Wet Reflection Pass] + [Defocus + Grain] → [Rainy Composite]

**4. Set Extension**

[Live Plate] + [CG Building Extension] + [Shadow Pass] + [Atmospheric Fog] → [Integrated Shot]

**5. Fire/Explosion Integration**

[Plate with Actor] + [Explosion Element] + [Smoke & Debris FX] + [Glow + Light Wrap] → [Final Blast Shot]

**6. Hologram / Sci-Fi Interface**

[Actor Plate] + [HUD Graphics] + [Screen Glow] + [Color Tint + Flicker] → [Hologram Composite]

**7. Underwater Scene**

[Plate] + [Caustics Pass] + [Bubbles FX] + [Blue-Green Grade] + [Depth Fog] → [Underwater Final]

**8. Creature Integration**

[Plate] + [CG Creature] + [Shadow Pass] + [Ambient Occlusion] + [Color Grade] → [Creature in Scene]

**9. Miniature / Scale Shot**

[Model Footage] + [Background Plate] + [Depth of Field] + [Color Match + Grain] → [Realistic Scale Shot]

**10. Futuristic City**

[Plate] + [CG Skyscrapers] + [Aerial Perspective] + [Light Pass + Fog] → [Futuristic Skyline]

---

## 💻 Getting Started with Nuke

### 🔧 Installation
- Download Nuke from [Foundry’s official website](https://www.foundry.com/products/nuke)
- Versions: *Nuke Non-Commercial* is free for personal learning

### 🧭 Interface Overview

+------------------------------------------------+ | Viewer | Toolbar | Node Graph | Properties Pane | +------------------------------------------------+

### 🔍 Key Areas
- **Viewer:** Where your final result is displayed  
- **Node Graph:** The workspace where you connect nodes  
- **Properties Panel:** Adjust settings of selected nodes  
- **Toolbar:** Add nodes like Merge, Read, Transform  

---

## 🟢 Beginner Level

### 🎯 Objective
Learn **foundational compositing techniques** and understand **how Nuke nodes work**.

---

### 🧩 1. Understanding Nodes

Nodes are **building blocks** in Nuke.  
Each node performs a specific operation — like reading an image, merging two elements, or adjusting colors.

[Read Footage] → [Grade] → [Blur] → [Merge] → [Viewer]

| Node | Description |
|------|--------------|
| `Read` | Imports an image or sequence |
| `Merge` | Combines two images |
| `Grade` | Adjusts brightness, contrast, gamma |
| `Transform` | Moves or scales an image |
| `Blur` | Softens details |

---

### 🎬 2. Basic Keying

**Keying** removes a green or blue background from footage.  
You’ll learn to use:
- `Keylight` node (powerful chroma key tool)
- `IBKColour` & `IBKGizmo` (for advanced setups)

**Keying Steps:**
1. Import footage (`Read`)  
2. Add `Keylight` node  
3. Pick screen color  
4. Adjust clip black/white  
5. Merge keyed footage over background  

---

### 🎨 3. Color Correction

Used to **match lighting, tone, and exposure** between elements.

**Key Nodes:**
- `Grade` – Adjust levels  
- `HueCorrect` – Adjust specific colors  
- `ColorLookup` – Apply curves or LUTs  

Example Flow:

[CG Render] → [Grade] → [Merge BG] → [Viewer]

---

### 🎯 4. Basic Tracking

**Tracking** follows the motion of an object or camera in the footage.

- `Tracker` node captures 2D movement  
- Use it to stabilize footage or attach CG elements

Example:

[Plate] + [Tracker] → [Stabilized Footage or Screen Insert]

---

## 🟡 Intermediate Level

### 🎯 Objective
Learn **Rotoscoping, AOVs, and cleanup techniques** for real production work.

---

### ✂️ 1. Rotoscoping & Masks

**Roto:** Drawing shapes to isolate areas (like a person or object).  
**RotoPaint:** Painting or cloning parts for cleanup.

Example:

[Read Plate] → [Roto Mask] → [Merge Background]

Tips:
- Animate roto shapes frame-by-frame  
- Use feathering for soft edges  

---

### ⚙️ 2. Working with AOVs (Render Passes)

CG renders often come with **AOVs** (Arbitrary Output Variables):
- Diffuse, Specular, Reflection, Shadow, Z-Depth, etc.

Use `Shuffle` nodes to extract each pass, then recombine.

Example:

[Read MultiPass EXR] ↓ [Shuffle Diffuse] [Shuffle Specular] → [Merge Add] → [Viewer]

---

### 🧹 3. Cleanup Techniques

Used to remove unwanted objects, rigs, or tracking markers.

**Methods:**
- `RotoPaint` (clone tool)
- `FrameHold` + `Transform`
- `SmartVector` + `VectorDistort`

Example:

[Plate] + [RotoPaint Patch] → [Clean Plate]

---

### 🎥 4. Camera Tracking

**Matchmove** or **Camera Tracking** reconstructs the 3D camera movement of a shot.

In Nuke:
- Use `CameraTracker`
- Solve the motion
- Attach 3D geometry or projections

---

## 🔵 Advanced Level

### 🎯 Objective
Build **complex 3D composites**, manage deep data, and handle realistic relighting.

---

### 🌐 1. 3D Compositing in Nuke

Nuke has an internal 3D workspace.

**Key Nodes:**
- `ScanlineRender`
- `Camera`
- `Card`
- `Scene`

Example:

[Read Plate] → [Card + Texture] → [Scene] → [ScanlineRender]

Use this to:
- Reproject matte paintings
- Place 3D elements in a scene  

---

### 🌊 2. Deep Compositing

**Deep Data** stores depth information per pixel.  
You can merge multiple 3D elements naturally without manually creating holdouts.

**Nodes:** `DeepMerge`, `DeepRecolor`, `DeepToImage`

Example:

[Deep Render 1] [Deep Render 2] ↓ [DeepMerge] ↓ [DeepToImage]

---

### 💡 3. Relighting

Using **Normal** and **Position** passes, you can change lighting in Nuke — no need to re-render!

Example:

[CG Render + Normal Pass + Position Pass] → [Relight] → [Viewer]

---

### 🎨 4. Color Management (ACES)

Professional VFX studios use **ACES (Academy Color Encoding System)**.

**Setup:**
- Use OCIO config in Preferences  
- Set correct color spaces for inputs/outputs  

Example Flow:

[ACEScg Render] → [Nuke OCIO Config] → [sRGB Output]

---

## 🔴 Master Level

### 🎯 Objective
Achieve **film-grade shot integration**, advanced cleanup, and pipeline automation.

---

### ⚡ 1. Shot Integration

The art of blending live action and CG seamlessly.  
Match **lighting, shadows, color temperature**, and **lens characteristics**.

Tip:
Use **grain matching**, **defocus**, and **chromatic aberration** to unify CG and plate.

---

### 🏞️ 2. Environment Compositing

Combine **matte paintings**, **sky replacements**, and **camera projections**.

Workflow:

[Matte Painting] ↓ [Project3D + Camera] ↓ [ScanlineRender] ↓ [Final Merge]

---

### 🧽 3. Advanced Cleanup

Includes **planar tracking**, **patch blending**, and **complex object removal**.

Tools:
- `PlanarTracker`
- `SplineWarp`
- `GridWarp`
- `VectorDistort`

---

### 🐍 4. Pipeline Automation (Python in Nuke)

```python
import nuke

def auto_read(filepath):
    node = nuke.createNode("Read")
    node["file"].setValue(filepath)
    return node

auto_read("/shots/seq01/plate_v001.exr")

Use scripts for:

Auto naming

File imports

Batch rendering
```


---

🔁 Pipeline & Workflow

VFX Pipeline Flow

[Modeling] → [Texturing] → [Lighting] → [Rendering] → [Compositing] → [Final Output]

💼 Compositor’s Role

Final layer of visual integration

Responsible for visual continuity and realism

Works closely with lighting and FX departments



---

🎨 Compositing Examples

1. Sci-Fi Portal Scene

[Actor Plate] + [Energy FX] + [Light Wrap] + [Lens Flare] → [Final Portal Shot]

2. Invisible Man Effect

[Plate] + [Clean Background] + [Roto Body] + [Displacement Refraction] → [Invisible Effect]

3. Time Freeze Shot

[Plate] + [Roto Moving Elements] + [Static BG Hold] + [Speed Ramps] → [Time Freeze Composite]

4. Magic Energy Shot

[Plate] + [Energy Element] + [Emissive Glow] + [Shockwave] → [Fantasy Composite]

5. Car Chase Dust Integration

[Car Plate] + [Dust FX] + [Motion Blur] + [Light Wrap + Grade] → [Dynamic Action Shot]


---

🎬 Project Example

Title: Spaceship Landing Sequence

Inputs:

Desert plate (live-action)

CG spaceship renders (multi-pass)

Dust FX simulation

Sky matte painting


Goal:
Blend all these into a believable shot of a spaceship landing in a desert.

Example Node Layout:

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

Build your own demo reels and breakdowns

Apply for junior to mid-level compositor roles
