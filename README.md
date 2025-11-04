<p align="center">
<img src="https://raw.githubusercontent.com/RoxDevvv/Unity-Blender-Control-Style/Alpha/logo.png" alt="Logo">
</p>


# Unity Blender Controller (Fork with ProBuilder Enhancements)

Blender-style transform plugin for Unity with improved ProBuilder integration.


## Overview

This plugin brings Blender-style transform controls to the Unity Scene (keys `G`, `S`, `R`).
In this fork, we added native alignment to ProBuilder "Element" orientation across Move, Rotate, and Scale,
respecting the Local axis of the selected element (Face/Edge/Vertex) and avoiding conflicts with `Tools.pivotRotation`.


## Installation

Prerequisites:
- Unity 2021.3+ (tested), Editor Tools enabled
- ProBuilder installed via UPM

Optional dependency (Pie Menu):
1) Open your Unity project.
2) Go to `Window > Package Manager`.
3) Click the `+` button and select `Add package from git URL...`.
4) Paste:
```
https://github.com/JonasWischeropp/unity-scene-view-pie-menu.git#1.1.0
```
5) Install and wait to finish.

Install this fork (two options):
- Via Git URL (recommended):
  1) `Add package from git URL...`
  2) Paste:
  ```
  https://github.com/GabrieldAlencon/Unity-Blender-Control-Style.git?path=/Assets/UnityBlenderControl
  ```

- Via Disk (local):
  1) `Add package from disk...`
  2) Select the `package.json` under `Assets/UnityBlenderControl` in your local clone.

    
## Usage

General (Object):
- Select an object in the scene.
- Press `G`/`S`/`R` to move/scale/rotate.
- Type a number to apply a precise value; `-` flips direction.
- Right-click to cancel; release the key to confirm.

ProBuilder (Element):
- Enter ProBuilder edit mode and set `Orientation: Element`.
- Select Face/Edge/Vertex.
- `G`/`S`/`R` respect the element’s Local axis.
- Axis lock (`X`, `Y`, `Z`) follows the element orientation when in Local; Global remains unchanged.


## Preview

![caption](https://raw.githubusercontent.com/RoxDevvv/Unity-Blender-Control-Style/Alpha/Preview.gif)

## Quick Validation (ProBuilder Element)
- Orientation: Element enabled.
- Select an inclined Face and press `R`; lock `X/Y/Z` and confirm rotation along the element axis.
- Select an Edge and press `S`; lock `X/Y/Z` and confirm scaling along the edge axis.
- Select vertices and use `G` with `X/Y/Z`; confirm movement aligned to the selection.
- Observe UVs and Normals stable after applying.

## Key Changes in This Fork
- Local axis alignment to the active element in `G`, `S`, `R`.
- Axis lock respects ProBuilder Element context without changing `Tools.pivotRotation`.
- UVs, Normals, and Bounds refreshed after transforms to avoid artifacts.

## Compatibility
- Unity 2021.3+ (tested)
- ProBuilder (current UPM version)
- EditorTools enabled

## Support

Open an issue in your fork/repo. For private support, use the original email: aminelaaraf@gmail.com.


## Contributing

- Use PRs with a clear description (problem, solution, validation).
- Keep commits small and descriptive.
- Include manual test steps (see Quick Validation).

## Recommended Best Practices
- Maintain a `CHANGELOG.md` with entries per release/fix.
- Document supported Unity/ProBuilder versions.
- Add a `CONTRIBUTING.md` and issue/PR templates.
- Include installation instructions via Git URL and Disk.
## License

This project is licensed under MIT.


## 💸 Donation
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/roxdevvv)
