# Lense and Sensibility

Amit Singh's photography website, hosted free on GitHub Pages. Each tab at the top of the site is one collection (for example **Mysore Trip**), plus an **About** tab.

- `index.html` is the gallery that visitors see.
- `upload.html` is your private page for adding photos from a phone or laptop.
- `photos.json` holds the site name, the About text, and every tab with its photos and captions.
- `photos/` holds the image files. `photos/md/` and `photos/sm/` hold smaller copies that the gallery grid loads so pages open faster; the upload page makes these for you.
- `share.jpg` is the picture shown when someone shares a link to the site (WhatsApp, LinkedIn and so on). The preview tags at the top of `index.html` point to `https://amitrishu-del.github.io/photography/`; change those two addresses if the site moves to another name or your own domain.

---

## One-time setup (about 15 minutes)

### Step 1. Create the repository
1. Sign in at github.com (or create a free account).
2. Click **+** at the top right, then **New repository**.
3. Name it `photography`, choose **Public**, and click **Create repository**.

### Step 2. Upload the files
1. On the new repository page, click **uploading an existing file**.
2. Unzip the folder you received, open it, select **everything inside** (`index.html`, `upload.html`, `photos.json`, `README.md` and the `photos` folder), and drag it all into the browser window.
3. Click **Commit changes**.

(The hidden `.nojekyll` file is optional. If your computer hides it, skip it.)

### Step 3. Turn on the website
1. In the repository, open **Settings**, then **Pages** in the left menu.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Choose branch **main**, folder **/ (root)**, and click **Save**.
4. Wait 1 to 2 minutes. Your site is now live at
   `https://YOUR-USERNAME.github.io/photography/`

### Step 4. Create your upload key (token)
The key lets your upload page save photos into this one repository, and nothing else.

1. On GitHub, click your profile photo, then **Settings**.
2. At the bottom of the left menu, click **Developer settings**, then **Personal access tokens**, then **Fine-grained tokens**.
3. Click **Generate new token**.
   - **Token name:** `photo uploads`
   - **Expiration:** 1 year (GitHub will remind you before it expires)
   - **Repository access:** **Only select repositories**, then pick `photography`
   - **Permissions:** open **Repository permissions**, find **Contents**, and set it to **Read and write**
4. Click **Generate token** and copy it right away. GitHub shows it only once.

### Step 5. Connect the upload page
1. Open `https://YOUR-USERNAME.github.io/photography/upload.html`
2. Fill in your username, `photography`, and paste the key.
3. Keep **Remember on this device** ticked on your own phone or laptop, and click **Connect**.

---

## Adding photos later
1. Open `upload.html`.
2. Choose photos straight from the camera. Each one is resized automatically, its GPS location is removed, and its camera settings (lens, aperture, shutter, ISO) are read and saved.
3. Pick which tab they go in, or choose **+ New tab…** and give it a name (for example `Coorg Trip`).
4. Write a title, subtitle and short story for each.
5. Press **Publish**. The gallery updates in about a minute.

You can also change a tab's cover photo or remove a photo from the same page.

## Changing text
In `photos.json`, `site` holds the site name and the About text, and `albums` holds one entry per tab (its name, heading, intro and photos). The order of `albums` is the order of the tabs.

To change any of this, open `photos.json` on github.com, click the pencil icon, edit the text, and click **Commit changes**.

## Keeping it safe
- Never paste the key into any file in the repository.
- If you lose a phone or laptop that has the key saved, delete the token on GitHub (Settings → Developer settings → Fine-grained tokens) and make a new one.
- The key only works for this one repository, so it cannot touch anything else in your GitHub account.
