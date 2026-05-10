# Sea Monster Crowdfunding - Web102 Prework

Submitted by: **Your Name Here**

**Sea Monster Crowdfunding** is a website for the company Sea Monster Crowdfunding that displays information about the games they have funded. The site provides users with comprehensive statistics, game filtering options, search functionality, and smooth navigation to explore the company's crowdfunded game portfolio.

Time spent: **X** hours spent in total

## Required Features

The following **required** functionality is completed:

* [x] The introduction section explains the background of the company and how many games remain unfunded.
* [x] The Stats section includes information about the total contributions and dollars raised as well as the top two most funded games.
* [x] The Our Games section initially displays all games funded by Sea Monster Crowdfunding
* [x] The Our Games section has three buttons that allow the user to display only unfunded games, only funded games, or all games.

## Bonus Features

The following **bonus** features are implemented:

* [x] **Search Functionality** - Users can search for games by name in real-time with a search bar
* [x] **Smooth Scroll Navigation** - Navigation menu in the header allows quick jumps to different sections (Welcome, Stats, Games)
* [x] **Enhanced Visual Design** - Modern gradient backgrounds, improved color scheme, smooth animations, and hover effects
* [x] **Improved UI/UX** - Better typography, shadows, rounded corners, and responsive card animations

## Project Features

### Core Functionality

- **Game Display**: All games are displayed as cards with image, name, description, and backer count
* **Statistics Dashboard**: Shows total contributions, total raised amount, total number of games, and top 2 funded games
* **Filter Options**: Users can toggle between viewing all games, funded only, or unfunded only
* **Dynamic Content**: Uses JavaScript to manipulate the DOM and display data from JSON

### Bonus Enhancements

- **Search Bar**: Real-time game search filtering (case-insensitive)
* **Navigation Menu**: Quick navigation links in the header with smooth scrolling
* **Modern Design**: Gradient backgrounds, animations on hover, floating logo effect
* **Responsive Layout**: Flexbox layouts for responsive card grids

## Technologies Used

* **HTML5** - Semantic markup and structure
* **CSS3** - Gradient backgrounds, flexbox, animations, transitions
* **JavaScript (ES6+)** - Import/export modules, arrow functions, array methods (map, filter, reduce), event listeners
* **DOM Manipulation** - Creating and modifying HTML elements dynamically

## How to Run

1. Open `index.html` in a web browser
2. The site will automatically load all game data from `games.js`
3. Use the buttons to filter games or the search bar to find specific games
4. Click navigation links in the header to smoothly jump to sections

## File Structure

```
web102_prework/
├── index.html          # Main HTML file with page structure
├── index.js            # JavaScript file with all functionality
├── style.css           # CSS styling and animations
├── games.js            # Game data in JSON format
├── package.json        # Project metadata
├── README.md           # This file
└── assets/             # Directory containing game images
    ├── tentacles.png
    ├── heroes_of_mythic_americas.png
    ├── cube_monster.png
    ├── zoo_tycoon.png
    ├── deity_tarot.png
    ├── camouflage.png
    └── beep_bapp_boom.png
```

## Video Walkthrough

Here's a walkthrough of implemented features:

<img src='http://i.imgur.com/link/to/your/gif/file.gif' title='Video Walkthrough' width='' alt='Video Walkthrough' />

<!-- Add your GIF/Video link above -->
GIF created with [ScreenToGif](https://www.screentogif.com/) or [Kap](https://getkap.co/)

## Key Code Snippets

### Search Functionality

```javascript
function searchGames(query) {
    deleteChildElements(gamesContainer);
    const searchResults = GAMES_JSON.filter((game) => 
        game.name.toLowerCase().includes(query.toLowerCase())
    );
    if (searchResults.length === 0) {
        // Show "no results" message
    } else {
        addGamesToPage(searchResults);
    }
}
```

### Filter & Display Games

```javascript
function filterUnfundedOnly() {
    deleteChildElements(gamesContainer);
    const unfundedGames = GAMES_JSON.filter((game) => game.pledged < game.goal);
    addGamesToPage(unfundedGames);
}
```

## Notes

* The project uses ES6 modules to import game data
* All styling uses CSS gradients and animations for a modern look
* The search functionality is case-insensitive for better user experience
* Navigation uses smooth scroll behavior for a polished feel

## License

    Copyright 2026 Sea Monster Crowdfunding

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
