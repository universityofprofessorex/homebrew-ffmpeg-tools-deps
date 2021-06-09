# homebrew-ffmpeg-tools-deps
Custom formulas to install/compile ffmpeg dependencies

[![Build Status](http://img.shields.io/travis/bossjones/homebrew-ffmpeg-tools-deps.svg?style=flat)](https://travis-ci.org/bossjones/homebrew-ffmpeg-tools-deps)

[Homebrew](http://brew.sh/) head-only [tap](https://github.com/Homebrew/homebrew/wiki/brew-tap) for [CMU Sphinx](http://cmusphinx.sourceforge.net/). Please see caveats for using head-only versions [here](https://github.com/Homebrew/homebrew-headonly#why-is-head-only-bad).

This has been tested on OSX Catalina 10.15.7. Feedback for other versions welcomed.

## Usage

Add the Homebrew tap:

```bash
$ brew tap universityofprofessorex/ffmpeg-tools-deps
```

You'll see some warnings as these formulae conflict with those in the main reponitory, but that's fine.

Install the libraries:

```bash
$ brew install --HEAD universityofprofessorex/ffmpeg-tools-deps/university-lnav
```

You can test continuous recognition as follows:

### Re-installing

To re-install, uninstall before following the instructions above:

```bash
$ brew uninstall university-lnav
```


## Troubleshooting

Please be aware that lnav is not maintained anymore. You can try submitting bugs [here](https://libav.org).

A few people seem to be experiencing this error (as descibed in #2). The solution seems to be to run the following and retry:

```bash
$ brew doctor
$ brew prune
```

--------------------------------
# Inspiration from
- https://github.com/half2me/homebrew-gstreamer
- https://github.com/Homebrew/brew/blob/master/docs/How-to-Create-and-Maintain-a-Tap.md
- https://github.com/watsonbox/homebrew-cmu-sphinx
- https://github.com/bossjones/homebrew-scarlett-deps
- https://github.com/Homebrew/homebrew-core/blob/HEAD/Formula/libav.rb