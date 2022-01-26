<div align="center">
    
<img src="https://raw.githubusercontent.com/ietf-tools/common/main/assets/logos/ietf-rfc-xmldiff-logo.svg" alt="IETF RFC-XMLDIFF" width="600" />
    
[![Release](https://img.shields.io/github/release/ietf-tools/rfc-xmldiff.svg?style=flat&maxAge=360)](https://github.com/ietf-tools/rfc-xmldiff/releases)
[![License](https://img.shields.io/github/license/ietf-tools/rfc-xmldiff)](https://github.com/ietf-tools/rfc-xmldiff/blob/main/LICENSE)
[![PyPI - Version](https://img.shields.io/pypi/v/rfc-xmldiff)](https://pypi.org/project/rfc-xmldiff/)
[![PyPI - Status](https://img.shields.io/pypi/status/rfc-xmldiff)](https://pypi.org/project/rfc-xmldiff/)
[![PyPI - Format](https://img.shields.io/pypi/format/rfc-xmldiff)](https://pypi.org/project/rfc-xmldiff/)

##### Create a difference on two RFC XML files

</div>

- [Changelog](https://github.com/ietf-tools/rfc-xmldiff/blob/main/CHANGELOG.md)
- [Contributing](https://github.com/ietf-tools/.github/blob/main/CONTRIBUTING.md)

---

This program takes two XML files containing SVG or RFC documents and creates an HTML file which shows the differences between the two documents.

The [RFC Editor](https://www.rfc-editor.org) is in the process of changing the canonical input format of [Internet-Draft](https://en.wikipedia.org/wiki/Internet_Draft) and [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) documents.  Further information on the process can be found on the RFC Editor at the [RFC Editor](https://www.rfc-editor.org) site.

## Usage

`rfc-xmldiff` accepts a pair of XML documents as input and outputs an HTML document.

### Basic Usage

```sh
rfc-xmldiff [options] SOURCE1 SOURCE2
```

### Options

The following parameters affect how rfc-xmldiff behaves, however none are required.

| Short         | Long                  | Description                                    |
|---------------|-----------------------|------------------------------------------------|
| `-C`          | `--clear-cache`       | purge the cache and exit                       |
| `-h`          | `--help`              | show the help message and exit                 |
| `-N`          | `--no-network`        | don't use the network to resolve references    |
| `-q`          | `--quiet`             | don't print anything                           |
| `-r`          | `--raw`               | don't use the xml2rfc vocabulary when matching |
| `-v`          | `--verbose`           | print extra information                        |
| `-V`          | `--version`           | display the version number and exit            |
| `-X`          | `--no-xinclude`       | don't resolve xi:include elements              |
| `-o FILENAME` | `--out=FILENAME`      | specify an output filename                     |
| `-t FILENAME` | `--template=FILENAME` | specify HTML template filename                 |
| `-D`          | `--no-defaults`       | don't load attribute defaults from the dtd     |
| `.`           | `--resource-url=URL`  | specify the URL for resources in the template  |

## Templates

Two template files are installed with the package:

- `single.html` - provides just the XML difference between the two files.
- `base.html` - provides three columns containing the left source files, the XML difference and the right source files. Uses color to highlight changes. This is the default template.
- `wdiff.html` - provides three columns containing the left source files, the XML difference and the right source files. Uses color and strike throughs to highlight changes.

For new template files, the following variables are define:

- `title` - provides a default window title
- `body` - contains the XML difference HTML
- `leftSourceNames` - the list of all input files for the left sources
- `leftFile` - contains the left source files
- `rigthSourceNames` - the list of all input files for the right sources
- `rightFile` - contains the right source files
- `resource_dir` - contains the URL to find the resources. This defaults to the Template directory of the package.
- `allScript` - contains the contents of `resize.js` so the resulting html file is self contained.

## Dependencies

`rfc-xmldiff` depends on the following packages:

- [lxml](http://lxml.de) *(>= 4.1.1)*
- [requests](http://docs.python-requests.org) *(>= 2.5.0)*
- [rfctools_common](https://pypi.python.org/pypi/pip) *(>= 0.5.10)*
- [cffi](https://pypi.python.org/pypi/pip) *(>= 1.0.0)*
