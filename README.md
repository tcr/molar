# incisor

CI integration shouldn't be like pulling teeth!

<code>Windows: [![Build status](https://ci.appveyor.com/api/projects/status/oj15ma4ayu7bimmp/branch/master?svg=true)](https://ci.appveyor.com/project/tcr/molar/branch/master)</code><br>
<code>Linux:&nbsp;&nbsp; [![Circle CI](https://circleci.com/gh/tcr/molar/tree/master.svg?style=svg)](https://circleci.com/gh/tcr/molar/tree/master)</code><br>
<code>OS X:&nbsp;&nbsp;&nbsp; [![Build Status](https://travis-ci.org/tcr/molar.svg?branch=master)](https://travis-ci.org/tcr/molar)</code>

stages:

* setup
* build
* test

All commands run in separate subshells.

---

OSes:

* appveyor: windows
* circle: linux
* travis: osx

submodules

* appveyor: http://help.appveyor.com/discussions/problems/930-git-checkout-and-submodules
* circle: https://circleci.com/docs/configuration#checkout
* travis: http://docs.travis-ci.com/user/customizing-the-build/#Git-Submodules

commit depth:

* appveyor: full, configurable
* circle: 10 (from all tips), not configurable (except with complete override)
* travis: 50, configurable

shells:

* appveyor: ps, cmd, cygwin
* circle: bash?
* travis: bash?

env:

* appveyor: literals in yaml
* circle: literals in yaml, but interpreted in encrypted ui
* travis: literals in yaml

folder:

* appveyor: folder preserved between commands (same shell)
* circle: folder not preserved between commands (separate subshells)
* travis: folder preserved between commands (same shell)

secure variables:

* appveyor: encrypted through ui, specified in yaml
* circle: encrypted through ui, automatically in env
* travis: encrypted through ui, automatically in env
