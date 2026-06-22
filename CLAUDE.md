# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

A single-file static web app (`index.html`) — a spinning wheel for picking a lunch restaurant near N26's Berlin HQ. No build step, no dependencies, no server required. Open `index.html` directly in a browser to run it.

## Adding or changing restaurants

All restaurant data lives in three parallel arrays at the top of the `<script>` block (~line 121):

```js
const options = ["Besh", ...];      // display name (also used in map search queries)
const colors  = ["#7b2ff7", ...];   // wheel segment fill color
const textColors = ["#fff", ...];   // label color — use "#fff" for dark fills, "#000" for light fills
```

Add one entry to each array to add a restaurant. The map links automatically append `' Berlin'` to the name when building the search query, so names should match how the place appears on Google Maps.
