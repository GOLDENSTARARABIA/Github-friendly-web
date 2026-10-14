GOLDEN STAR ARABIA WEBSITE
==========================

FILES
  index.html     the page shell
  styles.css     all design, layout and animation (colors are the variables at the top)
  fonts.css      self-hosted fonts (files are in the fonts folder)
  script.js      all text, stock list and behaviour
  fonts/         the font files
  robots.txt, _headers, .htaccess   search-engine and caching settings (Netlify / Apache)
  assets/        hero.mp4 (landing video), director.webp, star.png (logo mark),
                 img/ (your radiator, workshop and boom truck photos)

HOW TO PUBLISH
  Upload the whole folder (keep the folder structure) to any web host:
  Netlify (drag the folder onto app.netlify.com/drop), GitHub Pages,
  Vercel, or cPanel public_html. index.html must stay at the top level.
  Open index.html in a browser to preview it on your computer.
  Everything is included, fonts too. No internet connection is needed to run it.

GITHUB PAGES (do these steps in order)
  1. Upload everything from inside this folder to the ROOT of your repository
     (index.html, 404.html, favicon.ico, script.js, styles.css, fonts.css and the
     assets and fonts folders). Do not upload the zip and do not put the files
     inside another folder. Upload ALL files again every time you update, so the
     old and new versions never get mixed.
  2. Open github-pages/static.yml. In your repository open
     .github/workflows/jekyll-gh-pages.yml, press the pencil icon, delete all of its
     text, paste the text of static.yml and press Commit changes. (This replaces the
     Jekyll build, which is not needed for this site.)
  3. Settings > Pages > Build and deployment > Source: choose "GitHub Actions".
  4. Open the Actions tab and wait for a green tick (1 to 3 minutes).
  5. Share the address shown in Settings > Pages (https://USERNAME.github.io/REPOSITORY/).
  If a page still looks old, press Ctrl+Shift+R (Cmd+Shift+R on Mac).
  If the site ever fails to start, visitors see a plain page with your phone, email
  and address and a Reload button instead of a dark empty screen.

HOW TO EDIT
  Open script.js. At the top:
    SITE  phone, email, director photo, hero video, and the product list
          (inventory: code, vehicle, type, material, status, dim in mm)
    TXT   every word on the site, in English (en) and Arabic (ar)
  Replace a photo: put a new file in assets/img/ with the same name (WebP format),
  or change its path in the ASSETS block at the top of script.js.
  Director name and story: TXT.en.dir and TXT.ar.dir.

STOCK SEARCH (Radiators page)
  SITE.stock in script.js holds your Excel stock list (make, model, year, code,
  description, Dammam / Riyadh / Jeddah quantities; the site shows only an overall In stock / Low stock / Out of stock status). SITE.dims holds the radiator
  sizes by stock code (mm: w, h, t, inlet i, outlet o, and src = source).
  A code without a size shows "On request" and a reference drawing.

NOTES
  - The product list, dimensions, vision/mission and director story are
    placeholders. Replace them with your real information.
  - Make sure you have the right to use every photo (the copper-brass
    radiator photo is from a magazine and the bar-and-plate and heavy-duty
    pictures look like supplier product photos).
  - The contact form opens the visitor's email app (mailto). To receive
    messages directly, connect a form service such as Formspree.
  - Please have a native Arabic speaker check the Arabic text.
