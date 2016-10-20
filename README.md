md2dict
===============================================================================

As part of developing awesome list importer, md2dict reads markdown pages and
generates python dict data structure. With this, markdown awesome list will be
imported to python in dict.

First approach is simple.
we expect to see a markdown file in this format:

```
	# title
	description

	# section header 1
	## subsection header
	- [name](url) - description
	
	# section header 2
	## subsection header
	- [name](url) - description
	  - [name](url) - description
	- [name](url) - description
```

which will be converted to:

```

	{ title:
		{ section header 1:
			{ subsection header:
				[ { name: url } ]
			}
		{ section header 2:
			{ subsection header:
				[ 
				{ name: url },
				{ name: url } 
				]
			}
		}
	}
``

See example directory for the first results.



