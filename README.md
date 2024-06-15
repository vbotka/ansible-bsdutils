# bsdutils

[![quality](https://img.shields.io/ansible/quality/27910)](https://galaxy.ansible.com/vbotka/bsdutils)
[![Build Status](https://travis-ci.org/vbotka/ansible-bsdutils.svg?branch=master)](https://travis-ci.org/vbotka/ansible-bsdutils)
[![GitHub tag](https://img.shields.io/github/v/tag/vbotka/ansible-bsdutils)](https://github.com/vbotka/ansible-bsdutils/tags)

[Ansible role.](https://galaxy.ansible.com/vbotka/bsdutils/) Install and configure [bsd-utils](https://github.com/vbotka/bsd-utils).

Feel free to [share your feedback and report issues](https://github.com/vbotka/bsdutils/issues).

[Contributions are welcome](https://github.com/firstcontributions/first-contributions).


## Requirements and dependencies

### Collections

* community.general


## Role Variables

lib-mapgen is not enabled by default

```yaml
libmapgen_cron_enable: false
```

See defaults and vars/main.yml.sample


## lib-mapgen

Map library links and generate libmap.conf to fix potentially broken links. Optionally run it from the cron.

```bash
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


### Ansible lint

Use the configuration file *.ansible-lint.local* when running
*ansible-lint*. Some rules might be disabled and some warnings might
be ignored. See the notes in the configuration file.

```bash
shell> ansible-lint -c .ansible-lint.local
```


## License

[![license](https://img.shields.io/badge/license-BSD-red.svg)](https://www.freebsd.org/doc/en/articles/bsdl-gpl/article.html)


## Author Information

[Vladimir Botka](https://botka.info)
