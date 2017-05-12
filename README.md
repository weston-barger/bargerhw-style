# bargerhw-style

`bargerhw` is a package which includes my style commands, marcos and environments for typesetting homework.

To use, simply place "bargerhw.sty" and "lmacros.sty" in your latex path and use `\usepackage{bargerhw}` to include. One way to achieve this is to put "bargerhw.sty" and "lmacros.sty" in the same directory as your latex document which includes `bargerhw`. 

### Arguments
 Optional arguments:

* `lmacros`     - When specified, the the macros defined in `lmacros.sty' are included. These are mostly my preferred math shortcuts and are not essential to the package's use. 

* `draft`       - When specified, equation labels are shown on the left

* `doublespace` - When specified, document is double spaced

* `typewriter` - When specified, uses typewriter font, `LGRgreek` option in `mathastext`, and `lmtt` font for greek math letters 


### Commands for the document title 

Use these commands in your document preamble i.e. before `\begin{document}`. There is no need to use `\maketitle` after `\begin{document}`

*  `\course` (required) - specifies the course name 

*  `\name`   (required) - specifies the author

*  `\hwnum`  (optional) - specifies homework number

*  `\email`  (optional) - specifies the author's email

### Environments for exercises

* `exercise`  - This is the environment for exercises. Includes an optional argument for specifying title text (e.g. corresponding book exercise).

* `subpart`   - Used inside `exercise` to denote a subpart of the exercise. Includes an optional argument for specifying title text (e.g. corresponding book exercise).


* `subparta`  - Just like `subpart`, except using latin letters instead of numbers for list.

* `subsubpart` - Used inside `subpart` to denote a sub-subpart of the exercise. Includes an optional argument for specifying title text (e.g. corresponding book exercise).

* `subsubparta`- Just like `subsubpart`, except using latin letters instead of numbers for list.

* `solution`  - For denoting the solution. Includes and optional argument to set the `\qedsymbol` for the end of the exercise.


### Note
* The `eqnarray` environment is made illegal i.e. `\PackageError` is thrown when `eqnarray` is used. Please use the `align` environment instead, even for one line equations. 