# maxineparedes.github.io
This repository contains code for my portfolio website that was built using Quarto. It includes content such as a Home page, an About page, and several blog posts.

## Installation Instructions

Before building the site, install the following (versions used are listed):
- [Quarto] 1.10.18
- [uv] 0.12.7
- [R] 4.6.1

## How to Build the Site
**1.** In a terminal window, clone the repository and change into it:
```bash
git clone https://github.com/maxineparedes/maxineparedes.github.io.git
cd maxineparedes.github.io
```
**2.** Using the same terminal, install the Python packages listed in `uv.lock` file:
```bash
uv sync
```

**3.** With an R console at the root, install the R packages listed in the `renv.lock` file:
```r
renv::restore()
```
**4.** Switching back to the terminal, build the site:
 ```bash
uv run quarto render
```

## Location of the Built Site
Once built, the site will be saved in the `docs/` folder. In order to access it locally, open `docs/index.html` in your web browser (e.g., right-click > Open in Browser), or run this in the terminal for a live preview:
```bash
uv run quarto preview
```

## Data
## Data

My blog posts use the Palmer Penguins dataset, collected by Dr. Kristen Gorman and Palmer Station, Antarctica LTER, and released under the [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) license. The data is bundled with the `palmerpenguins` R package and its Python port, so the build does not need the network to fetch it. Network access is only needed during steps 2 and 3 to download packages.

Horst AM, Hill AP, Gorman KB (2020). palmerpenguins: Palmer Archipelago (Antarctica) penguin data. R package version 0.1.0. https://allisonhorst.github.io/palmerpenguins/. doi: 10.5281/zenodo.3960218.