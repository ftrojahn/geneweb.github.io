# gwu

## Documentation

Exports the content of a GeneWeb base to a .gw file.

```
Usage: geneweb.gwu <BASE> [OPT]
  -odir <dir>                       create files from original name in directory (else on -o file)
  -isolated                         export isolated persons (work only if export all database).
  -old_gw                           do not export additional fields (for backward compatibility: < 7.00)
  -raw                              raw output (without possible utf-8 conversion)
  -sep <1st_name.num surname>       To use together with the option "-odir": separate this person and all his ancestors and descendants sharing the same surname. All the concerned families are displayed on standard output instead of their associated files. This option can be used several times.
  -sep_only_file <file>             with option "-sep", tells to separate only groups of that file.
  -sep_limit <num>                  When using the option "-sep", groups of families can become isolated in the files. Gwu reconnects them to the separated families (i.e. displays them to standard output) if the size of these groups is less than 21. The present option changes this limit.
  -a <N>                            maximum generation of the root's ascendants
  -ad <N>                           maximum generation of the root's ascendants descendants
  -key <KEY>                        key reference of root person. Used for -a/-d options. Can be used multiple times. Key format is "First Name.occ SURNAME"
  -c <NUM>:                         when a person is born less than <num> years ago, it is not exported unless it is Public. All the spouses and descendants are also censored.
  -charset [ASCII|ANSEL|ANSI|UTF-8] set charset; default is UTF-8
  -d <N>                            maximum generation of the root's descendants.
  -mem                              save memory space, but slower.
  -nn                               no (database) notes.
  -nnn                              no notes (implies -nn).
  -nopicture                        don't extract individual picture.
  -o <GED>                          output file name (default: stdout).
  -parentship                       select individuals involved in parentship computation between pairs of keys. Pairs must be defined with -key option, descendant first: e.g. -key "Descendant.0 SURNAME" -key "Ancestor.0 SURNAME". If multiple pair are provided, union of persons are returned.
  -picture-path                     extract pictures path.
  -s <SN>                           select this surname (option usable several times, union of surnames will be used).
  -source <SRC>                     replace individuals and families sources. Also delete event sources.
  -v                                verbose

```

See also:
https://geneweb.tuxfamily.org/wiki/gwu
https://geneweb.tuxfamily.org/wiki/save
