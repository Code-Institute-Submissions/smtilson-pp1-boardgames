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
The purpose of the site is to inform people new to the boardgaming hobby about different games they may not be aware of. Not every game suits every person/group of players, and the site aims to help people make informed choices. Hundreds of new boardgames are released every year. Providing information about games for different audiences is a valuable endeavor as the hobby can be expensive and time consuming.

### User Demographics
The expected user is someone who has some experience with hobby boardgames and cardgames. They are interested in trying new games and determining what they do and do not like.

### Wireframes
After the initial idea and brainstorming, I used Balsamiq to mock up some initial wireframes. While I did not stick completely to the wireframes, they were helpful in terms of visualizing the kind of design I was interested in.

#### Site Plan
Here is the initial siteplan:
![Initial site plan wireframe](/assets/images/wireframes/wireframe-site-plan.png)
- I decided to not do a different page for each game, and to just put info on all of the games from that category on the same page. My mentor supported this idea.
- I used different games than those listed here as they were place holders.

#### Content pages
I then designed the pages that would contain the majority of the content of the site.
Desktop:
![Desktop content page wireframe](/assets/images/wireframes/wireframe-desktop-content-page.png)

Mobile:
![mobile content page wireframe](/assets/images/wireframes/wireframe-mobile-content-page.png)

For desktop, I changed the styling to columns from rows as I felt it looked nicer. This also increased the continuity of design between mobile and desktop view. I used rounded squares because I also liked their appearance. It was also a nice compromise between squares of the desktop design plan and the mobile design plan. I had intially wanted the different containers to overlap, but found that it did not look as clean in practice as I had envisioned.

#### Landing page
Desktop:
![Desktop landing page](/assets/images/wireframes/wireframe-desktop-landing-page.png)

Mobile:
![Mobile landing page](/assets/images/wireframes/wireframe-mobile-landing-page.png)

I kept some of the ideas present and elaborated on them.

### Future directions
The site does not have information on that many games, but the design is such that I can extend it to include details of many other games.

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
I used dev tools in chrome to test the responsiveness of the site. I also used <a href="https://ui.dev/amiresponsive" target="_blank">AmIResponsive</a> to help me determine how things would look on different sites. I primarily checked on screen widths of 320px, 375px, 425px, 768px, 916px (my laptop), and 1024px. I had to also adjust the height manually, as changing the width did not seem to always impact the height in chrome dev tools. Because of this, I manually entered 375×667, 414×736, 360×800, 390×844 (these were suggested by <a href="https://testsigma.com/blog/common-screen-resolutions/" target="_blank">TestSigma</a>).

On larger screens, I had planned to have the main content of the pages scroll underneath the logo, navbar, and social links while appearing above the rest of the header and footer. This caused positioning problems when transitioning between screens. The reason for this is that dev tools can not take into account the amount of space 

### Lighthouse tool
I used the Lighthouse extension to test my website. My initial score was:
![Lighthouse results index initial](/assets/images/screenshots/lighthouse-test-results-index-initial.png)

My poor performance was likely due to the images not being compressed. [Daisy](#daisy-mentor), a mentor, on slack suggested a way to address this.

After converting the hero images to webp format and compressing them I received the following score:
![Lightouse results final](/assets/images/screenshots/lighthouse-test-results-index-final.png)

Here is the lighthouse test results for 2-player.html, as it is fairly representative of the other pages:
![lighthouse results 2-player](/assets/images/screenshots/Lighthouse-test-results-2-player.png)

### Validation
Each html file was validated using <a href="https://validator.w3.org/" target="_blank">W3html validator</a>. <a name="label-div">I had 1 error</a>. I had wrapped one of the divs in the header in the label which controls the dropdown nav in mobile. This is frowned upon, so I removed it. My reason for putting the div inside the label element was so that the whole header would work as a toggle for the navbar dropdown menu. I also had warnings regarding the use of aria labels on the landing page. I ignored these as I was following the example set by the Love Running Walkthrough project, to add aria labels to images added as background through css as no alt-tag is present when images are added this way.

The CSS file was validated using <a href="https://jigsaw.w3.org/css-validator/" target="_blank">W3 Jigsaw CSS validator</a>. There were no errors. There were warnings regarding the font imports from google, which are unavoidable.

### Bugs

- Bug: I had 1 [error](#label-div) in my html according to the validator. I had placed a div element inside of a label element.
   
   - Fix: I removed the div from inside the label. This did require repositioning the burger menu icon.

- Bug: My form did not submit correctly (this was pointed out to me by [Daisy](#daisy-mentor), a mentor on slack).
   
   - Fix: This was fixed by changing the type of the input from button to sunmit.

- Bug: The landing page, the hover border on links caused them to visually move.

   - Fix: I fixed this by adding a margin with negative width equal to the width of the border being added. I learned this from reference [SO: hover bug](#so-hover-reference).

- Bug: The border on active links in the navbar caused a shift in position of navbar elements.
    
   - Fix: I fixed this by adding some negative space and changing when the extra padding was applied. Now the padding is applied to all anchor elements, not just the ones with the active class. However, this still seems to happen with the mailing list page.

- Bug: On some larger screens, clicking on the mailing list navbar link, or on another navbar link from the mailing list page causes a shift of the navbar. I could not remove this. It also appeared intermittently and so is not clear if it was an actual bug or an artifact of something in how dev tools was displaying things. It is a minor visual bug.

   - Attempted fixes: I tried adding negative padding to various navbar elements to account for padding that I thought was causing the issue.

- Bug: Headers on content pages were not regularly spaced.

   - Fix: Flex boxes were used. To make the style consistent across screen sizes, I used media queries.

<a name="tutor-support-bug"></a>
- Bug: Header and footer were cutting off part of the main element. I had styled it so that the main element scrolled beneath the navbar and social media links. This made it very hard to make it look good across different devices as I had to fiddle with the margin-top of main as well as the height of certain elements.

   - Fix: I removed the fancy scrolling of the main element. Now the footer cuts off some content, which is expected behavior. This was suggested by Tutor support. So ultimately, better design was the solution. Prior to this, there were several commits involving positioning, margins, and sizing of the header, footer, main, the hero3 div, and other elements on the landing page that were solely related to this issue.

- Bug: A strong element caused text to be pushed to the next line in the Earthborne Rangers section.

   - Fix: Instead, I used a span element that was specifically styled to bold an element and had display:contents as a rule. This was suggested by [SO strong tags new line](#so-strong-new-line).

- Bug: I was using logos for the external links but they were not responsive and very difficult.

   - Fix: I decided to use text with abbreviations for the website or channel for those external links.

- Bug: After removing h3 subtitle element from header, the underline underneath logo was cut off.

   - Fix: I removed the margin-bottom rule on the id logo

- Bug: On the landing page, the elements with text have darker background than the div.

   - Fix: What was happening was that two backgrounds where adding to each other so I fixed this by making the background of child elements transparent.

- Bug: There was a black line between main and header, underneath the bottom border from the header element.

   - Fix: I removed this by changing the background-color of the body and modifying background-color inheritance so that by default everything inherits background-color from its parent.

- Bug: The Onitama image was very stretched and weird.

   - Fix: This is due to the box for the game being a different shape. To address this I got the image from a different source and cropped it to have a more workable aspect ratio.
[return to Table of Contents](#toc)

## Deployment <a name="deployment"></a>
To deploy the project follow the following steps.

1. Copy/Clone the <a href="https://github.com/smtilson/pp1-boardgames" target="_blank">repository</a> on github.

2. Go to your copy of the repository on your github page (likely `https://github.com/YOUR-USERNAME-HERE/pp1-boardgames`)

3. Open settings tab on top right of page

4. Click on pages link on the left sidebar in the "Code and Automation" section.

5. Set "Source" to "Deploy from branch", select "main" branch, and set folder to /(root) under "Build and Deployment". Then click Save.

6. Return to the "Code" tab and wait for site to build. Try doing a hard refresh.

7. On the right hand side under "Deployments", click on "github-pages".

8. Click on the link which matches `https://USERNAME.github.io/REPO-NAME/` to view the deployed site.

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
I received a lot of support from my mentor. This took the form of helpful tips, explaining what to focus on in terms of prioritization, and which design decisions were relevant for the assessment criteria. He suggested having only the single h element on my landing page. He also provided me with sample readmes from previous students, these were vary helpful. For example, they made me aware of the lighthouse tool.

#### Tutor Support
I had a great deal of difficulty addressing certain responsiveness issues. Things kept on displaying differently depending on the zoom parameter on dev tools. In fact, what was happening is that the width was staying fixed but changing the zoom parameter impacted the height in pixels, and this is what was causing the change. This issue made predicting the appearance of my site very difficult, as you can not account for how much of the screen the operating system and the browser will take up (yet?). The Tutor advised that I opt for a more robust design choice to address the ambiguity, which was to remove a certain feature and opt for something simpler. As described in [this bug](#tutor-support-bug)

#### Feedback on Slack
- <a name="daisy-mentor">Daisy_mentor</a>, a mentor on slack
She pointed out to me that it would be good to decrease the size of the h1 header element on screens smaller than 360px. She also pointed out to me that my form button wasn't working. These things have been corrected for.

- Fellow students
In this <a href="https://code-institute-room.slack.com/archives/C06N62J3TKQ/p1711707098566759" target="_blank">thread</a>, some of my fellow students pointed out how I could use dev tools properly. Specifically, to help with positioning of elements.

#### StackOverflow
- <a href="https://stackoverflow.com/questions/44696874/forcing-a-h1-to-stay-in-1-line" target="_blank">Stackoverflow: single line</a>: keeping logo in one line.

- <a href="https://stackoverflow.com/questions/67252231/what-is-the-purpose-of-this-purple-dashed-line-area" target="_blank">Stackoverflow: purple dashed line</a> to explain purple dashed area in chrome dev tools

- <a href="https://stackoverflow.com/questions/25706012/how-do-i-prevent-auto-generated-links-in-the-github-wiki" target="_blank">Stackoverflow: prevent auto generated links in readme</a> to make urls not automatically links for this readme file
<a name="so-hover-reference"></a>

- <a href="https://stackoverflow.com/questions/9612758/add-a-css-border-on-hover-without-moving-the-element" target="_blank">Stackoverflow: hover border without moving the element</a> to make hover borders that don't move the element
<a name="so-strong-new-line"></a>

- <a href="https://stackoverflow.com/questions/18419254/strong-tags-new-line" target="_blank">Stackoverflow: strong tags new line</a> to prevent bolding some text from starting a new line

- <a href="https://stackoverflow.com/questions/41604263/how-do-i-display-local-image-in-markdown">Stackoverflow: display local image in markdown</a>

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