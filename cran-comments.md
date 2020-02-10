## Test environments
* local OS X install, R 3.6.1
* ubuntu 14.04 (on travis-ci), R 3.6.1
* win-builder (devel and release)

## R CMD check results

0 errors | 0 warnings | 2 notes

* This is a new release.

## CRAN-comments by Jelena Saf
* Please omit the redundant 'Through several functions, this package
provides' from your description field.
* If there are references describing (the theoretical backgrounds of) the
methods in your package, please add these in the description field of
your DESCRIPTION file in the form
authors (year) <doi:...>
authors (year) <arXiv:...>
authors (year, ISBN:...)
or if those are not available: <https:...>
with no space after 'doi:', 'arXiv:', 'https:' and angle brackets for
auto-linking.
(If you want to add the title as well, quote it. --> "title").
* \dontrun{} should be only used if the example really cannot be executed
(e.g. because of missing additional software, missing API keys, ...) by
the user. That's why wrapping examples in \dontrun{} adds the comment
("# Not run:") as a warning for the user.
Please unwrap the examples if they are executable in < 5 sec, or create
additionally small toy examples to allow automatic testing.
You could also replace \dontrun{} with \donttest{}, but it would be
preferable to have automatic checks for functions.

## Address CRAN-comments by Jelena Saf
* The sentence 'Through several functions, this package provides' was removed from the description field.
* Relevant citations were included in the description field.
* \dontrun{} was removed in the examples of each function; they are executable in < 5 sec.
