# jamesjunyuguo.github.io

Personal website of Junyu (James) Guo. Built with Jekyll and served by GitHub Pages:
push to `master` and the site rebuilds on its own.

## Where to edit things

| I want to...                         | Edit this                                             |
| ------------------------------------ | ----------------------------------------------------- |
| Change the bio on the home page      | `_pages/about.md` (the hero sentence is `lead:`)      |
| Add a news item                      | `_data/news.yml` (add at the top)                     |
| Add or edit a paper                  | `_data/publications.yml` (`selected: true` shows it on the home page) |
| Add work under review                | `_data/working_papers.yml`                            |
| Change the research interest cards   | `_data/interests.yml`                                 |
| Add a course                         | `_data/courses.yml`                                   |
| Add a course I taught                | `_data/teaching.yml`                                  |
| Update the CV page                   | `_data/cv.yml`, and replace `assets/CV_Junyu_Guo.pdf` |
| Write a blog post                    | new file in `_posts/` named `YYYY-MM-DD-title.md`     |
| Write a note                         | new file in `_portfolio/` (math with `$...$` works)   |
| Change name, email, social links     | `_config.yml` under `author:`                         |
| Change the top navigation            | `_data/navigation.yml`                                |
| Change colors or fonts               | the tokens at the top of `assets/css/site.css`        |

To use math in a blog post, add `math: true` to its front matter. Notes have it on by default.

## Structure

- `_layouts/`: `default` (page shell), `home`, `page`, `post` (blog posts and notes)
- `_includes/`: head, header, footer, social icons, paper card, inline SVG icons
- `assets/css/site.css`: all styles, plain CSS, light and dark themes
- `assets/js/site.js`: theme toggle, mobile menu, scroll reveal
- `assets/fonts/`: self-hosted fonts (Bricolage Grotesque, Inter, Source Serif 4; SIL Open Font License)

## Preview locally

```bash
bundle install
bundle exec jekyll serve --config _config.yml,_config.dev.yml
```

Then open http://localhost:4000.

## Credits

Icons from Lucide (ISC) and Simple Icons (CC0).
