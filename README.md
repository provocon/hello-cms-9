# Configurable Hello World Content

A Hello World content set as a minimal demo site or a starting point to set up 
a new site in an otherwise empty system.

Of course global base content and themes must be available and the theme in use 
defaults to the `corporate-theme`.

The Corporate Site Demo content may reside next to this.


## Configure Content

The content for even the smallest Site needs to have the following items set

* A base name - "Hello World" as a default in this case
* A locale - we chose the de-DE for this example
* A base path - /Sites/HelloWorld as our default

So alongside with the content describing files, this workspace contains the
tooling to prepare base names, locales and base folders before packaging
the then modified content into an archives which later can be easily imported
with the usual "serverimport" into the Content Management Server.


## Usage

Just the defaults for a site residing in `/Sites/HelloWorld`:

```
gradle build
```

Modify the locale to english in the US:

```
gradle -Plocale=en-UE build
```

This doesn't change the content but the locale setting in each of the 
documents.

Also the paths can be modified:

```
gradle -Pcontentpath=HelloWorld/UnitedStates/English build
```

Of course the prefix /Sites is constant.

Likewise the site Code and Title can be changed:

```
gradle -Ptitle="Hello Globe" build
```
