{:title "Clojure and data: wishes, problems, and ideas"
 :layout :post
 :toc true
 :author "Sami Kallinen, Konrad Kühne, Daniel Slutsky"
 :tags  ["community"]}

On Sunday afternoon, Sep. 29th 2019, we had a meeting at the 8-bit-sheep office of Sami at [Maria 01](https://maria.io/about/), Helsinki. One hour earlier, Konrad just finished participating in a 24h [opendata hackathon](https://www.meetup.com/Lamia-hackathons/events/264053121/). We were all tired and emotionally affected by [ClojuTRE](https://clojutre.org/2019/), that just ended on Friday.

We ended up having a long conversation about our goals and wishes, as individuals and as parts of a community. A lot of personal stories and wild ideas were running in the room. Later Sami took us on a ride around Helsinki, which opened our tired minds even wider.

This blog post is a brief summary of those parts of the conversation that relate to building the Clojure data science community. Hopefully, the list of problems and ideas that we offer here can serve as an actionable suggestion, as well as a beginning of a wider discussion. 

For the actionable part, you are invited to jump to the [Goals](#goals) section below. Hopefully, the parts preceding it are useful too.

Sami Kallinen, Konrad Kühne, Daniel Slutsky


## TL;DR

We discussed some of the challenges of an expanding community, and suggested some concrete projects to tackle some of these challenges:

* Tooling. Have more meetings to learn and discuss existing Clojure tooling projects, with the focus of the question of friendliness to data analysts.

* Experimental meetings. Have a variety of experimental meetings that expose Clojure to other communities.

* Learning materials. Consider writing a 4Clojure4Data project.

* Team building. Start thinking about a study group with friends from other communities.

* Face-to-face. Check the option of organizing a big meetup near ClojureD.

* Discussion. Keep discussing the broader dilemmas suggested here.

## Wishes

Sami and Daniel shared the wish for Clojure to become more accessible to wider groups of people, especially beginners, in particular data analysts.

Konrad added the wish to have more community activity around data analysis (rather than just building tools and libraries); to develop Datalog as a way of expressing queries; and to promote activity around open source and open data.


## Personal experiences

Sami shared some of his experience in group facilitation, and described different models of learning meetings, with different variations around the Coding Dojo idea.

Konrad told about his development efforts in the ecosystem around Datalog, and about the challenge of creating cooperation across different groups working on Datalog-related libraries.

Sami and Konrad shared similar experiences about building professional groups that are dispersed across different locations, and mentioned the challenges of keeping group communication continuous in such conditions.

Daniel told about the attempt to create a local Clojure data science workshop. The workshop began with some fun talks and discussions, and a diverse group of speakers and participants. However, it failed to actually create a continuous learning experience. Gradually, it converged to a less diverse group of people.

We also discussed the growth of the Scicloj community so far. It began as an intimate, small group of people who were very involved and all influenced the thought process and directions. The group tried to expand, and gradually more people started taking part in the process. However, in the current dynamics, many members do not get to practically influence the goals and directions of the group.

## Challenges

### Accessibility

Once central question we discussed was whether Clojure could become a beginner-friendly tool in the field of data analysis.

Will we reach a state where newcomers can easily find clear Clojure paths to solve the data problems that they face? 

### Convergence

A related problem is the so-called [Lisp Curse](http://www.winestockwebdesign.com/Essays/Lisp_Curse.html), where many individuals and groups tend to enjoy the flexibility of the language and create their own flavours of methods and solutions, thereby often diverging from widely-accepted practices. Of course, this also means lots of creativity, and many opportunities for beautiful things to happen. However, being able to converge to common practices might be important.

For actual beginner-friendliness to arise, probably some clear main paths would rather be marked. Moreover, convergence around popular, well accepted ways seems essential to allow for the critical mass that enables enough questions and answers, enough tutorials, etc.

Also, for the ecosystem to get far enough as a platform for data science, it seems important for libraries to be able to build upon each other. 

### Cooperation

One expression of that tendency, not to converge to common practices, can be seen in the fact that it seems uncommon for Clojure libraries to use abstractions defined by others. 

In the field of data science and scientific computing, there have been some opposite tendencies.

One notable case has been the use of the [core.matrix](https://github.com/mikera/core.matrix) abstractions in several libraries (and the communication around those in the [Numerical Clojure forum](https://groups.google.com/forum/#!forum/numerical-clojure)). There are now some tendencies to replace the core.matrix set of protocols by those of [tech.datatype](https://github.com/techascent/tech.datatype) and [tech.ml.dataset](https://github.com/techascent/tech.ml.dataset) (ironically exercising The Curse once again, but inspired by the ideas and lessons of the core.matrix story). In the Scicloj activity and [discussions](https://clojurians.zulipchat.com/#narrow/stream/151924-data-science/) around these, we intend to use them as a common basis for some of the emerging libraries. Indeed, the explicit [intention](https://clojureverse.org/t/online-meeting-clojure-data-science/3503/17) behind the 'tech' stack is to support building bridges in our ecosystem, as well as bridges across ecosystems.

A related example of libraries building upon each other is a collection of libraries written by a single author, Tomasz Sulej. [Fastmath](https://github.com/generateme/fastmath), [Clojure2d](https://github.com/Clojure2D/clojure2d), [Cljplot](https://github.com/generateme/cljplot), [Fitdistr](https://github.com/generateme/fitdistr), [Inferme](https://github.com/generateme/inferme), etc. are very much interrelated.

Another cooperation potential is around Datalog. Here, Konrad tells about the intention to create cooperation across the different groups developing Datalog libraries, and about the actual [efforts](https://lambdaforge.io/2019/09/20/datahike-release-0.2.0.html) to decouple [some parts](https://github.com/lambdaforge/datalog-parser) of Datahike, so that they can be useful in a wider context.

One potential cooperation that has not become fruitful yet is the discussion of document formats. Martin Kavalar of Nextjournal [suggessted](https://clojurians.zulipchat.com/#narrow/stream/187445-scicloj-tutorials/topic/Runnable.20tutorials) to have some dialogue about the definition of import/export formats for various literate programming tools. This is relevant to several projects that have some notion of document-with-code, such as [Marginalia](https://gdeer81.github.io/marginalia/), [Gorilla-REPL](http://gorilla-repl.org/), [Maria.cloud](https://www.maria.cloud), [Clojupyter](https://github.com/clojupyter/clojupyter), [Saite](https://github.com/jsa-aerial/saite) and [Oz](https://github.com/metasoarous/oz). Some conversation has started, without conclusion yet.

### Growth

How can we reach out to more people? What would actually encourage people to get involved? And what paths can we offer people to get involved?

### Diversity

Diversity in our community is a goal in itself.

It is also related to several of the other problems mentioned here.

As Jack Rusher commented in one of our ClojuTRE chats, experienced Clojurians are not so much in a position to see what is actually necessary to make Clojure easy to non-experienced Clojurians. If we wish to have a team that works on making things accessible, it ought to be more diverse.

### Democracy

Democracy can mean different things, in particular in the context of open-source communities.

In our context, we should ask at least that the goals, the directions and the spirit of our community will be effectively influenced by its members, and be effectively transparent to them. This should be true not only for those who are privileged to be involved every day. It is important that those who are limited in time and are less involved will be influential and well-informed too.

Our current experience shows that intentions, declarations and efforts are not always enough to achieve that.

Power relations exist, even if we do not wish them to. They are partly caused by the fact that community members are different in their availability of free time, their background, their convenience about language, their involvement in related processes in the past, their timezone, all kinds of glass ceilings, etc. Such differences sometimes affect the ability of members to affect certain processes, and even to be aware of them.

Of course, the question of power relations becomes even more relevant and problematic when we seek to expand our team with people who are of different backgrounds, and specifically, of little Clojure background.

We want to be a living community, not a small group that drives things by inertia.

### Community

Very much related to the above question of power and participation, is the question whether community members actually feel that the community is theirs, and that it is a thing they are building.

In the case of Scicloj, so far about 20 people have agreed to be part of the organizing team and be minded about the community building story. But even for those who have actively decided to be in that standpoint, is the door actually open? Is it convenient enough to participate? And does the general atmosphere allow everybody to feel at home?

### Team building

We wish to create a more diverse team of people who will be involved in our agenda.

Of course, it might be problematic to diversify the team, if we are not willing to expand the agenda itself.

Currently, we are a group of Clojurians who dream of bringing Clojure to people of different backgrounds. As we realize, to actually grasp this dream and understand the problems around it, we need people of different backgrounds in the team. But let us remember, that a more diverse team may of course have more diverse dreams. Keeping the goal concentrated around one culture, with the team containing several other cultures, might create an imbalance and unwanted power relations across members.

How should we tackle this paradox? Can we create a diverse team of members who work together towards a common agenda, where the agenda is balanced with respect to the backgrounds, dreams and wishes of team members?

And can we create such a team in a way that would at least be related to our current, narrower goals as Clojurians?

### Continuity

Processes are happening in parallel. Libraries are developed; ideas are raised and wait to be implemented; meetings are planned; series of meetings begin, stop and continue; discussions begin, stop and continue; decisions wait to be made.

Some of these take time. There is always a danger to lose some threads, and also to lose some of the members involved, as they may not be available when things actually continue.

Our job is to glue things together, so that the activities, their fruit and the people around them will keep going, as much as possible.

The answer to this may be partly about careful knowledge management and task management. But it is also about relationships between people.

Here we might draw some lessons from Sami's and Konrad's experience in building managing groups of people divided across multiple locations. As Sami says, it is important for team members have to actually look into each other's eyes once in a while. Even maintaining that is a challenge.

### Meeting up

This brings us to the following question: how can community members meet?

Face-to-face meetings are important. Local communities are important too. Connecting across localities is important too.


## Goals

As a way to cope with the challenges discussed above, we offer the following concrete goals.

### Better ecosystem

This has been and will be discussed in length elsewhere. But let us mention it, at least: we agree that there is a lot to be built on the technical side, until Clojure actually becomes friendly and comfortable for beginners.

### Tooling

Another topic that would be discussed elsewhere is the creation of beginner-friendly tooling.

[Maria.cloud](https://www.maria.cloud) is an example of a project of this kind of spirit, but at the moment it does not target specifically data analysts. [Rstudio](https://rstudio.com) could be another possible direction. Several of the other emerging tools, such as [Clojupyter](https://github.com/clojupyter/clojupyter), [Saite](https://github.com/jsa-aerial/saite) and [Oz](https://github.com/metasoarous/oz), can hopefully also go in that direction and gradually offer transparency and ease to beginners.

We suggest at least to create some more learning and discussion around these existing projects, while stressing the explicit goal of making things friendly for data analysts.

### Experimental meetings

We need to constantly challenge ourselves and the ecosystem we are building: How accessible is it? Where are the main obstacles? What could be done to improve? To do that, we need to expose ourselves, and to expose Clojure, to diverse groups of people.

We suggest to start a series of meetings that will experiment with different ways of doing that. Following Sami's experience in similar situations (such as teaching groups of young people to program), we discussed different variations of such meetings:
- tutorials about data analysis with clojure 
- facilitated discussions
- "Just open a REPL" and play with some data

Different formats of group coding could be used. Variating on the idea of "coding Dojo", typically there is one "driver" with the REPL or editor, and one or more "navigators", who say what is to be done. One may also think about multiple people remotely affecting the same REPL or editor.

Different combinations of online and physical meetings might be considered. One possible idea is to conduct several concurrent local meetups in different locations, with an online communication between them.

Some meetings can be somewhat internal community meetings; other can reach out and invite curious people who are willing to hear. 

One possibility would be to create a series of meetings that build up some body of knowledge. Another mode would be of singular meetings, that may touch a topic without continuation.

### Learning materials for data analysts

We need to create materials that will allow for more-or-less independent learning, as well as for efficient teaching.

One suggestion is "4Clojure4Data" -- something like [4Clojure](https://github.com/4clojure/4clojure), but with data analysis problems.

### Team building: a study group

As mentioned in the challenges above, we wish to create a diverse team working towards some common agenda, balanced around the backgrounds, dreams and wishes of its members; and we wish that team to be at least related to our own, narrower wishes.

One format we suggest to try in this direction is a study group: a forum of people of several backgrounds (say, R, Julia and Lisp in terms of programming languages), who go on a long-term journey to study some topic together.

One possible topic could be a comparative study of languages (say, meeting to analyse some data, and doing it in more than one way).

Another possible topic could be something that is relevant to everybody, but is maybe less known to most of them. The field of probabilistic programming could be a good choice.

### Face-to-face

We suggest to organize face-to-face meetups of the community.

We actually tried that with a [meetup](https://www.meetup.com/Helsinki-Clojure-Meetup/events/264887242/) the day before ClojuTRE, with the kind help of the Clojure Helsinki meetup group, the ClojuTRE organizers and the host Emblica.

Now, we wish to have something longer, broader, and more carefully planned.

We suggest to plan a 1-day meetup close to one of the upcoming Clojure conferences, and encourage the Clojure data science community to arrive on that day. 

Probably, taking into account the locations of most people currently involved, we need to try that once in Europe and once in the US. One of the close-but-not-too-close opportunities is [ClojureD](https://clojured.de), on Feb. 29th, 2020.

## Summary

Here are the concrete projects we are suggesting at the moment.

* Tooling. Have more meetings to learn and discuss existing Clojure tooling projects, with the focus of the question of friendliness to data analysts.

* Experimental meetings. Have a variety of experimental meetings that expose Clojure to other communities.

* Learning materials. Consider writing a 4Clojure4Data project.

* Team building. Start thinking about a study group with friends from other communities.

* Face-to-face. Check the option of organizing a big meetup near ClojureD.

* Discussion. Keep discussing the broader dilemmas suggested here.

## Conclusion

Very few days after ClojuTRE, Helsinki finally got some snow. Some of us were already too far to feel it, and could only hear about it through the Slack channel.

In the few days around the conference, people could feel and see each other. Many important little conversations took place. Most of them cannot be written in blog posts, but have probably had their effects in other ways.

In this rant we tried to capture some of the thoughts of one conversation.

To us, it was an opportunity to experience how important and transformative a face-to-face meeting can be.

Let us hope we can now somehow continue the discussion in a wider forum, across continents, climates and timezones.


## Recommended reading

We wish to thank Daniel Szmulewicz for recommending to look into Pieter Hintjens' writings. In particular, the ideas presented in [Building Online Communities](http://hintjens.com/blog:117) may trigger some thought around the dilemmas we are discussing here.

