---
layout: page
title: Contribute
---

* [How to contribute](#howcontrib)
    * [Cats for git!!](#git)
    * [Love git - i'm so so on R](#gitlessr)
    * [What's git?](#nogit)
    * [I just wanna say something](#issue)
* [Contributors](#contributors)

## <a href="#howcontrib" name="howcontrib">#</a> How to contribute

<a href="#git" name="git">#</a> __If you like git__

1. Fork <https://github.com/sckott/apisforcats> to your account
2. Clone down to your machine from your account
3. Add an upstream remote for the `sckott/apisforcats` repo by doing `git remote add upstream git@github.com:sckott/apisforcats.git`
4. Make a new feature branch
5. The only file to change is `index.Rmd`. It's a R markdown document, which is essentially just Markdown, so should be easy to add to/change. After you make your changes, run `knit("index.Rmd")` in R, which will build a new `index.md`. If you have time/interest, also build the html page by doing `jekyll build`. This requires `jekyll` of course. You can also preview the site by doing `jeyll serve`, then navigate in your browser to <http://localhost:4000>
6. Commit those changes and push to your account
7. Send a pull request to `sckott/apisforcats`



<a href="#gitlessr" name="gitlessr">#</a> __If you like git, but aren't that familiar with R__

1. Fork <https://github.com/sckott/apisforcats> to your account
2. Clone down to your machine from your account
3. Add an upstream remote for the `sckott/apisforcats` repo by doing `git remote add upstream git@github.com:sckott/apisforcats.git`
4. Make a new feature branch
5. The only file to change is `index.Rmd`. It's a R markdown document, which is essentially just Markdown, so should be easy to add to/change. 
6. Commit changes and push to your account
7. Send a pull request to `sckott/apisforcats`



<a href="#nogit" name="nogit">#</a> __If you don't like git (or, _I don't know what git is_)__

1. Go to the [index.Rmd file](https://github.com/sckott/apisforcats/blob/gh-pages/index.Rmd) in the `apisforcats` GitHub repository
2. Edit whatever you want
3. Then write a message in the box at the bottom, and press the green button _Propose file change_. This will make a fork of the repo to your github account. You then can write any other message you want and press another green button _Send pull request_
4. The end!


<a href="#issue" name="issue">#</a> __Issues/bugs/questions/feature requests__

If you want to submit an issue (bug report/question/feature request/etc.), go to the [issues page](https://github.com/sckott/apisforcats/issues?state=open) and do that.

Thanks for contributing whether you or your cat wrote the code!!!!!


## <a href="#contributors" name="contributors">#</a> Contributors

### people

* Scott Chamberlain [@sckott](https://github.com/sckott)
* You?
