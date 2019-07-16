[![Build Status](https://travis-ci.org/pl-ds-dict/pl-ds-dict.github.com.svg?branch=source)](https://travis-ci.org/pl-ds-dict/pl-ds-dict.github.com)

## English-Polish Data Science dictionary / Angielsko-polski słownik Data Science

This is the source code behind the site: https://pl-ds-dict.github.io/

#### Goals of the project

- gather Polish equivalents of Data Science-related terms **already being used**
- discuss and determine best practices - what to translate and how

#### TODO

This project is in a very early stage. Pull requests are preferred to criticism.

Other than adding new words and improving old ones, the following issues seem to
be important:

- improving the layout - better placement of things, aesthetics, etc. Knowledge
of Hugo might be useful - e.g. maybe the `ananke` theme is not necessary?
- adding some JS to make the table searchable and sortable (purely client-side)


#### Why not just use English terms everywhere?

In many cases we should use English terms, clearly. `Dropout` is Dropout, no
translation required (or possible). This project does not intend to promote
weird translations or coming up with any new ones.

On the other hand, sentences that with too many English words are hard to
read, sometimes unacceptable for formal reasons (academia, bureaucracy).
Besides, Polish terms are already in use. Sometimes they fit well and we should
use them. Why use `neural net` or `random forest` in a foreign language?
And sometimes people use strange Polish translation - maybe this site
can help decode them.


#### How this site works

It is based on [Hugo](https://gohugo.io/), a static page generator. There is
one page per term. They are searchable in a big table, but each has its own page
with additional information and comments. Comments are attached to
auto-generated GitHub issues. Issues are created when the first comment is
added for each page.

** The default branch of this repo is `source`.** The `master` branch
contains the html files resulting from a build. Such a setup is necessary, as
GitHub User Pages can only be served from the `master` branch.

#### How to run it locally

After cloning the repository, simply run `hugo server`. The site will be
available at `http://localhost:1313/`.

To build the static version, simply run `hugo`. It will generate the `public`
directory.

**Please do not commit the `public` directory to the repo. The online version
is being built automatically, it is enough to edit the appropriate `.md` file
and send a pull request**

#### How to contribute

You can contribute to the discussion in the comments under each word
(and equivalently - issue).

Pull Requests modifying existing content or adding something new are very
welcome! If modifying a file please mention the relevant issue.

If you want to add a word, please create a new file in `content/dict_entries`,
e.g by clicking [here](https://github.com/pl-ds-dict/pl-ds-dict.github.com/new/source/content/dict_entries).

Current template:
```
---
title: "Some English term"
abbreviations: "SET"
recommended_translation: "Najlepsze tłumaczenie"
other_translations: "Gorsze tłumaczenie, Najgorzej"
---
Any additional information, including **markdown**. Maybe a video interview
with a linguist?
```

The first section, between the triple dashes, is in YAML. After that, there
is some extra space for (optional) additional information. That part is in
Markdown.

##### Why is this README in English?

To accommodate the very unlikely person who would like to fork this project
for use in another language.
