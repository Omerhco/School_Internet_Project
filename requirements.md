# Personal Internet Project \- Omer Cohen

## What Is This App?

The website is a portfolio for my brother who is a student in Thelma Yellin studying visual art.  
The website includes his most notable videos, animations, photos, drawings and paintings.  
Its target audience is anyone who is interested in his work and/or would like to see it all in one place.

---

## Technologies Used

| Technology | Role |
| :---- | :---- |
| HTML5 | Page structure and content |
| CSS3 | Visual styling and layout |
| JavaScript (vanilla) | Client-side interactivity and data fetching |
| C\# with .NET Minimal API | Web server and API endpoints |

**No frameworks are used — on either the client or the server.** There is no React, Vue, Angular, Bootstrap, jQuery, or any other library. The C\# backend is equally bare: no Entity Framework, no MVC, no Razor Pages — just a single file with route handlers.

---

## Graphic Design 

The website has a clean white design with black text and a black footer at the bottom.

---

## Pages and What They Do

### Home (`index.html`)

The landing page. It orients the visitor and tells them how to use the site.

- Showcases a notable painting, and the website name when entering the website.  
- Displays a list with the website’s pages and their descriptions next to an image.  
- When hovering over different parts of the list, the image changes to represent the page that is being hovered over, and the text underneath the image changes accordingly.  
- When clicking the different parts of the list, you get taken to the corresponding page.

---

### About (`about.html`)

Explains how the site itself was built, and for what purposes.

- Describes Ilan’s work in a few short sentences.  
- Describes the purpose of the website and why it was created.  
- Displays the HTML, JavaScript, CSS and C\# that were used to create the website, in simple terms.  
- Includes a comment section to comment about the website and the various projects. the comments can be seen across all devices, as long as the server doesn’t restart.

---

### Photography (`photos.html`)

A page displaying notable photography projects.

- Includes a grid of one notable photograph from each project, when clicking on that photograph the entire project will be displayed.  
- Each photograph includes a name and a date.

---

### Paintings and drawings (`paintings.html`)

A page displaying notable paintings and drawings.

- Displays all his notable paintings and drawings, stacked vertically so that the viewed painting/drawing takes all or almost all of the screen.  
- Each painting includes a name, date, original aspect ratio and materials.

---

### Videos and animations (`videos.html`)

A page displaying notable videos and animations.

- Displays a grid of all videos and animation.  
- Each video/animation has some background information, as well as a date.  
- Includes an embedded media player at the bottom of the page.  
- When clicking on a video, the page will scroll down to the media player and the video will be shown.

---

## Behaviour That Applies to Every Page

### Shared navigation header

Every page displays the same header at the top, containing:

- The site logo. The logo is clickable and leads to the home page.  
- A navigation bar with five links: Home, About, Photography, Paintings & drawings, Video art & Animations.  
- The header is **not duplicated** in each HTML file. It is stored in a single separate file and loaded dynamically by JavaScript on every page.

### Shared footer

Every page contains the same footer at the bottom with contact information.  
The footer is **not duplicated** in each HTML file. It is stored in a single separate file and loaded dynamically by JavaScript on every page.

---

## Data and State

- **Comment Section content:** a single string on the server that grows with each POST. It is held in memory only — it resets when the server restarts. There is no database.

---

## 

| Interaction | Where | Result |
| :---- | :---- | :---- |
| Click a nav link | Any page | Navigates to that page |
| Click the logo | Any page | Sends user to home page |
| Click Video thumbnail | Video art & Animations page | Scrolls down to media player and shows video |
| Click Photo | Photography page | Opens up the full project with all the photos  |
| Type a comment and click “Send” | About page | Comment is submitted to server, page reloads and comment appears |
| Refresh the page | About page | Comment section reloads with latest comments |

---

## What the App Does NOT Do

- No user accounts or login.  
- No persistent storage — messages are lost on server restart.  
- No client-side routing or single-page app behaviour.  
- No form validation — empty messages are silently ignored by the server.  
- No error messages shown to the user when API calls fail (elements show a fallback text string).  
- No admin interface.  
- No search.

