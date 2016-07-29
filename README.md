# changa-buildtools
Some simple scripts/tools I use to aid in building ChaNGa

`configure` can be used as a simple wrapper around the ChaNGa `configure` script, but it will record the configuration `#defines` and the `CHARM_DIR`.  `configure` is called exactly like ChaNGa's `configure`, from the ChaNGa directory.  The `#defines` will be saved to `ChaNGa.config` and the `CHARM_DIR` will be saved to `config.charmdir`.  To define the `CHARM_DIR`, make a one-line file `config.charmdir` with the directory defined, e.g.:

```bash
cd /path/to/changa_directory
echo /path/to/charm > config.charmdir
```

This also outputs a file `config.args` which records the arguments which were passed to ChaNGa's `configure` script.
