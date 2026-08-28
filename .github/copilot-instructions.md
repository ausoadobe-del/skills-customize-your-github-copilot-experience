# Copilot Instructions

## Project Overview

This project is an educational website for sharing homework assignments and coding exercises with students. Students can browse, view, and download assignments directly from the portal.

The repository contains a static Computer Science course portal for Mergington High School. The site is built with plain HTML, CSS, and browser JavaScript. Course and assignment metadata lives in `config.json`; assignment content and starter files live under `assignments/`.

## Project Structure

- `assignments/`: Each homework assignment is stored in its own subfolder with a consistent structure.
- `templates/`: Reusable templates for new content.
- `assets/`: Website assets, including CSS, JavaScript, and images.
- `index.html`: The main static portal page for browsing and viewing assignments.
- `config.json`: Course and assignment configuration used to dynamically generate assignment lists and details.

## General Guidelines

- Keep changes focused and preserve the existing structure and visual language.
- Maintain consistent styling across all pages.
- Keep file and folder names descriptive and organized.
- Use vanilla HTML, CSS, and JavaScript. Do not add a framework or build step unless explicitly requested.
- Preserve the relative paths used by the static site. The site is expected to work when served from the repository root.
- Prefer clear, small changes over broad refactors.
- Use double quotes in JavaScript where that matches the surrounding code; preserve existing formatting in untouched areas.
- Do not add dependencies for behavior that can be implemented with the browser APIs already in use.

## Site Conventions

- Update course or assignment metadata in `config.json`, not by hard-coding it into page markup.
- Keep homepage behavior in `assets/js/script.js` and assignment-detail behavior in `assets/js/assignment.js`.
- Keep shared styling in `assets/css/styles.css`.
- Assignment links use the `id` query parameter and target `assets/pages/assignment.html`.
- New assignments should follow the existing layout: an assignment directory containing `README.md`, with optional starter files or datasets referenced by `config.json` under `attachments`.
- Use accessible HTML: meaningful headings, descriptive image `alt` text, valid links, and controls that are keyboard usable.
- When rendering user- or file-sourced text into the DOM, avoid unsafe HTML interpolation; use `textContent` or sanitize trusted markup appropriately.

## Educational Standards

When generating assignments, README files, examples, or other educational content:

- Keep the content learning-focused, with clear learning objectives and an appropriate difficulty level.
- Use clear, encouraging, student-friendly language.
- Make requirements and expected outcomes concrete, testable, and easy for students to follow.

When asked to explain this project, briefly describe it as a student-facing portal for browsing, viewing, and downloading homework assignments and coding exercises, then mention its static HTML/CSS/JavaScript implementation and configuration-driven assignment catalog.

## Validation

- Serve the repository root with a local static server before testing fetch-based behavior, for example: `python3 -m http.server 8000`.
- Check the homepage and an assignment detail page in a browser, including assignment links and attachment downloads.
- For JavaScript-only changes, run a syntax check such as `node --check assets/js/script.js` or `node --check assets/js/assignment.js` for the touched file.
- For Python assignment changes, run the relevant starter file with Python 3 and verify the examples in its README.
- Do not commit generated files, editor state, or unrelated changes.
