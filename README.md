# IAVD

> This website has been created to provide information about the project “Integrated Audio-Visual Documentation of Itelmen.” This is a collaborative endeavor between the University of Connecticut (Jonathan Bobaljik, PI) and the University of Alaska Fairbanks (David Koester, PI), with the further collaboration of Chiba University in Japan(Chikako Ono, PI). It inolves directly also Tatiana Degai (Ph.D. candidate, University of Arizona) and technical consultants and developers, Alexandre Arkhipov, Tom Myers, and Alexander Nakhimovsky. With funding from the National Science Foundation, the aim of the project is to integrate accumulated recordings of the Itelmen language with transcriptions into a digital corpus with additional linkages to Itelmen language.

## Design Overview
This site is currently written with the [Twitter Bootstrap](http://getbootstrap.com/) front end framework.
It also uses the [Modern Business](http://startbootstrap.com/template-overviews/modern-business/) theme.

For static HTML generation, we use [staticninja](http://staticjinja.readthedocs.org/en/latest/), because it is dead simple. All
we are really doing is re-including the `/templates/_base.html` in all the pages, so we don't have to retype
the header.

### How to run the HTML generator
```bash
// Using Fig
$ fig up -d
$ open "$(boot2docker --ip):8080"

// Using Docker
$ docker build -t iavd .
$ docker run --rm -v $(pwd):/usr/src/app/ iavd

// Not using docker
$ pip install -r requirements.txt
$ staticjinja build
```
