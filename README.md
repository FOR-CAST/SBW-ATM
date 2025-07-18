# Spruce Budworm Atmospheric Transport Model (Website)


<img src="images/sbw_nrcan.jpg" style="width:75.0%"
alt="Source: https://natural-resources.canada.ca/forest-forestry/insects-disturbances/spruce-budworm" />

This is a [Quarto](https://quarto.org/) website developed using the
[RStudio IDE](https://posit.co/products/open-source/rstudio/). This
project uses [`renv`](https://rstudio.github.io/renv/articles/renv.html)
to manage R package dependencies.

The site is automatically built using [GitHub
Actions](https://github.com/features/actions) and published via [GitHub
Pages](https://pages.github.com/).

## Getting started

You will need `git`, `R`, `RStudio`, and Quarto installed.

1.  [Clone](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)
    the repository from GitHub;

2.  Open the project in the RStudio IDE;

3.  You will be prompted to install the required R package dependencies
    – use `renv::restore()` to install the necessary package versions;

4.  Add the Quarto
    [`fontawesome`](https://github.com/quarto-ext/fontawesome)
    extension:

    ``` bash
    quarto add quarto-ext/fontawesome
    ```

5.  See <https://quarto.org/docs/websites/#workflow> for working with
    Quarto;

### File and directory structure

#### Project configuration files

- The Rstudio project file `SBW-ATM.Rproj` contains project
  configuration information;
- The R package versions required to work with the project are recorded
  in `renv.lock` and installed to a subdirectory of `renv/`;

#### Website configuration files

- Overall website layout, navigation, and theme, are defined in
  `_quarto.yml`;
- See <https://quarto.org/docs/websites/#website-theme> for configuring
  the website’s theme;
- See <https://quarto.org/docs/websites/website-navigation.html> for
  configuring website layout and navigation;

#### Website content

- Images and logos are located in `images/`;
- Animated images depicting simulation runs of the model are located in
  `outputs/` and organized by year;
- Pages are rendered using the `.qmd` files (*NOTE:* this `README.qmd`
  file and it’s rendered `REAADME.md` are not built as part of the
  site);
- Bibliographic references are used by some pages, and may be referenced
  in several `.bib` files:
  - `publications.bib` lists all of the publications *using* the SBW-ATM
    tool;
  - `references.bib` lists all of the publications *used by* the SBW-ATM
    tool; (see <https://quarto.org/docs/authoring/citations.html> for
    more information about using citations)

#### Built website files

- The built (generated) website files are in `docs/`;
- You can preview your changes after rendering the site by opening
  `docs/index.html` in your web browser;

## Updating the site

After making any updates, render the website locally to preview your
updates. If all looks good, commit your changes to the source files, and
push to GitHub.

> [!WARNING]
>
> Do not commit any of the rendered website files in `docs/` (they are
> already `.gitignore`d). These files will be automatically built and
> the website rendered using [GitHub
> Actions](https://github.com/features/actions).

> [!TIP]
>
> To avoid rebuilding the site after making minor changes, use
> [`[skip ci]`](https://docs.github.com/en/actions/how-tos/managing-workflow-runs-and-deployments/managing-workflow-runs/skipping-workflow-runs)
> in the commit message.
