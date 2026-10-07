# The Reading Reel website

This is the full website for www.thereadingreel.com, built to live on GitHub Pages for free.
Selling and booking happen on Stan Store, and email signups go to Flodesk.

## What's in this folder

| File | What it does |
|---|---|
| `index.html` | The whole website (one page: About, Services, Shop, Reviews, Freebies, Contact) |
| `404.html` | The page people see if they follow an old Wix link that no longer exists |
| `images/` | Your logo and photo go here |
| `CNAME` | Tells GitHub your domain is www.thereadingreel.com |
| `robots.txt`, `sitemap.xml` | Tell Google it's allowed to list your site (your Wix site was blocking this) |

---

## Step 1: Fill in your last three links

Your Instagram, TikTok, logo, and photos are already in. Open `index.html` in any text editor and use Find & Replace for these:

| Replace this | With |
|---|---|
| `STAN_STORE_URL` | Your Stan Store link, e.g. `https://stan.store/thereadingreel` |
| `SKOOL_URL` | Your Skool community link (until it's live, you can use `#freebies` so the button goes to your email signup) |
| `CONTACT_EMAIL` | The email you want parents and schools to use |

(Or send these to Claude and it will fill them in for you.)

## Step 2: Photos (already done)

The `images` folder already has your logo, favicon, hero photo, and three shop photos from your Wix media. To swap one, replace the file but keep the same file name.

## Step 3: Put it on GitHub

No coding tools needed. Everything happens in your web browser.

1. Sign in at github.com (or create a free account).
2. Click **+** (top right) → **New repository**.
   - Name it `thereadingreel-site`
   - Set it to **Public** (required for free GitHub Pages)
   - Click **Create repository**
3. On the next screen click **uploading an existing file**.
4. Drag in **everything inside this folder** (the files and the `images` folder), then click **Commit changes**.
5. Go to the repository's **Settings** → **Pages**.
   - Source: **Deploy from a branch**
   - Branch: **main**, folder **/ (root)** → **Save**
6. After a minute or two, GitHub shows a preview link like `https://YOURNAME.github.io/thereadingreel-site/`. Check that it looks right.

## Step 4: Connect Flodesk

1. In Flodesk, go to **Forms** → create an **Inline** form (call it something like "Website – Kickstart Kit").
2. Connect it to the segment you want new subscribers in, and set up your Kickstart Kit welcome email/workflow.
3. Click **Share** → **Embed code**. Flodesk gives you two pieces of code:
   - The first goes just before `</head>` near the top of `index.html`.
   - The second goes inside the box marked `PASTE YOUR FLODESK FORM EMBED CODE HERE`. Delete the placeholder line there.
4. In GitHub, open `index.html`, click the pencil icon, paste, and click **Commit changes**. The site updates by itself.

## Step 5: Point your domain at the new site

Do this only after the GitHub preview link looks good.

1. In GitHub **Settings → Pages → Custom domain**, enter `www.thereadingreel.com` and save.
2. Wherever your domain is managed (if you bought it through Wix, it's in Wix under **Domains → Manage DNS Records**), set:

   | Type | Host / Name | Value |
   |---|---|---|
   | A | @ | 185.199.108.153 |
   | A | @ | 185.199.109.153 |
   | A | @ | 185.199.110.153 |
   | A | @ | 185.199.111.153 |
   | CNAME | www | `YOURNAME.github.io` |

   Remove any old A or CNAME records for `@` and `www` that point to Wix.
3. DNS can take a few hours (occasionally up to 48). When GitHub shows the domain as verified, tick **Enforce HTTPS**.

## Step 6: Cancel Wix (last!)

- Only cancel your Wix **site plan** after www.thereadingreel.com is showing the new site.
- If your domain was bought through Wix, **don't let it lapse**. Either keep renewing it there or transfer it to a cheaper registrar such as Cloudflare or Porkbun (about $10–15/year).
- Make sure you've downloaded anything you need from Wix first: product files, customer and order exports from Wix Stores, contacts/email list (Contacts → Export), and booking history.

## Step 7: Tell Google you're back

Your Wix site was set to "noindex," so Google wasn't listing it. After launch:

1. Go to Google Search Console (search.google.com/search-console) and add `www.thereadingreel.com`.
2. Submit the sitemap: `https://www.thereadingreel.com/sitemap.xml`.

---

## Making changes later

- **Text:** open `index.html` on GitHub, click the pencil, edit, commit. Live in about a minute.
- **Colors:** the brand colors are listed at the top of `index.html` under "EASY EDITS."
- **Products and prices:** change them in Stan Store; the website just links there.
