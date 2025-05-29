---
permalink: /
title: "Dr. Mike Sosteric"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
Greetings and welcome. My name is Mike. I am an Associate Professor of Sociology at Athabasca University (AU). PhD. from the University of Alberta, Masters from University of Regina. At AU I coordinate [introductory sociology](https://www.athabascau.ca/syllabi/soci/soci287.html), the [sociology of religion](https://www.athabascau.ca/syllabi/soci/soci231.html), [statistics](https://www.athabascau.ca/syllabi/soci/soci301.html), [introduction to social movements](https://www.athabascau.ca/syllabi/soci/soci288.html), and the [sociology of information technology](https://www.athabascau.ca/syllabi/soci/soci460.html).  In the past I have been created and coordinated theories of social change (Sociology 435) and Canadian society. 

In addition to all that course work, I do a little bit of publication in scholarly journals (THB, just enough to get by) and a lot of writing, editing, revising, and shaping the things I've already written. I also spend a lot of time thinking about how to organize everything, and a lot of time reorganizing, particularly as information technology has evolved, organizing things. The organizational component is a big thing and has taken a lot of time. I retain my sanity by always focusing on the improvements and never spending too much time on the tasks ahead. If I did that I'd surely lose all hope.

## Early Career

I started my career off interested in typical sociological things like the Labour Process, inequality, and gender.  In my third year of 

Coincidentally, I entered the PhD program at about the same time that the Internet and the World Wide Web were beginning to enter public consciousness. The WWW lowered publication entrance barriers. Basically anybody with a computer and a bit of tech-savvy could publish a paper, a journal, or whatever. Being a budding scholarly-type, I saw an opportunity to publish a scholarly journal, and so that is what I did. I created the worlds very first electronic journal of sociology named, appropriately enough, the [Electronic Journal of Sociology](https://en.wikipedia.org/wiki/Electronic_Journal_of_Sociology). 

My dissertation was on the political economy of scholarly communication. with a bit of a bang, publishing an article in the a top tier academic journal without first submmission, no revision request. 

The main configuration file for the site is in the base directory in [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml), which defines the content in the sidebars and other site-wide features. You will need to replace the default variables with ones about yourself and your site's github repository. The configuration file for the top menu is in [_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml). For example, if you don't have a portfolio or blog posts, you can remove those items from that navigation.yml file to remove them from the header. 

Create content & metadata
------
For site content, there is one markdown file for each type of content, which are stored in directories like _publications, _talks, _posts, _teaching, or _pages. For example, each talk is a markdown file in the [_talks directory](https://github.com/academicpages/academicpages.github.io/tree/master/_talks). At the top of each markdown file is structured data in YAML about the talk, which the theme will parse to do lots of cool stuff. The same structured data about a talk is used to generate the list of talks on the [Talks page](https://academicpages.github.io/talks), each [individual page](https://academicpages.github.io/talks/2012-03-01-talk-1) for specific talks, the talks section for the [CV page](https://academicpages.github.io/cv), and the [map of places you've given a talk](https://academicpages.github.io/talkmap.html) (if you run this [python file](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.py) or [Jupyter notebook](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb), which creates the HTML for the map based on the contents of the _talks directory).

**Markdown generator**

The repository includes [a set of Jupyter notebooks](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator
) that converts a CSV containing structured data about talks or presentations into individual markdown files that will be properly formatted for the Academic Pages template. The sample CSVs in that directory are the ones I used to create my own personal website at stuartgeiger.com. My usual workflow is that I keep a spreadsheet of my publications and talks, then run the code in these notebooks to generate the markdown files, then commit and push them to the GitHub repository.

How to edit your site's GitHub repository
------
Many people use a git client to create files on their local computer and then push them to GitHub's servers. If you are not familiar with git, you can directly edit these configuration and markdown files directly in the github.com interface. Navigate to a file (like [this one](https://github.com/academicpages/academicpages.github.io/blob/master/_talks/2012-03-01-talk-1.md) and click the pencil icon in the top right of the content preview (to the right of the "Raw | Blame | History" buttons). You can delete a file by clicking the trashcan icon to the right of the pencil icon. You can also create new files or upload files by navigating to a directory and clicking the "Create new file" or "Upload files" buttons. 

Example: editing a markdown file for a talk
![Editing a markdown file for a talk](/images/editing-talk.png)

For more info
------
More info about configuring Academic Pages can be found in [the guide](https://academicpages.github.io/markdown/), the [growing wiki](https://github.com/academicpages/academicpages.github.io/wiki), and you can always [ask a question on GitHub](https://github.com/academicpages/academicpages.github.io/discussions). The [guides for the Minimal Mistakes theme](https://mmistakes.github.io/minimal-mistakes/docs/configuration/) (which this theme was forked from) might also be helpful.
