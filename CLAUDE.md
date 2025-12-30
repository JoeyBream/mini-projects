# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a collection of 11 standalone mini web applications built with vanilla HTML, CSS, and JavaScript. Each project is completely self-contained in its own directory with a single `index.html` file containing all HTML structure, CSS styles, and JavaScript code inline.

## Architecture

**Self-Contained Structure**: Each project (01-11) follows this pattern:
- Single `index.html` file with embedded `<style>` and `<script>` tags
- No external dependencies, libraries, or frameworks
- No build process or compilation required
- All state management uses browser APIs (localStorage, canvas API, etc.)

**Root Homepage**: `index.html` at the repository root serves as a gallery/launcher that links to all 11 projects.

## Running Projects

Open any project directly in a web browser:
```bash
# Open a specific project
open 01-snake-game/index.html

# Open the homepage gallery
open index.html
```

No build, install, or server commands needed. All projects run entirely client-side.

## Project List

1. **Snake Game** - Canvas-based game using `setInterval` for game loop, localStorage for high scores
2. **Todo List** - CRUD operations with localStorage persistence and filter states
3. **Weather Dashboard** - Demo mode with hardcoded data (no actual API calls)
4. **Password Generator** - Client-side cryptographic random generation
5. **Expense Tracker** - Financial tracking with income/expense categorization
6. **Pomodoro Timer** - Interval timer with session statistics
7. **Quiz App** - Multiple choice quiz with scoring system
8. **Drawing App** - HTML5 canvas drawing with touch support and PNG export
9. **Music Player** - HTML5 audio player interface (requires external audio files)
10. **Chat Bot** - Pattern-matching conversational interface
11. **Data Table** - Sortable, filterable data table with pagination

## Common Patterns

**State Persistence**: Most apps use `localStorage.getItem()` and `localStorage.setItem()` for data persistence across sessions.

**Event Handling**: All interactivity uses inline event handlers (`onclick`, `onchange`) or `addEventListener` within `<script>` tags.

**Styling**: Consistent gradient backgrounds (`linear-gradient(135deg, #667eea 0%, #764ba2 100%)` is the primary theme), white card containers with `border-radius: 15px`, and `box-shadow` for depth.

**No Modularization**: Code is intentionally not split into separate files. When modifying projects, maintain the single-file structure.

## Modifying Projects

When editing any project:
- Keep all code within the single `index.html` file
- Maintain the inline `<style>` and `<script>` structure
- Test by simply refreshing the browser (no build step)
- Preserve localStorage keys to avoid breaking existing user data
- Ensure responsive design is maintained (most use flexbox/grid)

## Adding New Projects

To add a new project:
1. Create a new directory (e.g., `12-project-name`)
2. Add a single `index.html` file following the existing pattern
3. Update the root `index.html` to include a new project card linking to it
4. Increment the project count in the stats section
5. Update README.md with the new project description
