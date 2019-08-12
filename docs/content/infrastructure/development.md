# Notes for developers

## Testing installation

Once you have successfully installed the `gds` environment using 
`install_gds_stack.yml`, you can
programatically test the installation using the
`nbconvert` utility. 
You can run it from this folder as follows :

> jupyter nbconvert --execute --stdout check_gds_stack.ipynb

Which will run it and print the output into the command line. 

Alternatively, you can also run it using the project's `Makefile`:

> make test_stack

## Tweaking CSS theme for html slides

Modifications to the original theme can be done using `reveal.js` custom theme
support. You will need the development setup (`node.js` and `grunt`). Follow
instructions in reveal.js [Github](https://github.com/hakimel/reveal.js). Once
setup, change the theme by:

* Edit the source file (`.scss`).
* Run `grunt css-themes`.
* Copy the resulting `.css` file into the course project.

## Converting html slides to pdf

Conversion is automated by using
[`decktape`](https://github.com/astefanutti/decktape). In particular,
`darribas`'s fork contains an additional utility script that allows the
conversion through the Makefile. To get the fork working, follow these steps:

* Clone the [fork](https://github.com/darribas/decktape).
* Follow install instructions.
* Add the `decktape` folder to your system path so the executable `decktape`
  inside the folder can be called.

Note the executable is a Python script, so you'll need a basic Python
distribution installed.

## Running the website locally

The website is build on Jekyll, so running it on a local server requires the following dependencies:

* [Jekyll](http://jekyllrb.com)
* [jekyll-scholar](https://github.com/inukshuk/jekyll-scholar)

