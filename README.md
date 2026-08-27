# thunderdawg.com

The public landing page for **Thunder Dawg** — hyperlocal thunderstorm warning
for dogs who hate storms, serving Chagrin Falls, Ohio.

Static [Jekyll](https://jekyllrb.com) site, deployed by **GitHub Pages** from
the `main` branch. It is a translation of the Rails homepage in the `rainman`
app (`app/views/home/show.html.erb`); every figure on it is a labelled backtest
number, not a live reading.

## Structure

| Path | What it is |
| --- | --- |
| `index.html` | The page. Front matter + body; renders through the layout. |
| `_layouts/default.html` | HTML skeleton: head, favicon, stylesheet link. |
| `assets/css/main.css` | All styling, self-contained (own `:root` tokens, light/dark). |
| `assets/images/` | TJ's poses. |
| `_config.yml` | Site config. |
| `CNAME` | Custom domain: `thunderdawg.com`. |

## Run it locally

```bash
bundle install
bundle exec jekyll serve
```

Then open <http://127.0.0.1:4000>.

## Deploy

Push to `main`. GitHub Pages rebuilds and serves it. The custom domain is set
by the `CNAME` file; the DNS records for `thunderdawg.com` are configured at the
registrar.
