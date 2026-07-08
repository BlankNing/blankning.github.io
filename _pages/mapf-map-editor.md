---
title: "MAPF Grid Map Editor — draw & export Moving AI .map files"
permalink: /tools/mapf-map-editor/
layout: single
author_profile: true
description: "Free, browser-based MAPF grid map editor — draw obstacles and terrain, import and export Moving AI .map files, and create benchmark maps for multi-agent path finding, all in your browser."
excerpt: "A free online grid map editor for creating and editing Multi-Agent Path Finding (MAPF) benchmark maps in the Moving AI .map format."
---

A **free, browser-based grid map editor** for building and editing
**Multi-Agent Path Finding (MAPF)** benchmark maps in the
[Moving AI](https://movingai.com/benchmarks/mapf.html) `.map` format. Use it as a MAPF map
maker, a Moving AI `.map` generator, or a quick obstacle-grid creator — it runs entirely in
your browser, so nothing is uploaded to a server and everything you draw stays on your machine.

<p style="margin:1.5em 0">
  <a href="/tools/mapf-map-editor.html" target="_blank" rel="noopener"
     style="display:inline-block;padding:12px 22px;background:#0b76d0;color:#fff;
            border-radius:8px;font-weight:600;text-decoration:none;">
    Launch the editor &rarr;
  </a>
</p>

## Why I built it

MAPF research relies on shared benchmark maps so that different planners can be compared on
the same problems. These maps use the de-facto standard **Moving AI `.map`** format, which is
simple but tedious to hand-write. This editor lets me sketch obstacle layouts visually,
tweak them, and export a valid `.map` file ready to drop into a benchmark set — or import an
existing map to inspect and modify it.

## How it works

**Drawing tools.** Choose a tool and paint directly on the grid:

- **Paint** — click or drag to fill cells with the selected terrain.
- **Erase** — clear cells back to free space. You can also erase with any tool by
  right-clicking or holding **Shift** while dragging.
- **Rectangle** — drag to fill a filled block between two corners.
- **Line** — drag to draw a straight line of cells between two points.

**Terrain palette.** Every map has two built-in terrain types — **Free** (id 0) and
**Obstacle** (id 1). You can add your own custom terrains, recolour any swatch by clicking it,
and remove a terrain (its cells revert to free). The selected terrain is what the paint,
rectangle, and line tools lay down.

**Canvas controls.** Resize the grid to any width and height, zoom in and out, and *fit to
screen* to frame the whole map. An **undo** history lets you step back through edits.

**Import.** Load an existing map either by choosing a `.map`/`.txt` file or by pasting its
text. The parser reads the Moving AI header (`type octile` / `height` / `width` / `map`),
maps the passable characters `.`, `G`, and `S` to free space, matches any recognised terrain
characters to your palette, and treats any other character as an obstacle.

**Export.** Save your map as a `.map` file — set the filename, download it, or copy the text
straight to your clipboard. You can also export a **PNG preview** of the grid for slides and
figures.

**Theme & shortcuts.** Toggle between light and dark themes, and switch tools quickly with
keyboard shortcuts.

## The Moving AI `.map` format

For reference, a Moving AI octile map is a small text file: a header followed by the grid,
where `.` is passable and `@`/`T` are blocked. For example:

```
type octile
height 4
width 8
map
........
..@@....
..@@....
........
```

This is the format used by the standard MAPF benchmark sets, so anything you export here can
be fed directly into common MAPF solvers and benchmark harnesses.
