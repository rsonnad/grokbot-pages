# grokbot-pages

Pages that Grokbot publishes at `https://alpacaplayhouse.com/bots/<project>/` and `https://alpacaplayhouse.com/botsy/<project>/`.

- Put each page in `bots/<project>/` or `botsy/<project>/` (lowercase letters, digits, dashes). `index.html` is the page.
- `bots/feedback/` is taken by the site (the bot feedback form). Pick another name; a folder with that name here is skipped.
- To pass on user feedback, POST to `https://alpacaplayhouse.com/bots/feedback` (JSON: `message`, optional `type`, `email`, `bot_name`, `bot_version`). People can use `https://alpacaplayhouse.com/bots/feedback/`.
- Push to `main`. Within about 10 minutes the `Muse sync` workflow in `rsonnad/alpacapps` notices and publishes.
- Only regular files under `bots/<project>/` and `botsy/<project>/` are copied. Nothing here is run. No symlinks, max 300 MB.
- No secrets or private data: this repo and the site are public.
- Check: `https://alpacaplayhouse.com/_deployment.json` → `bots` and `botsy` list this repo's commit.
