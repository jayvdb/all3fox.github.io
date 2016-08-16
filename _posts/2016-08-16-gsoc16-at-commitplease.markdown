---
layout: post
title: GSoC16 at commitplease
---

TL;DR Here is a [list of my commits][1] to commitplease made during Google Summer of Code 2016

# What has been done

[Commitplease][13] is an npm module which checks that your commit messages follow a commit message style. During GSoC16, I added support for:

 1. AngularJS commit message style
 1. 3rd party git hook managers: [PR to overcommit][8] and [PR to husky][5]

As well as that, I fixed [commitplease/jQuery Core][2] issue, improved unit-test coverage, updated documentation, implemented a CLI and worked on supporting multiple node/npm versions.

# What is to be done

As of this writing, there are open PRs to [Angular 1][4] and [Angular 2][3] about using commitplease. The plan is to get them merged. There is also an ongoing [effort to spread the word][14] about commitplease.

# Thank you

I would like to thank Google for the fantastic [GSoC program][9] and [jQuery Foundation][10] for a multitude of amazing Open-source projects and an unbelievably [friendly team][11]. A huge thank you to my mentor [Jörn Zaefferer][12] for being so helpful, knowledgeable and patient! I have very much enjoyed working with you!

[1]: https://github.com/jzaefferer/commitplease/commits/master?author=all3fox
[2]: https://github.com/jquery/jquery/pull/3176
[3]: https://github.com/angular/angular.js/pull/14888
[4]: https://github.com/angular/angular/pull/9953
[5]: https://github.com/typicode/husky/pull/47
[6]: https://github.com/npm/npm/issues/5452
[7]: https://github.com/npm/npm/issues/13381
[8]: https://github.com/brigade/overcommit/pull/408
[9]: https://developers.google.com/open-source/gsoc/
[10]: https://jquery.org/
[11]: https://jquery.org/team/
[12]: https://github.com/jzaefferer/
[13]: https://github.com/jzaefferer/commitplease/
[14]: https://github.com/jzaefferer/commitplease/issues/62