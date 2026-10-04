# Responsive Course Cards

## Introduction
A desktop-style course-card interface converted into a **mobile-first responsive component** using only HTML and CSS. On phones the cards stack one below another, and on screens 768px and wider they sit side by side in a row.

No Bootstrap, Tailwind CSS or any other UI framework is used.

**Live demo:** `https://YOUR-USERNAME.github.io/responsive-course-cards/` (replace with your GitHub Pages link)

## Features
- Three course cards: AIML, CSE and IT, each with an **Enroll** button
- **Mobile-first** design: cards stack in a column on small screens
- **Media query** at 768px moves the cards into one row on larger screens
- Equal-width cards on desktop using `flex: 1`
- Hover effect on cards and buttons
- No horizontal scrolling at any tested width

## Technologies Used
- HTML5
- CSS3 (Flexbox, media queries, transitions)

## Project Structure
```
responsive-course-cards/
├── index.html      # Page structure: heading and three cards
├── style.css       # Mobile-first styles and the desktop media query
└── README.md       # Project documentation
```

## How It Works
**Mobile first:** the cards are placed in a Flexbox column.
```css
.course-container {
    display: flex;
    flex-direction: column;
    gap: 20px;
}
```

**Desktop:** a media query changes the column into a row when the screen is 768px or wider.
```css
@media (min-width: 768px) {
    .course-container {
        flex-direction: row;
    }
    .card {
        flex: 1;
    }
}
```

## Testing
Tested in Chrome Developer Tools (Inspect → device icon):

| Screen width | Layout | Horizontal scroll |
| --- | --- | --- |
| 320px | Column (stacked) | None |
| 375px | Column (stacked) | None |
| 425px | Column (stacked) | None |
| 768px | Row (side by side) | None |
| 1024px | Row (side by side) | None |
| 1440px | Row (side by side) | None |

## Installation
1. Download or clone this repository.
2. Open the project folder.
3. Open `index.html` in a browser.

## Usage
1. Open `index.html` in Chrome or Edge.
2. Resize the window, or use Inspect → device icon, to see the layout change.
3. Below 768px the cards stack; from 768px they appear in a row.

## Future Enhancements
- Add more courses
- Course detail page for each card
- Working enrollment form
- Dark mode
