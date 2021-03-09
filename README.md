> __Cite__: Haghish, E. F. (2020). Developing, maintaining, and hosting Stata statistical software on GitHub. The Stata Journal, 20(4), 931-951.

# ssczip

Most of Stata software are published on _Boston College Statistical Software Components_ (SSC) Archive. However, Stata lacks a modular package installation and thus Stata user-written packages are stored in many directories with alphabetic names to ensure all program names are unique. The mere consequence is that SSC packages cannot be downloaded as Zip files and also, their versions can only be looked up by reading the source... 

__`ssczip`__ packages and download Stata packages from SSC as a zip file. More importantly, it also reads the source code and includes the last release date of the package (as a unique identifier of version). 

With this package, you can download and store the current versions of the add-on packages you use in your data analysis and incase they change in the future, you can re-run and reproduce your previous analyses using the previous versions. 


## Installation


The [__`github package`__](https://github.com/haghish/github) is the only recommended way for installing **`ssczip`**. Once [__`github`__](https://github.com/haghish/github) is installed, type:

```js
github install haghish/ssczip, stable
```
