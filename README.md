Data Product dp_cars_us001
================

To build and deploy

### STEP 1: Activate the project

Clone the project, set working directory to project top folder and
activate

``` r
dpbuild::dp_activate(project_path = ".")
```

### STEP 2: Set environment variables

Set `GITHUB_PAT` as environment variable for
<https://github.com/camorosi/dp_cars.git>

``` r
Sys.setenv("GITHUB_PAT" = "<GIHTUB_PAT for the remote url>")
```

Set environment variables as needed to enable evaluation of

\`\`

and order to access the data board

| board_type  | board_alias | folder        |
|:------------|:------------|:--------------|
| local_board | cars_test   | \~/devel/test |

### STEP 3: Build

This by convention involves sourcing the main script `dp_make.R`

``` r
source("./dp_make.R")
```

### STEP 4: Deploy

Simple call to `dpdeploy`. By default expects you to be in the project
directory

``` r
dpdeploy()
```
