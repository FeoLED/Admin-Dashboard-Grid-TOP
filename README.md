# Admin Dashboard (A CSS Grid Exploration)

A responsive admin dashboard mockup built as a solution for The Odin Project's curriculum. The primary goal was to deepen my understanding of CSS Grid layout.

[Live Demo](https://feoled.github.io/Admin-Dashboard-Grid-TOP/)

[Full View Screenshot](assets/images/full-screenshot.png) 

[Shrunk View Screenshot](assets/images/shrunk-screenshot.png)

## Features

-   Fixed sidebar navigation
-   Header with search bar, user info, and buttons
-   Main content area with:
    -   A responsive grid of project cards
    -   An announcements section
    -   A trending users section
    
## Tech Stack & Credits

-   **HTML5**
-   **CSS3:** Grid, Flexbox, Custom Properties
-   **Fonts:** [Fragment Mono](https://fonts.bunny.net/) from Bunny Fonts (GDPR-friendly!)
-   **Icons:** Font Awesome, Material Design Icons
-   **User Avatars:** Generated using [Perchance AI Icon Generator](https://perchance.org/ai-icon-generator)

## The Build: Embracing CSS Grid

This project was a deliberate dive into CSS Grid, moving away from my comfort zone with Flexbox. The process was challenging—I rewrote the stylesheet multiple times!

My breakthrough came from a hybrid approach:
-   **Grid for Macro-Layout:** I used CSS Grid to define the high-level page structure (sidebar, header, main content). This provided a robust foundation without needing complex media queries for basic responsiveness.
-   **Flexbox for Micro-Layout:** Inside each grid area, I often used Flexbox for aligning content, as it felt more intuitive for component-level spacing.

### Key Code Snippet: The Main Grid Container

```css
.container {
    display: grid;
    grid-template-columns: 160px repeat(4, 1fr); /* First column fixed for sidebar */
    grid-template-rows: auto repeat(4, 1fr);
}
```

### Key Code Snippet: Responsive Project Cards

The auto-fit and minmax() functions were crucial for creating the responsive card layout.
css

```css
.cardContainer {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    grid-auto-rows: 200px;
    gap: 4px;
}
```

## Design Choices

I opted for a light, pastel-like color scheme inspired by the project example, a departure from my usual dark themes.
-  **Sidebar:** White and cyan for clarity.
-  **Main Area:** A soft lilac background.
-  **Cards:** Project cards in green, with announcements/trending in bisque (a soft off-white).
-  **Details:** Subtle border-radius, hover states on interactive elements, and a coral/salmón border on the search bar for a pop of contrast.

## What I Learned

This project solidified my practical understanding of CSS Grid. I learned to appreciate its power for two-dimensional layout and how it can work in tandem with Flexbox to create complex, responsive designs efficiently.
