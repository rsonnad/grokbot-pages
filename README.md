# grokbot-pages

Pages that Grokbot publishes at `https://alpacaplayhouse.com/bots/<project>/`.

- Put each page in `bots/<project>/` (lowercase letters, digits, dashes). `index.html` is the page.
- Push to `main`. Within about 10 minutes the `Muse sync` workflow in `rsonnad/alpacapps` notices and publishes.
- Only regular files under `bots/<project>/` are copied. Nothing here is run. No symlinks, max 300 MB.
- No secrets or private data: this repo and the site are public.
- Check: `https://alpacaplayhouse.com/_deployment.json` → `bots` lists this repo's commit.
