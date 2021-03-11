# G Suite Regex SSN

All examples generated via "Fake Name Generator" or made up.
Note that all RegEx queries needs to be compliant with RE2.

[More Info](https://support.google.com/a/answer/1371417?hl=en)


## Snippets

### Year
```
(\d{2})
```

### Month
```
(0[1-9]|1[012])
```

### Day
```
([012]\d|3[01])
```

## Swedish SSN

### Information
[Wikipedia Article](https://en.wikipedia.org/wiki/Personal_identity_number_(Sweden))

#### TLDR
```
YYYYMMDD(-)XXXX
```

### Query
```
\b(19|20)?(\d{2})(0[1-9]|1[012])([012]\d|3[01])([-+]?)(\d{4})\b
```

### Should Match
```
 9902150110
 070829-2396
 20000413-7527
 199501192856
 840901-3816
```
### Should Not Match (Company IDs)
```
 556776-0797
 556098-9591
 556746-8870
 559168-8980
 556635-7124


```

## Danish SSN

### Information
[Wikipedia Article](https://en.wikipedia.org/wiki/Personal_identification_number_(Denmark))

#### TLDR
```
DDMMYY-SSSS

DDMMYY is the date of birth and SSSS is a sequence number
```

### Query
```
\b([012]\d|3[01])(0[1-9]|1[012])((\d{2}))([-]?)([0-9]{4})\b
```

### Should Match
```
 220789-3245
 100539-4674
 290379-1600
 140302-6049
 110409-7972
```
### Should Not Match
```
N/A
```

## Norwegian SSN

### Information
[Wikipedia Article](https://www.skatteetaten.no/en/person/national-registry/birth-and-name-selection/children-born-in-norway/national-id-number/)

#### TLDR
```
DDMMYYSSSCC

DDMMYY is the date of birth, SSS is an individual number, CC is Control Digits
No dashes used.
```

### Query
```
\b([012]\d|3[01])(0[1-9]|1[012])(\d{2})([0-9]{5})\b
```

### Should Match
```
31120012345
01129955131

```
### Should Not Match
```
N/A
```

## Finnish SSN

### Information
[Wikipedia Article](https://en.wikipedia.org/wiki/National_identification_number#Finland)

#### TLDR
```
DDMMYYCZZZQ
```

### Query
```
\b([012]\d|3[01])(0[1-9]|1[012])(\d{2})(-|A)([0-9]{3})(.)\b
```

### Should Match
```
191107A804V
100855-0036
080712A2211
090353-8422
181174-030J
```
### Should Not Match
```
N/A
```

## Belgian SSN

### Information
[Wikipedia Article](https://en.wikipedia.org/wiki/Belgian_national_identity_card)

#### TLDR
```
YYMMDD*XXXCD
YYMMDD XXXCD
YYMMDD=XXXCD
```

### Query
```
\b(\d{2})(0[1-9]|1[012])([012]\d|3[01])(([\s])|([*]|[=]))([0-9]{3})(.?)[0-9]{2}\b
```
### Should Match
```
680721 013-58
120601 053-17
120601*053-46
110501=043-12
```
### Should Not Match
```
N/A
```

## Italian SSN

### Information
[Wikipedia Article](https://en.wikipedia.org/wiki/Italian_fiscal_code)

#### TLDR
```
3 Letter Surname, 3 Letter Given Name, Birthday + Letter Month + Gender, Town of Birth Code, Check Char.
```

### Query
```
\b([A-Z]{3})(\s)?([A-Z]{3})(\s)?([0-9]{2})([A|B|C|D|E|H|L|M|P|R|S|T])([0-6][0-9]|[7][0-1])(\s)?([A-M]|[Z])([0-9]{3})([A-Z]|[1-9])\b
```
### Should Match
```
MLLSNT82P65Z404U
MRTMTT25D09F205Z
LVE RBS 89T14 D637D
LVERBS89T14D637D
VRNMNL63D02D018O
FOX DRA 26C24 H872Y
VRNMNL63D71D018O

```
### Should Not Match
```
VRNMNL63D99D018O
```
