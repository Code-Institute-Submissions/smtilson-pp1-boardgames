# Title <a name="title"></a>
### Sean Recommends
#### Boardgames for the Newly Converted
<a href="https://smtilson.github.io/pp1-boardgames/index.html" target="_blank">Sean Recommends Github pages link</a>

## Table of contents <a name="toc"></a>

- [Title](#title)
- [Introduction](#intro)
- [Design Planes](#planes)
- [Features](#features)
- [Testing](#testing)
- [Deployment](#deployment)
- [Credits and Outside Sources](#credits)

## Introduction <a name="intro"></a>

![Landing page responsive screenshot](/assets/images/screenshots/landing-page-screenshot.png)

### Project Description
This site is a collection of recommendations for different boardgames and cardgames for people new to the hobby. There are pages devoted to 2 player games, games for new players, and the authors personal favorite games. Information on specific games is accompanied by links to relevant external sites. 

### Project Purpose
The purpose of the site is to inform people new to the hobby about different games they may not be aware of. Not every game suits every person/group of players, and the site aims to help people make informed choices. Hundreds of new boardgames are released every year as the hobby and market grows. Providing information about games for different audiences is a valuable endeavor as the hobby can be expensive and time consuming.

### User Demographics
The expected user is someone who has some experience with hobby boardgames and cardgames. They are interested in trying new games and determining what they do and do not like.

### Design Process and Wireframing
After the initial idea and brainstorming, I used Balsamiq to mock up some initial wireframes.

### Future directions
The site does not have information on that many games, but the design is such that it can be extended to include details of many other games.



[return to Table of Contents](#toc)

## Features <a name="features"></a>
#### Navbar
There is a navbar at the top of the page. For screens of width less than 768px, the navbar is hidden. 

![mobile navbar hidden](/assets/images/screenshots/mobile-navbar-hidden.png)

Clicking on the burger icon will toggle the navbar, which drops down below the header.

![mobile navbar displayed](/assets/images/screenshots/mobile-navbar-displayed.png)

On larger screens, it displays horizontally beneath the header. Also, the current page is highlighted and hovering over an item will cause it to be underlined.

![tablet navbar](/assets/images/screenshots/tablet-navbar.png)

#### Content pages
There are 3 pages of content. They each relate to a different (but potentially overlapping) category of games: games for 2 players, games for new players, and my favorite games. Each page contains entries on multiple games. 

![content page for two player games](/assets/images/screenshots/content-page-screenshot.png)

Each entry contains an image of the boardgame cover, a brief blurb about the game from the author, and links to external sites regarding the game.

#### Links to external resources
These external links are to the games page on BGG (the definitive online resource for boardgames), and reviews on youtube (when available). The primary reviews are to the YouTube channels Shut Up and Sit Down, and the Dice Tower. These are the two most influential review channels on YouTube.

![external links to BGG, SUSD, and DT](/assets/images/screenshots/external-links.png)

#### Footer
The footer contains links to social media sites. These open in new tabs and only go to the main page of the respective social media site. The links are social media icons. They are displayed differently on mobile and desktop screens.

![mobile social media links](/assets/images/screenshots/mobile-social-links.png)

![desktop social media links](/assets/images/screenshots/desktop-social-links.png)

#### Signup form
The signup form "subscribes users to a mailing list". It asks for first name, favorite game, and email address.

![form page on different devices](/assets/images/screenshots/form-page-screenshot.png)

#### Features left to implement
- Pages for other categories of games
- A page of Links to external resources

[return to Table of Contents](#toc)

## Testing <a name="testing"></a>
### Manual Testing
I used dev tools in chrome to test the responsiveness of the site. I also used <a href="https://ui.dev/amiresponsive" target="_blank">AmIResponsive</a> to help me determine how things would look on different sites. I primarily checked on screen widths of 320px, 375px, 425px, 768px, 916px (my laptop), and 1024px. I had to also adjust the height manually, as changing the width did not seem to always impact the height in chrome dev tools. Because of this, I manually entered 375×667, 414×736, 360×800, 390×844 (these were suggested by [TestSigma](https://testsigma.com/blog/common-screen-resolutions/)).

On larger screens, I had planned to have the main content of the pages scroll underneath the logo, navbar, and social links while appearing above the rest of the header and footer. This caused positioning problems when transitioning between screens. The reason for this is that dev tools can not take into account the amount of space 

### Validation
Each html file was validated using <a href="https://validator.w3.org/" target="_blank">W3html validator</a>. I had 1 error. I had wrapped one of the divs in the header in the label which controls the dropdown nav in mobile. This is frowned upon, so I removed it. I did this so that the whole header worked as a toggle for the navbar dropdown menu.

The CSS file was validated using <a href="https://jigsaw.w3.org/css-validator/" target="_blank">W3 Jigsaw CSS validator</a>. There was a minor error which was easily fixed. There were also warnings regarding the font imports from google

### Bugs

[return to Table of Contents](#toc)

## Deployment <a name="deployment"></a>
To deploy the project follow the following steps.

1. Copy/Clone the <a href="https://github.com/smtilson/pp1-boardgames" target="_blank">repository</a> on github.

2. Go to your copy of the repository on your github page (likely https://github.com/YOUR-USERNAME-HERE/pp1-boardgames)

3. Open settings tab on top right of page

4. Click on pages link on the left sidebar in the "Code and Automation" section.

5. Set "Source" to "Deploy from branch", select "main" branch, and set folder to /(root) under "Build and Deployment". Then click Save.

6. Return to the "Code" tab and wait for site to build. Try doing a hard refresh.

7. On the right hand side under "Deployments", click on "github-pages".

8. Click on the link which matches https://USERNAME.github.io/REPO-NAME/ to view the deployed site.

[return to Table of Contents](#toc)

## Credits and Outside sources <a name="credits"></a>

#### Inspiration

-Love Running Walkthrough
This project was influenced by the Love Running walkthrough project. I learned many things there.
In particular
1. CSS for dropdown menu for the navbar
2. header section
3. sticking footer to bottom of page
4. favicon

#### Mentor
I received a lot of support from my mentor. This took the form of helpful tips, explaining what to focus on in terms of prioritization, and which design decisions were relevant for the assessment criteria.

#### Feedback on Slack
- Daisy_mentor
She pointed out to me that it would be good to decrease the size of the h1 header element on screens smaller than 360px. She also pointed out to me that my form button wasn't working. These things have been corrected for.

- Fellow students
In this <a href="https://code-institute-room.slack.com/archives/C06N62J3TKQ/p1711707098566759" target="_blank">thread</a>, some of my fellow students pointed out how I could use dev tools properly. Specifically, to help with positioning of elements.

#### StackOverflow
- <a href="https://stackoverflow.com/questions/44696874/forcing-a-h1-to-stay-in-1-line" target="_blank">Stackoverflow: single line</a>: keeping logo in one line.

- <a href="https://stackoverflow.com/questions/67252231/what-is-the-purpose-of-this-purple-dashed-line-area" target="_blank">Stackoverflow: purple dashed line</a> to explain purple dashed area in chrome dev tools

#### Images
Images for game covers:
1. <a href="https://boardgamegeek.com/boardgame/50/lost-cities" target="_blank">Lost cities on BGG</a>
2. <a href="https://boardgamegeek.com/boardgame/221965/fox-forest" target="_blank">Fox in the Forest on BGG</a>
3. <a href="https://boardgamegeek.com/boardgame/173346/7-wonders-duel" target="_blank">7 Wonders Duel on BGG</a>
4. <a href="https://boardgamegeek.com/boardgame/205637/arkham-horror-card-game" target="_blank">Arkham Horror: the Card Game on BGG</a>
5. <a href="https://boardgamegeek.com/boardgame/342900/earthborne-rangers" target="_blank">Earthborne Rangers on BGG</a>
6. <a href="https://boardgamegeek.com/boardgame/366013/heat-pedal-metal" target="_blank">Heat on BGG</a>
7. <a href="https://boardgamegeek.com/boardgame/209685/century-spice-road" target="_blank">Century: Spice Road on BGG</a>
8. <a href="https://m.media-amazon.com/images/I/51JxHhJQMmL._AC_.jpg" target="_blank">Onitama logo from amazon</a>
9. <a href="https://boardgamegeek.com/boardgame/199561/sagrada" target="_blank">Sagrada on BGG</a>

#### Assorted external links
- <a href="https://ui.dev/amiresponsive" target="_blank">AmIResponsive</a> to generate images of my page on different screen sizes.

- <a href="https://favicon.io/favicon-converter/" target="_blank">online favicon generator</a> to generate a favicon from an image file

- <a href="https://stock.adobe.com/de/images/colorful-board-game-vector-template/222236135" target="_blank">stockimage photo</a> for favicon

- <a href="https://colorhunt.co/palette/22283131363f76abaeeeeeee" target="_blank">Color Hunt</a> to find a color palette

- <a href="https://www.eddymens.com/blog/how-to-make-a-markdown-link-open-in-another-tab#:~:text=You%20just%20add%20the%20target,in%20a%20different%20browser%20tab" target="_blank">Random page</a> for the code to open links in markdown in a new page

[return to Table of Contents](#toc)