# lecture-slides

Lecture slides for [CS 2043][cs2043].  This repository has been designed to accompany the course website in the form of a git submodule.

## Acquiring the Slides

All you need to do is `git clone` this repository, the up to date pdf's are all being tracked.  When I add a new lecture or make changes to an existing one, you will receive these via a `git pull`, and you are done!

## Building the Slides

Is a bit more involved.  At a high level, the items you will need are

- XeLaTeX
- The Beamer-Metropolis theme.  You should be able to install either using the CTAN package, or from the source.
    - CTAN package: [here](https://www.ctan.org/pkg/beamertheme-metropolis)
    - Source Code: [here](https://github.com/matze/mtheme)
    - Review the README instructions on the source code page *regardless* of how you install it!
- The Mozilla Fira Sans font. Note that at this time, even if you have the `fira` tex package, you must install from source.
    - Source Code: [here](https://github.com/mozilla/Fira)
    - Effectively, all you need is all of the files in the `otf` folder, and to put them in a location where your OS knows to look for fonts.
        - On Linux
            - I made the directory `/usr/share/fonts/mozilla-FiraSans/`
        - On OSX (note: only available for *current* user...you could put it in `/Library` (no `~`), but I would suggest not playing around down there.
            - I made the directory `~/Library/Fonts/mozilla-FiraSans/`
        - For both: copy all of the `*.otf` files from the `Fira` repositories' `otf` folder into the directory you just made. Do not rename the files!
- The `DejaVuSansMono` font (should be there with any *TeX installation).
- The `minted` package for *TeX.
- I used the `monokai` code listings color scheme.  If you execute `pygmentize -L` and do not have `monokai` two options:
    - Change the `\usemintedstyle{monokai}` line in `common-header.input` to one that you do have (or just delete the line), or
    - Update `pygmentize` e.g. with `sudo pip3 install --upgrade pygments`

- - -
[cs2043]: http://cs2043-sp16.github.io/

Contributions are welcome in the form of Pull Requests.

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.

