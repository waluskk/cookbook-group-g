# Visit page: https://lukaszchomatek.github.io/cookbook-base/

# Student Cookbook — Collaborative GitHub Pages Application

## Overview
The *Student Cookbook* project is a simple web application designed to demonstrate teamwork and collaboration using Git, GitHub, and GitHub Pages.  
The application provides a minimal but functional front end built with **Vue.js** (loaded via CDN). It dynamically lists all recipe files from the GitHub repository and renders their Markdown content into HTML.

## How the Application Works
1. The application consists of a single `index.html` file placed in the repository root.  
2. It loads **Vue 3**, **Marked**, and **DOMPurify** directly from CDNs — no build tools or package managers are required.  
3. When the page is opened (e.g., `https://lukaszchomatek.github.io/cookbook-base/`), Vue fetches a list of `.md` files from the `/recipes/` folder using the **GitHub Contents API**.  
4. The list of recipes is displayed in the sidebar.  
5. When a user clicks a recipe name, the Markdown file is fetched from the same GitHub Pages domain (e.g. `https://lukaszchomatek.github.io/cookbook-base/recipes/Tea.md`) and rendered in the main panel.  
6. Markdown is converted to safe HTML using **Marked** and sanitized with **DOMPurify** to prevent security issues.  

## Project Structure
```
cookbook-base/
│
├── index.html          # Main application file (Vue + Marked + DOMPurify)
├── recipes/            # Folder containing Markdown recipes
│   ├── Tea.md
│   ├── Pasta.md
│   └── Sandwich.md
└── README.md           # Instructions for contributors
```

Each `.md` file should include a short recipe, for example:

```markdown
# Tea

## Ingredients
- Water  
- Tea bag  
- Lemon  

## Steps
1. Boil water.  
2. Pour over tea bag.  
3. Add lemon and enjoy.
```
