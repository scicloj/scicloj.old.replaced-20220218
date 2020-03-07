{:title "Meeting Video: Guix-Jupyter with Ludovic Courtès"
 :layout :post
 :toc false
 :author "Daniel Slutsky"
 :tags  ["reproducibility" "notebooks"]}

A lot has been happening at Scicloj in the last few weeks, but now we finally managed to edit and publish the video from a meeting we've had at January 9th.

It was a special meeting, as we the topic was something out of the ususal Clojure scope: Guix-Jupyter reproducible notebooks.

Kindly, Ludovic Courtès of the Guix community agreed to give a talk at this scicloj web meeting, and have a discussion with us.

Here are [the video](https://youtu.be/GFyv3qUXHpU) and [the slides](https://github.com/scicloj/scicloj/blob/master/resources/slides/scicloj-guix-jupyter.pdf).

Now, let us discuss what it is about.

## Guix

[GNU Guix](https://guix.gnu.org/) is a unique toolbox for Linux package management, as well as a Linux distribution. It is built on principles of Functional Programming, inspired by [Nix](https://nixos.org/nix/), and is written and configurable in GNU Guile, a dialect of Scheme. Functional package management has beautiful implications in enabling systems which are secure, transparent and reproducible.

Recently, the Guix community started the [Guix-HPC](https://gitlab.inria.fr/guix-hpc) project, that brings these principles to the field of scientific computing. Specifically, the [Guix Jupyter kernel](https://gitlab.inria.fr/guix-hpc/guix-kernel) allows Jupyter users to specify their precise software dependencies as Guix dependencies.

Ludovic, who is a research engineer at [Inria Bordeaux Sud-Ouest](https://www.inria.fr/fr/centre-inria-bordeaux-sud-ouest), has been active both in academic research and in libre software. Some of his involvement has been in the Guile, Guix and Guix-HPC projects.

At the scicloj, we are minded about various aspects of reproducible deployment and reproducible research. Of course, we also love Functional Programming and curious about Scheme. So, a whole meeting about Guix-Jupyter would naturally be inspiring and joyful for us.

## The meeting

In the meeting we have had several participants from the Guix community and from the Scicloj community.

It was the first time for us to use an open-source video-conferencing tool, [Jitsi](https://jitsi.org/). This was a little step outside of our comfort zone, and so some small parts of the discussion are missing in the recorded video.

We began with a talk, where Ludovic gave a general introduction to Guix and reprocibility, as well as a demonstration of Guix-Jupyter.

Then, we moved to an open discussion. A nice conversation emerged, with three of the participants: Martin Kavalar, the CEO of [Nextjournal](http://nextjournal.com/), a web notebook built on principles of immutability and reproducibility; Klaus Harbo, who is, among other things, the maintainer of [Clojupyter](https://github.com/clojupyter/clojupyter), a Clojure Jupyter kernel; and Daniel Szmulewicz, who has been studying various dialects of Scheme, and builds Clojure development tools on top of the Maven ecosystem.

We discussed some technical aspects and usability aspects of Guix, as well as some conceptual questions. Interesting dilemmas arise when the Guix approach towards libre software, pure functions, reproducibility, security and transparency is used alongside other pieces of software. We also discussed some issues of possibly bringing Clojure ecosystem more fully into the Guix ecosystem. 

## Thanks!

Many thanks to Ludovic and the other Guix community members who kindly joined us at Scicloj for this meeting!

See you on the next meetings.
