# nanoc-template

My basic template for building sites using [nano](http://nanoc.stoneship.org/), including [HAML](http://haml-lang.com/), [SASS](http://sass-lang.com/), and [Markdown](http://daringfireball.net/projects/markdown/).

## Author

Cameron Desautels, <camdez@gmail.com>, [camdez.com](http://camdez.com)

## To Do

- Automatically minify scripts & CSS, but probably copy both versions over. But this should really be conditional on the whether this is production or dev.  Need to build that system into place.
- Do we really need to have the relativize paths stuff scattered around?  Is it enough to just change the `items_root` in the config.yaml file?  And if so, can that me done based on production/dev environment?
- Break out HAML options to a separate file.  Shouldn't be too hard. Look at the way it's done for Compass.  Just write a method to read a config file, run that from lib/haml.rb, and have a method that returns a hash of options to pass to `layout` (which gets passed to HAML).  If I do this, create a separate config/ directory for the configuration files.
- Rework the `nanoc create_item foo` concept to do something useful. I believe it actually does cool stuff like adding the created file to version control.
- Parameterize stuff like site name?  Helpers for copyright, current year?

## Resources

- http://stackoverflow.com/questions/2386014/is-it-possible-to-set-different-sass-output-style-for-development-and-production
- http://github.com/ddfreyne/nanoc/blob/master/lib/nanoc3/filters/haml.rb