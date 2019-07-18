# Source of the Scicloj website

## What is this?
The [Scicloj website](https://scicloj.github.io/) is hosted on Github Pages [here](https://github.com/scicloj/scicloj.github.com). 


It is written using [Cryogen](http://cryogenweb.org/) in [this repo](https://github.com/scicloj/scicloj) using [this workflow](https://tangrammer.github.io/posts/02-12-2014-cryogen-and-github.html).

## Development
To develop this locally, try `lein ring server`, and open the browser at http://localhost:3000/.

To publish an update to Github Pages, you can use the convenience script `./publish`.

## Knowledge Management
The default branch at this github repo is `drafts`. 

Everybody are invited to push their knowledge into that branch. The place to put that knowledge is the directory of markdown pages at [./resources/templates/md/pages](./resources/templates/md/pages). These correspond to pages in the website.

If you wish to be able to push to this repo, contact <scicloj@gmail.com>.

Every once in a while, the editor (from the scicloj-website task group) will tidy up the knowledge in pages, merge into `master` and publish to the website. In that process, knowledge may pass some cleanup and standardization, move across pages, etc. 

## License

Copyright © 2019 Scicloj

Distributed under the Eclipse Public License.
