# dolgirev.pe

Personal site of Pavel E. Dolgirev. It is one static page (`index.html` + `avatar.jpg`) hosted on GitHub Pages.

## 1. Put it on GitHub Pages (free)
1. On github.com, create a public repository named **PashaDolgirev.github.io**.
2. Push this folder to it (`git push`).
3. Go to Settings → Pages. Under "Source", pick **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. The site goes live at https://pashadolgirev.github.io within a minute or two.

## 2. Custom domain dolgirev.pe
1. Buy `dolgirev.pe` from a registrar that sells .pe, such as Namecheap or Gandi. Anyone can register .pe; expect roughly $30–60 per year.
2. In the registrar's DNS settings, add four A records for `@`:
   185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   and a CNAME record `www` → `pashadolgirev.github.io`.
3. In the repo, go to Settings → Pages → Custom domain. Enter `dolgirev.pe`, save, and tick **Enforce HTTPS** once it becomes available.
   GitHub then adds a `CNAME` file to the repo automatically; pull it with `git pull`.

## 3. Visit counter (GoatCounter, free)
1. Sign up at https://www.goatcounter.com with the code **dolgirev**, so your dashboard lives at dolgirev.goatcounter.com.
2. In GoatCounter Settings, enable **"Allow adding visitor counts on your website"**.
3. That's it. The footer shows "N visits", and the dashboard lists countries and where visitors came from.
   If you use a different code, change `GOATCOUNTER` at the top of the script in `index.html`.

## 4. "Buy me a coffee" button
1. Sign up at https://buymeacoffee.com and claim the page name **dolgirev**.
2. Connect payouts: it goes through Stripe, and you add your bank account there. Money then lands in your bank automatically. There are iPhone and Android apps.
3. If your page name differs, change `COFFEE_URL` at the top of the script in `index.html`.

## Editing papers
Each paper is one line in the `P` list inside `index.html`. The fields are: `y` year, `t` title, `a` authors, `v` venue, `j` journal link, `ar` arXiv ID (this also creates the arXiv and pdf buttons), and `id`, an optional anchor used by the Research section.
