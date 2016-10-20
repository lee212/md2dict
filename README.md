md2dict
===============================================================================

As part of developing awesome list importer, md2dict reads markdown pages and
generates python dict data structure. With this, markdown awesome list will be
imported to python in dict.

First approach is simple.
we expect to see a markdown file in this format:

``
	# title
	description

	# section header
	## subsection header
	- [name](url) - description
