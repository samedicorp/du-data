# Welcome, DUDE.

Welcome to DUDE, the Dual Universe Data Enclave*.

This is an open source repository containing data files useful for [Dual Universe](https://www.dualuniverse.game) scripting.

(* _yes, this absolutely could have been any word at all, as long as it began with "E" and enabled the cheesy acronym_)

**Credits**: Thanks to **Movix** for the initial data extraction, **Archaegeo:** for feedback & suggestions, and of course to Novaquark for the actual game.

### Industry

The first file in this repo is a dump of all schematics JSON data, captured using an in-game script. The plan is to try to keep this up to date by re-running the script periodically. If you notice minor errors, please also consider subitting a pull-request.

Along with the raw data are some index files processed from it, which may prove to be more compact/useful, depending on your requirements.

These have been automatically generated from the raw data, and will be updated whenever it is.

Each schematic uses one or more ingredients, and produces one or more products. All the data for each product is repeated everywhere that it appears in the raw index, which is not very efficient.

A compact index has therefore been generated, which only refers to each product using its unique identifier and quantity. To accompany this, the product data has been extracted into its own file. If a product is produced by more than one schematic (eg as a side-effect of another schematic), it is linked only to the schematic where it is the first output. 

### Data Files

```
Data/
  Schematics/
    raw.json        The raw data dump
    compact.json    A compact index removing all names.
    names.json      An index mapping a schematic name to its id.
    ids.json        An index mapping a schematic id to its name.
    
  Products/
    products.json   A dump of all products, extracted from the schematic data, indexed by type identifier.
    names.json      An index that maps from a product name to the corresponding type identifier. 
```

