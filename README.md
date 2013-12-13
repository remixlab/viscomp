# VisComp

*Visual Computing* slides for the course of the same name given at [National University of Colombia](http://www.disi.unal.edu.co/) by [Jean Pierre Charalambos](http://otrolado.info) and [Andres Colubri](http://codeanticode.wordpress.com/).

Powered by [reveal](https://github.com/hakimel/reveal.js).

Made possible thanks to... 

<!--- a long list of students and links to their pages. To come ;) -->

## Folder Structure

    |-- css/
    |-- js/
    |-- plugin/
    |-- lib/
    |-- lectures/
    |   |-- 1
    |       |-- fig/
    |       |-- index.html
    |       |-- source.md
    |   |-- ...
    |       |-- fig/
    |       |-- index.html
    |       |-- source.md
    |   |-- template
    |       |-- fig/
    |       |-- index.html
    |       |-- source.md
    
Refer to [reveal folder structure](https://github.com/hakimel/reveal.js#folder-structure) for more details, and to the *Setup* below.


## Setup

External markdown and speaker notes, require that presentations run from a local web server. The following instructions will set up such a server as well as all of the development tasks needed to make edits to the slides source code.

1. Install [Node.js](http://nodejs.org/)

2. Install [Grunt](http://gruntjs.com/getting-started#installing-the-cli)

4. Clone the VisComp repository
```sh
$ git clone https://github.com/nakednous/viscomp.git
```

5. Navigate to the viscomp folder
```sh
$ cd viscomp
```

6. Install dependencies
```sh
$ npm install
```

7. Create a presentation
```sh
# replace *n* with the number of the presentation to be created:
$ cp -r lectures/template/ lectures/n
# uncomment lines 49-55 (section block) and edit line 50 to reflect *n* above:
$ nano lectures/n/index.html
# edit the presentation source using markdown:
$ nano lectures/n/source.md
$ ln -s lectures/n/index.html index.html
```
*Note:* `lectures/1` followed the aforementioned method.

8. Serve the presentation and monitor source files for changes
```sh
$ grunt serve
```

9. Open <http://localhost:8000> to view your presentation

You can change the port by using `grunt serve --port 8001`.
