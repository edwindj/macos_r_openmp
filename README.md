## openmp on MacOS

This is a configuration to enable openmp on MacOS. 
It is based on the instructions found in <https://mac.r-project.org/openmp>, with the extra assumption that 
you, the user, use `brew` to manage packages on your system. 

Copy the "Makevars" file to "~/.R/Makevars".

Install libomp:

```bash
brew install libomp
```

Whenever you want omp support from an R package, e.g. `data.table`, make sure you do an "source" install, which
allows the package to find the libomp installation.

```R
install.packages("data.table", type="source")
```
