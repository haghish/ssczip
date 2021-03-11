> __Cite__: Haghish, E. F. (2020). Developing, maintaining, and hosting Stata statistical software on GitHub. The Stata Journal, 20(4), 931-951.

# ssczip

Most of Stata software are published on _Boston College Statistical Software Components_ (SSC) Archive. However, the packages are not stored there as downloadable zip files. Instead, each script file is stored in a seperate directory based on the first character of its name (e.g. _apple__ is stored in a directory of _A_) to ensure each script file has a unique name. The reason is that Stata lacks a modular package installation and thus, Stata user-written face a threat of having programs with similar names or similar file names, which can interrupt one another... The consequence is that SSC packages cannot be downloaded as Zip files.

Speaking of software version, when the package cannot be stored independently (e.g. as a zip file), managing its version also becomes difficult. In this case, every new update replaces the previous version and the users have no way to keep track of the version of the packages they use. The practice of software versionning is so poor on  SSC that the package versions can only be looked up by reading the source code (Assuming the author has cared about writing or updating it)!  

This, however, can be improved a little without applying a dramatic change in Stata. My solution was to provide a program that creates a Zip file for each package and uses the "release date" as a unique version indicator (not a good replacement, but certainly better than nothing).

The __`ssczip`__ program that is presented here __packages and downloads__ Stata packages from SSC as a zip file. More importantly, __it also reads the source code and includes the last release date of the package__ (as a unique identifier of version). With this package, you can download and store the current versions of the add-on packages you use in your data analysis and in case they change in the future, you can re-run and reproduce your previous analyses using the previous versions. 

## Installation


The [__`github package`__](https://github.com/haghish/github) is the only recommended way for installing **`ssczip`**. Once [__`github`__](https://github.com/haghish/github) is installed, type:

```js
github install haghish/ssczip, stable
```
