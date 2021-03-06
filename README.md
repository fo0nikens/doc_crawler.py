`doc_crawler.py` can explore a website recursively from a given URL and retrieve, in the
descendant pages, the encountered document files (by default PDF, ODT, CSV, RTF, DOC and XLS)
based on their extension.

It can directly download found documents, or output their URL to pipe them somewhere else.

It can also be used to directly download a single file or a list files.

## Options
### `--accept`
Optional regular expression (case insensitive) to keep matching document names.

Example : `--accept=jpe?g`
Will hopefully keep all : .JPG, .JPEG, .jpg, .jpeg
### `--download`
Directly download found documents if set, output their URL if not.
### `--verbose`
Creates a log file to keep trace of what was done.
### `--wait`
Will wait that number of seconds before each download (page or document) if set.

Example : `--wait=5`
Will wait 5s before each download.
### `--random-wait`
Will randomly wait between 1 second and --wait seconds if set.
### `--download-file`
Will directly retrieve and write in the current folder the pointed URL.

Example : `--download-file url`
### `--download-files`
Will download files which URL are listed in the pointed file.

Example : `--download-files url.lst`

## Usage
`doc_crawler.py [--accept=jpe?g] [--download] [--verbose] [--wait=5] [--random-wait] http://…`

`doc_crawler.py [--wait=5] [--random-wait] --download-file http://…`

`doc_crawler.py [--wait=5] [--random-wait] --download-files url.lst`
