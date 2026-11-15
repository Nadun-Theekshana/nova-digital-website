# Nova Digital – Creative Digital Agency Website

A fictional agency website built with HTML5 and CSS3 only (no JavaScript, no frameworks).
Nova Digital is a concept created for portfolio demonstration. The portfolio projects, contact details
and form are demonstration content, not real businesses or working services.

## Folder structure

```
Nova-Digital/
│
├── index.html
├── style.css
├── README.md
└── images/
    ├── hero-image.jpg
    ├── about-image.jpg
    ├── project-restaurant.jpg
    ├── project-portfolio.jpg
    └── project-business.jpg
```

## Run it in Visual Studio Code

1. Unzip the project and open the `Nova-Digital` folder in VS Code (File → Open Folder).
2. Install the **Live Server** extension (by Ritwick Dey).
3. Right-click `index.html` and choose **Open with Live Server**.

You can also double-click `index.html` to open it in any browser.
An internet connection is needed for the Google Fonts; without it the site falls back to Arial.

## Replace the images

All images are original abstract illustrations in the `images/` folder.

| File | Where it appears | Suggested size |
|------|------------------|----------------|
| `hero-image.jpg` | Hero section | 1200 x 1000 px |
| `about-image.jpg` | "Who We Are" section | 1000 x 800 px |
| `project-restaurant.jpg` | Portfolio card 1 | 1000 x 700 px |
| `project-portfolio.jpg` | Portfolio card 2 | 1000 x 700 px |
| `project-business.jpg` | Portfolio card 3 | 1000 x 700 px |

1. Save your new image with the **same file name** in `images/` to replace it automatically,
   or use a new name and update the `src="images/..."` in `index.html`.
2. Update the `alt` text so it describes the new image.
3. Keep roughly the same shape as the suggested size. The CSS crops with `object-fit: cover`,
   so other shapes will be trimmed rather than stretched.

## Edit the business details

All text lives in `index.html`. Use Ctrl+F to find and change it:

- **Business name / logo:** search for `Nova` (the logo appears in the header and footer).
  The "N" square is `.logo-mark`.
- **Tagline:** `Creative Ideas. Digital Growth.` in the hero.
- **Email, phone, location:** search for `novadigital.example` and `+94 00 000 0000`
  (Contact section and footer). They are marked as demonstration content, so remove those labels only
  if you replace them with real details.
- **Services and portfolio:** edit the text inside each `<article>` card. Copy a whole `<article>` block to add another.
- **Portfolio cards:** each card shows "Concept only – no live demo" because these fictional projects have no demo page.
  When you build one, replace that line with `<a href="your-demo-page.html" class="text-link">View Project <span aria-hidden="true">&rarr;</span></a>`.
- **Contact form:** a frontend demonstration only. "Send Message" checks the required fields and email format, then shows
  a "Demo only" message. Nothing is sent anywhere (HTML and CSS only, no JavaScript).
- **Colours:** change the variables at the top of `style.css` (`--violet`, `--indigo`, `--navy`, ...).

## Test mobile responsiveness

1. Open the site with Live Server, then press **F12** to open DevTools.
2. Press **Ctrl+Shift+M** (Cmd+Shift+M on Mac) to turn on device mode.
3. Choose **iPhone SE**, **iPad Mini** and desktop widths, or drag the edge of the preview to resize.
4. Check that:
   - Below 992px the menu becomes a hamburger button. Tap it to open and close the menu.
   - The hero and About sections stack vertically on mobile.
   - Service cards go from 4 columns to 2 to 1, and portfolio cards go from 3 columns to 1 on mobile.
   - There is no horizontal scrollbar at any width.

Note: the mobile menu is CSS only (a hidden checkbox), so it stays open after you tap a link.
Tap the "X" to close it. This is the normal trade-off of a no-JavaScript menu.

## Publish later

Because this is a static site, free hosting works well: GitHub Pages, Netlify (drag and drop the folder)
or Cloudflare Pages.
