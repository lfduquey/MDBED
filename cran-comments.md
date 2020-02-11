# Round 1

#### Test environments
* local OS X install, R 3.6.1
* ubuntu 14.04 (on travis-ci), R 3.6.1
* win-builder (devel and release)

#### Submission comments 
27-01-2020

0 errors | 0 warnings | 2 notes

* Two harmless notes.
* This is a new release.

#### Reviewer comments

10-02-2020 Jelena Saf

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

# Round 2

#### Test environments
* local OS X install, R 3.6.1
* ubuntu 14.04 (on travis-ci), R 3.6.1
* win-builder (devel and release)

#### Submission comments 

10-02-2020

0 errors | 0 warnings | 2 notes

* The sentence 'Through several functions, this package provides' was removed from the description field.
* Relevant citations were included in the description field.
* \dontrun{} was removed from the examples of each function; they are executable in < 5 sec.


#### Reviewer comments

10-02-2020 Uwe Ligges

*  The Title field should be in title case. Current version is:
   'Moran-Downton Bivariate exponential Distribution (MDBED)'
   In title case that is:'Moran-Downton Bivariate Exponential Distribution (MDBED)'
   Please omit the MDBED in the title as it is already the name.
*  The Description field should not start with the package name,'This package' or similar.
    Please fix and resubmit.

# Round 3
#### Test environments
* local OS X install, R 3.6.1
* ubuntu 14.04 (on travis-ci), R 3.6.1
* win-builder (devel and release)

#### Submission comments 

10-02-2020

0 errors | 0 warnings | 0 notes

* The title was written in title case.
* The MDBED was omitted in the title.
* The sentence 'This package' was removed from the description field.

