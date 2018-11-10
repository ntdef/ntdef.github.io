---
layout: page
---
# Projects

- [cran-server](#cran-server)
- [groupby](#groupby)
- [Hume](#hume)

## [cran-server](https://github.com/UptakeOpenSource/cran-server)
`cran-server` is a CRAN like R package repository that can run in containerized environment
like Mesos or Kubernetes, meant for zero-touch R package hosting. I built `cran-server` while
at Uptake to host our internal packages to make it easier for data scientists to install
within their existing workflows without having to use git.

## [groupby](https://github.com/ntdef/groupby)
`groupby` is a command line tool for running group by operations in parallel, inspired by `xargs` and `GNU Parallel`. It's built with Rust, and it's really really fast. 

## [Hume](https://github.com/ntdef/hume)
`Hume` is a tool for building and deploying machine learning models that's language agnostic.
Hume tries to solve the problem of creating machine learning artifacts that are completely portable using Docker,
that are easily deployed and reproducible.