# ged2gwb

## Documentation

Imports a GEDCOM 5.5.1 file to a Geneweb base. GEDCOM is a popular format
among genealogy enthusiasts.
[GEDCOM 5.5.1 documentation](http://www.ancestris.org/dl/ancestris/norme_gedcom/Gedcom_norm_551_2019_11_15.pdf)

```
Usage: geneweb.ged2gwb [<ged>] [options] where options are:
  -charset [ANSEL|ASCII|MSDOS] Force given charset decoding, overriding the possible setting in GEDCOM
  -dates_dm Interpret months-numbered dates as day/month/year
  -dates_md Interpret months-numbered dates as month/day/year
  -ds Set the source field for persons and families without source data
  -efn When creating a person, if the GEDCOM first name part holds several names, the first of this names becomes the person "first name" and the complete GEDCOM first name part a "first name alias".
  -epn When creating a person, if the GEDCOM first name part looks like a public name, i.e. holds:
* a number or a roman number, supposed to be a number of a nobility title,
* one of the words: "der", "den", "die", "el", "le", "la", "the", supposed to be the beginning of a qualifier, then the GEDCOM first name part becomes the person "public name" and its first word his "first name".
  -f Remove database if already existing
  -fne <be> When creating a person, if the GEDCOM first name part holds a part between 'b' (any character) and 'e' (any character), it is considered to be the usual first name: e.g. -fne '""' or -fne "()".
  -lf Convert first names to lowercase letters, with initials in uppercase.
  -log <file> Redirect log trace to this file.
  -ls Convert surnames to lowercase letters, with initials in uppercase. Try to keep lowercase particles.
  -nc No consistency check
  -no_efn Cancels the previous option.
  -no_epn Cancels the previous option.
  -no_nd Don't interpret a year preceded by a minus sign as a negative year
  -no_pit Do not consider persons having titles as public
  -nopicture Don't extract individual picture.
  -o <file> Output database (default: "a").
  -particles <FILE> Use the given file as list of particles
  -rs_no_mention Force relation status to NoMention (default is Married)
  -tnd Set negative dates when inconsistency (e.g. birth after death)
  -trackid Print gedcom id to gw id matches.
  -udi x-y Set the interval for persons whose death part is undefined:
       - if before x years, they are considered as alive
       - if after y year, they are considered as death
       - between x and y year, they are considered as "don't know"
       Default x is 80 and y is 120
  -uin Put untreated GEDCOM tags in notes
  -us Convert surnames to uppercase letters.
```

Depends on the library `gwexport`.
