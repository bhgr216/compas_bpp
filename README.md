# compas_bpp

Converts COMPAS regular output files into the same format as a COSMIC `bpp` table.

## Features
* Extract different binary stellar evolution events from a COMPAS regular output HDF5 file, storing them in a `bpp` DataFrame
* Generate cartoon plots from a COMPAS regular output file using [cogsworth](https://github.com/TomWagg/cogsworth)

## Instructions
* Move `compas_bpp.py` to your project directory to use functions

## Functions
* `initial(compas_output)`, `rlof(compas_output)`, `supernovae(compas_output)`, `stc(compas_output)`
    * Generate a `bpp` with one of the following event types: initial state, RLOF, supernovae, or stellar type changes
    * Takes in a file path to a COMPAS output file
    * Returns a `bpp` DataFrame
* `generate_full_bpp(compas_output)`
    * Generates a `bpp` with all of the event types listed above
* `generate_cartoon_plot(compas_output, seed)`
    * `compas_output`: file path to a COMPAS output file
    * `seed`: integer seed to generate a cartoon plot of
    * Generates a cartoon plot for a given seed from COMPAS output using `cogsworth`