---
title: "Do somthing on the second render? NO!"
date: 2022-08-02T22:35:40+10:00
tags: ["TIL"]
categories: ["TIL"]
---

If something is expected to run on the second render when a dependency is changed in `useEffect`. It's probably wrong!

Instead, try to move `useEffect` to lower level, and when the dependency is ready, `useEffect` will run something on it's first render.
