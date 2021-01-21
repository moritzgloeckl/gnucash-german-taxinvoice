# Beautiful DACH Tax Invoice
This repository is a fork of the work of Sven Eusewig's [original repository](https://github.com/sveneusewig/gnucash-german-taxinvoice). It aims to make further improvements to the German Taxinvoice template by generating a DIN5008 conform invoice for the DACH region.

## Requirements
- [Gnucash](https://www.gnucash.org/) Version >= 4.2

## Installation
To install this report you need to download the following files:

- [german-taxinvoice.scm](german-taxinvoice.scm)
- [german-taxinvoice.eguile.scm](german-taxinvoice.eguile.scm)

These need to be put into the [GNC_DATA_HOME](https://wiki.gnucash.org/wiki/Configuration_Locations#GNC_DATA_HOME) directory.

Create or edit the file `config-user.scm` in the [GNC_CONFIG_HOME](https://wiki.gnucash.org/wiki/Configuration_Locations#GNC_CONFIG_HOME) and add the following line:

```
(load (gnc-build-userdata-path "german-taxinvoice.scm"))
```

## Usage

If GnuCash was able to load the report successfully you will find it under

`Reports -> Business -> German Tax Invoice`

or in if you're using the German language pack:

`Berichte -> Geschäft -> German Tax Invoice`

Various different settings can be adjusted from within the report settings area.

**WARNING:** Make sure you save your report after adjusting the settings, otherwise they will be lost the next time you open the report.

## Development
Clone the repository to your desired location. Edit the `config-user.scm` file like shown above but change it to:

```
(load "/absolute/path/to/repository/german-taxinvoice.scm")
```

You'll then be able to make adjustments to both the eguile and scm file. Make sure to quit and re-open GnuCash when you edit the `config-user.scm` or `german-taxinvoice.scm`. 

The eguile file should be linked to the [GNC_DATA_HOME](https://wiki.gnucash.org/wiki/Configuration_Locations#GNC_DATA_HOME) directory. GnuCash expects the file to be in this directory. You can just link the file from the repository to this folder.
If you're making chances to the eguile file itself you can CTRL+R in the opened report in GnuCash and it'll reload your changes instantly. 

## License
This project is provided under the GNU General Public License v2. See [LICENSE](LICENSE).
