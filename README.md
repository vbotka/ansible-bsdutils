bsdutils
=======

[![Build Status](https://travis-ci.org/vbotka/ansible-bsdutils.svg?branch=master)](https://travis-ci.org/vbotka/ansible-bsdutils)

[Ansible role.](https://galaxy.ansible.com/vbotka/bsdutils/) Install and configure bsd-utils from https://github.com/vbotka/bsd-utils.


Requirements.
------------

None.


Role Variables.
--------------

lib-mapgen is not enabled by default.

```
libmapgen_enable: "no"
libmapgen_cron_enable: "no"
```

TBD (Check defaults).


Dependencies.
------------

None.


lib-mapgen
----------

Map library links and generate libmap.conf to fix potentially broken links. Optionaly run it from the cron.

```
lib-mapgen [-V|--version] [-h|--help] [-s|--silent] [-d|--debug]
           [-l|--list] [-a|--ansible] [-m| --libmap] [-ma|--libmap-append]
	              -- Map library links and generate libmap.conf

where:
-V  --version .......... print version
-h  --help ............. show this help
-s  --silent ........... print errors only
-d  --debug ............ print debug output
-l  --list ............. list broken links
-a  --ansible .......... list broken links in yaml array format
-m  --libmap ........... list only broken links missing in $LIBMAP
-ma --libmap-append..... append broken links to $LIBMAP

Examples:
List broken links in $LIBDIR
# lib-mapgen  -l
List broken links in $LIBDIR in yaml array format
# lib-mapgen  -a -l
List broken links in $LIBDIR not fixed in $LIBMAP
# lib-mapgen  -m
List broken links in $LIBDIR not fixed in $LIBMAP in yaml array format
# lib-mapgen  -a -m
Append broken links to $LIBMAP
# lib-mapgen  -ma
```


License.
-------

[![license](https://img.shields.io/badge/license-BSD-red.svg)](https://www.freebsd.org/doc/en/articles/bsdl-gpl/article.html)


Author Information.
------------------

[Vladimir Botka](https://botka.link)
