# Round 1

#### Test environments
* local OS X install, R 3.6.1
* ubuntu 14.04 (on travis-ci), R 3.6.1
* win-builder (devel and release)

#### R CMD check results
There were no ERRORs, or WARNINGs.

There were 2 NOTEs:

  * Checking CRAN incoming feasibility ... NOTE
  Maintainer: 'Luis F. Duque <lfduquey@gmail.com>'
  
  According to CRAN Maintainer Uwe Ligges, "This is just a note that reminds CRAN maintainers to check that the          submission comes actually from his maintainer and not anybody else." Thus, it can be considered a harmless note.

  * checking top-level files ... NOTE
  Files 'README.md' or 'NEWS.md' cannot be checked without 'pandoc' being installed.
  
  It is a harmless note. If I add the README.md file to .Rbuildignore, this note will disappear, but I prefer to leave   it. 
  

#### Submission comments 
27-01-2020

* New submission
  
  
#### Reviewer's comments

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
* "\dontrun{}" should be only used if the example really cannot be executed
(e.g. because of missing additional software, missing API keys, ...) by
the user. That's why wrapping examples in "\dontrun{}" adds the comment
("# Not run:") as a warning for the user.
Please unwrap the examples if they are executable in < 5 sec, or create
additionally small toy examples to allow automatic testing.
You could also replace "\dontrun{}" with "\donttest{}", but it would be
preferable to have automatic checks for functions.

# Round 2

#### Submission comments 

10-02-2020 This is a resubmission. In this version I have:

* Removed the sentence 'Through several functions, this package provides' from the description field.
* Included relevant citations in the description field.
* Unwrapped the examples of each function; they are executable in < 5 sec.


#### Reviewer's comments

10-02-2020 Uwe Ligges

*  The Title field should be in title case. Current version is:
   'Moran-Downton Bivariate exponential Distribution (MDBED)'
   In title case that is:'Moran-Downton Bivariate Exponential Distribution (MDBED)'
   Please omit the MDBED in the title as it is already the name.
*  The Description field should not start with the package name,'This package' or similar.
    Please fix and resubmit.

# Round 3

#### Submission comments 

12-02-2020 This is a resubmission. In this version I have:

  * Written the title in title case.
  * Omitted the MDBED in the title.
  * Removed the sentence 'This package' from the description field.
  * Used "\donttest{}" for the examples of the functions CDF_3dPlot and Contour_Plot. The run times of these 
  examples depend on the number of cores of the computer; they can be greater than 5 seconds.
  
#### Reviewer's comments

10-02-2020 Martina Schmirl

  * Please ensure that you do not use more than 2 cores in your examples.


# Round 4

#### Submission comments 

21-02-2020 The functions that use more than one core are CDF_3dPlot, Contour_Plot, pBED, and rBED. They are limited to using a number of cores <=2 (It is done by using a ifelse statement). If they would use more than 2 cores, it would appear in the R CMD check results (which is not the case). Therefore, I do not understand the reviewer's comments. However, in this resubmission, I have changed the ifelse statement by the if… else statement which, I think, is the only thing that can cause an error in the number of cores chosen. However, as I mentioned above, the package passes the RCMD check by using the ifelse statement. 
