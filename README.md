
# Artificial Ecology for Chemical Ecology Project

## How to replicate results from [Interaction Strengths Affect Whether Ecological Networks Promote the Initiation of Egalitarian Major Transitions](https://direct.mit.edu/isal/proceedings/isal/35/73/116913)

-   All relevant scripts are located in scripts/matrices
-   To enumerate over a given matrix scheme and find the fitnesses associated with different parameters of that scheme, run "sbatch search_params.sb \[generation_scheme\]"
    -   Options for generation schemes are klemm, klemm_random, motif, mangal, random
    -   The sbatch script will need to be modified to point to where your code is stored.
-   Once the data is generated, it can be analyzed using analyze_params.py and analyze_schemes.py
    -   Data is read in using the helper file get_results.py, the file path in the get_data() function will need to be modified to point to where search_params.sh stored the data
    -   Run each analysis script using "python3 analyze_schemes.py" or "python3 analyze_params.py \[generation_scheme\]"
        -   Results from analyze_params.py were not included in the paper due to space restrictions.

## Credits

This package was created with [Cookiecutter][] and the [devosoft/cookiecutter-empirical-project][] project template.

This package uses [Empirical](https://github.com/devosoft/Empirical#readme), a library of tools for scientific software development, with emphasis on also being able to build web interfaces using Emscripten.

## Dependencies

To install [Empirical](https://github.com/devosoft/Empirical), pull down a clone of the Empirical repository.  See [Quick Start Guides](https://empirical.readthedocs.io/en/latest/QuickStartGuides) for directions on cloning and using the library.


  [https://emilydolson.github.io/chemical-ecology]:
    https://emilydolson.github.io/chemical-ecology
  [Cookiecutter]: https://github.com/audreyr/cookiecutter
  [devosoft/cookiecutter-empirical-project]: https://github.com/devosoft/cookiecutter-empirical-project
