# 🕸️ Spider Surfer Maps

Spider Surfer is a hacked-together, reverse-engineered, physics-patched, DOM-punching PyVis crawler built for visualizing website link structures as interactive node webs.

The goal: map every page, every internal link, and every ghosted reference in a way that's not only functional... but fun to watch explode.

---

## 🤖 What It Does

- Recursively crawls a site
- Normalizes and filters internal vs external links
- Flags phantom nodes and 404s
- Generates a PyVis graph
- Injects JS that lets you click any node and see all inbound/outbound edges live

---

## 🧠 Why It Was Built

Most visualizers are boring. Spider Surfer was built from scratch to look good, act fast, and expose the true lattice structure of a site — including orphaned content, link clusters, and strange SEO behaviors.

---

## 🧪 PyVis Wasn't Made For This

PyVis is great... until you try to do anything interesting. To make Spider Surfer work, we had to:

- Override PyVis’ physics engine post-render
- Inject live JavaScript into the exported HTML
- Patch DOM nodes manually to show edge direction and flow
- Handle graphs PyVis would normally choke on

We don't touch PyVis's source, but we do... coerce it.

---

## 📂 What's In This Folder

### `site_map.html`
> A real-world crawl output from a production scan. Massive node count. Rendered with physics overrides and stabilized post-load.

### `dna_helix.html`
> A demo structure meant to mimic coiled link logic — shows PyVis tolerating layout constraints with fake gravity modeling.

### `exploding_graph.html`
> A visual stress test. This simulates nodes exploding outward from a central hub and demonstrates color-cycling and edge highlighting.

### `orbit_lattice.html`
> Demo of a lattice-style link structure with artificial bidirectionals. Built to show how PyVis can simulate orbit behavior through hacked spring tension and disabled gravity.

---

## 🧪 Developer Notes

We’ll submit an issue (or enhancement request) to the PyVis team showing what’s possible when you break their renderer a little. These examples are intentionally engineered edge cases — useful for pushing the limits of network visualization in client-side HTML.

We’re not saying this is the right way to use PyVis.  
We’re saying it’s the **fun** way.
