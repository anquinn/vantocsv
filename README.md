# vantocsv
A utility to convert VAN/Liberalist PDF print files to CSV

## Installation
### Homebrew
```bash
$ brew tap anquinn/vantocsv
$ brew install vantocsv
# or
$ brew install anquinn/vantocsv/vantocsv
```

### Manual
Copy `vantocsv` to `/usr/local/bin/`

## Usage

```bash
$ vantocsv INPUT.pdf OUTPUT.csv
```
vantocsv relies on a few assumptions for the input PDF file: 
1) all columns are comma delimited
2) newlines are denoted with `$$`

The output CSV file does not need to exist, vantocsv will create it for you. You can supply a file path for both the input and output files, however, this utility will not create directories for you. The directory must exist for the output file to be created.

**Example VAN Report Format**
```text
100000000 , Bruce , Wayne , 1007 Mountain Drive , Gotham ,
$$ New York , K1A OA6 , 1/1/1980 , M , (333) 333-3334 ,
$$ bruce@wayneenterprises.com
```

## Options

```text
-h, --help        show brief help
-v, --version     show version number
```

## Notes
vantocsv relies on `pdftotext` which is distributed in the poppler project. If you install vantocsv using Homebrew, this will be installed for you. If you install manually you will have to install poppler yourself. 
