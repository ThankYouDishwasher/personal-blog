---
title: "TS files may reference JS files complied"
date: 2022-08-12T21:39:46+10:00
tags: ["Mistakes", "Testing"]
categories: ["TIL"]
---

This is a case happening in unit testing. Any changes and console.log couldn't be reflected in the testing log. It finally turned out that the testing was referencing a JS file complied as the route I imported didn't have a suffix, and by default, the JS files will be consumed.

In order to reduce the noises caused by JS files, you can run `yarn clean`
