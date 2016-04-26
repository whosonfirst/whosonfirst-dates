# whosonfirst-dates

This is where we will think about time. Which is hard. Because it can not be denied...

## EDTF

The decision to use the Library of Congress' [Extended Date/Time Format](http://loc.gov/standards/datetime/) (EDTF)
for dates in Who's On First has not been formalize but it seems like a good
idea.

There are not many working implementations for handling EDTF date strings in
code which is not ideal. On the other hand it is the most robust format, to
date, for representing ambiguities in dates which is probably the more important
criteria in the short-term.

## Currently

### edtf:inception

An EDTF date string indicating when a place was "created". The semantics of what created means – a declaration
of independence, a recognition of that declaration, it's administrative
incorporation and – are left for another dicussion.

### edtf:cessation

An EDTF date string indicating when a place ceased to exist as a political
entity or social construct in "popular" culture.

### edtf:deprecated

An EDTF date string indicating when a Who's On First record was officially deprecated, for example if the record references a place considered to be invalid.

### Examples

#### British North America

```
wof:name="British North America"
edft:inception="1783~"
edtf:cessation="1907"
```

_Note: As of this writing we do not actually have a WOF record for [British
North America](https://en.wikipedia.org/wiki/British_North_America). It is included only as an example._

#### Yugoslavia

```
wof:name="Kingdom of Yugoslavia"
edtf:inception="1918"
edtf:cessation="1941"
```

```
wof:name="Socialist Federal Republic of Yugoslavia"
edtf:inception="1945-11-29"
edtf:cessation="1991-06~/1995-12~"
```

```
wof:name="Bosnia and Herzegovina"
edtf:inception="1992-03~/1992-04~"
```

_Note: As of this writing we do not actually have a WOF records for
[Yugoslavia](https://en.wikipedia.org/wiki/Yugoslavia). They are included only
as examples._

## To consider

`chartered` and `incorporated` as does TGN, for example: [Montreal](https://www.getty.edu/vow/TGNFullDisplay?find=Montreal&place=&nation=&prev_page=1&english=N&subjectid=7013051).

## See also

### Who's On First

* https://whosonfirst.mapzen.com/
* https://github.com/whosonfirst/whosonfirst-docs

### EDTF

* http://loc.gov/standards/datetime/
* https://github.com/ixc/python-edtf
* http://digital2.library.unt.edu/edtf/

### ISO-8601 / RFC 3339

* https://tools.ietf.org/html/rfc3339

### CIDOC-CRM (temporal representation)

* https://github.com/whosonfirst/go-whosonfirst-temporal
* http://cidoc-crm.org/tools.html
