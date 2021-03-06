# Scikit-HEP ecosystem tutorials

Repository collecting tutorials, demos and examples on how to exploit
the Scikit-HEP ecosystem packages.

## Local notebook testing and build

To install locally, make sure miniconda is installed then run from this
directory:

```bash
conda env create
conda activate scikit-hep-tutorials
python -m ipykernel install --user --name scikit-hep-tutorials
jupyter lab
```

Only the activate and lab lines need to be run once this is installed. Use
`conda env update` to bring the environment back up to date.

To build the notebooks:

```bash
jupyter book build .
```

If you want to enable the code formatter button to put things into Black
format, run the following in the environment:

```bash
conda install -c conda-forge jupyterlab_code_formatter black isort nodejs
jupyter labextension install @ryantam626/jupyterlab_code_formatter
jupyter serverextension enable --py jupyterlab_code_formatter
```

You will now have a new button and a new command in the command pallete.

And the spell checker (can be found in the Lab UI as well, under extensions):

```bash
jupyter labextension install @ijmbarr/jupyterlab_spellchecker
```

You may be asked to rebuild.