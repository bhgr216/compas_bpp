# compas_bpp

Converts COMPAS regular output files into the same format as a COSMIC `bpp` table.

## Features
* Extract different binary stellar evolution events from a COMPAS regular output HDF5 file, storing them in a COSMIC style `bpp` DataFrame
* Generate cartoon plots from a COMPAS regular output file using [cogsworth](https://github.com/TomWagg/cogsworth)

## Instructions
* Move `requirements.txt` and `compas_bpp.py` to your project directory
* Install the required packages to your project's environment: `pip install -r requirements.txt`
* Import compas_bpp and use the functions (Jupyter notebook is recommended)

## Functions
* `initial(compas_output)`, `rlof(compas_output)`, `supernovae(compas_output)`, `stc(compas_output)`
    * `compas_output`: a file path to a COMPAS output file
    * Generate a `bpp` with one of the following event types: initial state, RLOF, supernovae, or stellar type changes
    * Returns a `bpp` DataFrame
* `generate_full_bpp(compas_output)`
    * `compas_output`: a file path to a COMPAS output file
    * Generates a `bpp` with all of the event types listed above
* `generate_cartoon_plot(compas_output, seed)`
    * `compas_output`: file path to a COMPAS output file
    * `seed`: integer seed from which to generate a cartoon plot
    * Generates a cartoon plot for a given seed from COMPAS output using `cogsworth`