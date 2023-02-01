This is a repository for phylogenetics packages in R. It is like CRAN, but builds directly from GitHub or other repositories without packages needing to pass CRAN checks. For regular users, this gives you access to packages that are not yet on CRAN (or that have been kicked off as requirements change) that are compiled for your computers. There is a possibility that there is something wrong with the packages, of course (this is true on CRAN, but less likely due to their robust checking). For package developers, this lets package changes be pushed out more quickly and have packages that don't comply with CRAN's standards (like having a package that might require three entire floppy disks to store: CRAN's limit for a package is 5 MB total). 

To use this, if you want to go here first to look for packages, include this in your R session:

```
options(repos = c(
  phylotastic = 'https://phylotastic.r-universe.dev',
  CRAN = 'https://cloud.r-project.org')
 )
```

That will look for packages on this server first, then only go to CRAN for packages that aren't here.

If you want to use CRAN first, and then only go here if a package isn't on CRAN, do:

```
options(repos = c(
  CRAN = 'https://cloud.r-project.org'),
  phylotastic = 'https://phylotastic.r-universe.dev'
 )
```

The only difference in practice will be if the version on CRAN is older than the version in the R-universe: the first approach will install the newer one from here, the second approach will install the older one from CRAN.

If you know of a package that should be added, email Brian O'Meara (bomeara@utk.edu).

You might also be interested in the [CRAN Task View for Phylogenetics](https://cran.r-project.org/web/views/Phylogenetics.html)
