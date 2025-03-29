![](/assets/images/nes.gif)
# 8bit Nintendo Science

This is a fan-maintained Jekyll site hosted on GitHub Pages that tracks Dr. Jeff Gerstmann’s scientific mission to rank all NES games released in North America. ([YouTube](https://www.youtube.com/playlist?list=PLDKeuvgV0sxZ_xs4zUvQcMEV-LTjSf-Ok)).

## Contributing

Feel free to open an issue or pull request to help improve the site.

The main content of this site is on [/_data/list.csv](/_data/list.csv).

| Column      | Description                                                                 |
|-------------|-----------------------------------------------------------------------------|
| `game`      | Title of the game                                                           |
| `ep`        | Episode number where the game was discussed                                 |
| `ytid`      | YouTube video ID for the episode                                            |
| `seconds`   | Timestamp (in seconds) where the game appears in the video                  |
| `screenshot`| Filename of the game’s image in the [Libretro Thumbnails](https://github.com/libretro-thumbnails/libretro-thumbnails) repository|
| `wiki_line` | Line number for the game in [\_data/licensed_games.csv](/\_data/licensed_games.csv) or [\_data/unlicensed_games.csv](/\_data/unlicensed_games.csv). Prefixed with `l_` or `u_` to indicate the source file. |

The template will try to find the content for `screenshot` and `wiki_line` automatically based on the game title.

Due to GitHub Pages restrictions (no custom code), this is limited to simple string matching using Jekyll’s `where_exp` filter. When the automatic search fails, you'll have to manually add the content.

You can search for the content in [data.html](https://8bitnintendo.science/data.html).

## Running Locally

To run the site locally with Jekyll:

1. Make sure you have [Ruby](https://www.ruby-lang.org/en/) and [Bundler](https://bundler.io/) installed.
2. Clone the repository:

   ```bash
   git clone https://github.com/vNakamura/8bitnintendo-science.git
   cd 8bitnintendo-science
   ```

3. Install dependencies:
   ```bash
   bundle install
   ```

4. Run the Jekyll server:
   ```bash
   bundle exec jekyll serve --livereload
   ```

5. Open your browser and go to http://localhost:4000.

More information on https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll
