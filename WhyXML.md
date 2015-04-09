The philosophy is that you write your document once, and use your simple Python script to generate any output you want easily and reliably (no XSL stylesheets or similar mess).

Main points:

## simple ##

You can write any UTF-8 text that you want, including all special characters, accents, whatever, there are only two exceptions:

  * "<" needs to be written as "&lt;"
  * "&" needs to be written as "&amp;"

This means you no longer have to worry about escaping characters like "$", "\", "^" and you don't have to use some hard to remember markup for accented characters. You simply write UTF-8 (but you can use XML entities if you want, like "&ouml;" for "ö")

## easy to parse in a program ##

Because of the simple structure above, it's easy to parse and you can use standard tools for that in Python, e.g the `python-lxml` library.

Because the format is so simple, you will always be able to write a simple program to generate any output you want even 50 years from now using tools available then. If XML goes out of the fashion, you can easily convert it from XML to any other format, that will become the standard.

## content separation ##

You concentrate on content and let the converter handle the rest. The default converter
in `prettydoc` does a good job and you can customize it's output as easily as deriving a simple Python class.