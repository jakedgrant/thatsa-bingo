# That's a bingo!

A single static page at [thatsa.bingo](https://thatsa.bingo), hosted on GitHub Pages.

The page displays a looping GIF from *Inglourious Basterds* (2009). The GIF is stored in this repository, so visitors don't depend on a third-party embed. [GIF source on GIPHY](https://giphy.com/gifs/stephen-django-djangostephen-DFu7j1d1AQbaE).

## Editing

Edit `index.html` or replace `assets/thats-a-bingo-giphy.gif`, then push to `main`. GitHub Pages publishes the repository root. No build step or dependencies are needed.

To preview locally, run `python3 -m http.server 8000`, then open <http://localhost:8000>.

## Domain setup

GitHub Pages uses `thatsa.bingo` as its custom domain. Keep the `CNAME` file in the repository.

In Porkbun DNS, replace the default parking records with:

| Type | Host in Porkbun | Answer |
| --- | --- | --- |
| A | Leave blank | 185.199.108.153 |
| A | Leave blank | 185.199.109.153 |
| A | Leave blank | 185.199.110.153 |
| A | Leave blank | 185.199.111.153 |
| AAAA | Leave blank | 2606:50c0:8000::153 |
| AAAA | Leave blank | 2606:50c0:8001::153 |
| AAAA | Leave blank | 2606:50c0:8002::153 |
| AAAA | Leave blank | 2606:50c0:8003::153 |
| CNAME | www | jakedgrant.github.io |

Enable **Enforce HTTPS** in the repository's Pages settings once GitHub issues the certificate. GitHub manages certificate renewal.

References: [GitHub custom domains](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site), [Porkbun DNS editing](https://kb.porkbun.com/article/68-how-to-edit-dns-records).
