## Jekyll Quickstart

A default directory structure for a [Jekyll](https://github.com/mojombo/jekyll) site, suitable for rapid prototyping.

Clone and go.

## Features

  * Ready to use config file for [Compass](http://compass-style.org)
  * Simple "rake watch" task to run the Jekyll server and start the Compass poll process.
  * Rackup file to easy integration with [Pow](http://pow.cx/)

## Workflow

For ideal system intregation, create an alias in your .bash_profile:

`alias jekyll-create='git clone https://github.com/mikefowler/jekyll-quickstart.git'`

With the alias in place, get a prototype up and running quickly with the following steps:

```
jekyll-create mySite
cd mySite
rake watch
```

Jekyll's server will be up and running at http://localhost:4000.