# RE/MAX Boone Realty — Agent Social Studio

A static, browser-based agent social content generator, prepared for **GitHub Pages**.

## Publish with GitHub Pages

1. Create a new GitHub repository, such as `agent-social-studio`.
2. Upload **the contents of this folder** to the repository root (including `index.html`, `assets/`, and `.nojekyll`). You can also upload the ZIP contents using GitHub Desktop or Git.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**; choose **main** and **/(root)**, then save.
5. Wait for GitHub Pages to show the live URL. Your site will usually be `https://YOUR-USERNAME.github.io/agent-social-studio/`.

GitHub Pages is public hosting. Do not commit agent headshots, personal phone numbers, private contact information, or unlicensed photography to the repository. Agents enter their details and upload poses in their own browser session.

## Add more background photos

The 12 starter backgrounds are in `assets/photos/` and work without editing any code.

For additional photos:

1. Copy `.jpg`, `.jpeg`, `.png`, or `.webp` files into `assets/photos/`. Prefer optimized square or landscape files (about 1200–1800px across; typically under 400 KB each). Use **licensed photos** with permission for marketing use.
2. Edit `assets/photos/library.json` and add **one object per photo**, like:

```json
[
  {
    "id": "gutters-autumn-01",
    "file": "gutters-autumn-01.jpg",
    "name": "Autumn gutter maintenance",
    "tags": ["gutter", "roof", "exterior", "autumn", "fall", "maintenance", "leaves"]
  },
  {
    "id": "kitchen-white-01",
    "file": "kitchen-white-01.webp",
    "name": "Bright kitchen with island",
    "tags": ["kitchen", "island", "countertop", "cabinet", "renovation", "interior"]
  }
]
```

3. Commit/push both the images and updated JSON manifest. GitHub Pages will publish the updated library automatically. Each generated post shows **three topic-ranked photo options in a dropdown**.

**Important:** GitHub Pages cannot automatically enumerate files in a directory. A photo must be listed in `library.json` to become available to the generator. The JSON manifest is the photo catalog. Photos are never uploaded by agents.

**Performance:** 1,000 large photos will make the site slow and the repository heavy. Keep images compressed; for larger libraries, consider a thumbnail/index architecture and lazy loading. This prototype currently creates image objects for the catalog and loads them in the browser; test performance before adding hundreds of photos.

## Fonts and other assets

The supplied **Allura Regular** font is in `assets/fonts/Allura-Regular.ttf` and is loaded locally from the deployed site. No Google Fonts dependency is required. The approved brokerage logo and existing content are preserved in the application HTML.

## Operational notes

- The site is entirely static. It does not save agent profiles to a server, host generated images, or publish to social platforms.
- Agent pose creation still happens in ChatGPT, then agents upload their finished transparent PNG poses to the site.
- Browser-side downloads/exports should be tested in Chrome and Edge after deployment.
- This is a deployable prototype, not a security/compliance certification. Review photo rights, brokerage logo placement, required contact details, content accuracy, accessibility, and export behavior before sharing with agents.


## Light theme and font options
This edition removes the navy interface background, uses cream/white/charcoal and RE/MAX red/blue accents, and adds an agent-facing headline font dropdown on Step 1. Allura is bundled locally. The additional options are browser standard fonts (Georgia, Times New Roman, Trebuchet MS), so they do not require downloads. The dark tile behind the official brokerage logo remains for contrast.


## Expanded font choices and image visibility

The headline font selector now includes Allura, Tangerine Regular/Bold, Italianno, Corinthia Regular/Bold, and three standard typefaces. All script fonts are bundled in `assets/fonts/`. The photo darkening overlay was reduced from 40% to 27% black, making the property photographs more visible. The footer still uses Allura for the agent name.


## Latest update
Headline font selection is on Step 5, with clickable font samples and a live preview. The uploaded white RE/MAX Boone Realty logo is embedded directly into the generated graphic footer. Some browsers do not style native dropdown options with custom fonts; the preview tiles work around this.
