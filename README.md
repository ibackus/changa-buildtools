# changa-buildtools
Some simple scripts/tools I use to aid in building ChaNGa

`configure` can be used as a simple wrapper around the ChaNGa `configure` script, but it will record the configuration `#defines` and the `CHARM_DIR`.  `configure` is called exactly like ChaNGa's `configure`, from the ChaNGa directory.  The `#defines` will be saved to `ChaNGa.config` and the `CHARM_DIR` will be saved to `config.charmdir`.  The most recent configure command can be re-run by executing the generated `config.sh`.

### Example
```bash
cd /path/to/changa_directory
# define the CHARM_DIR (this only needs to be done once).  This file takes precedence
echo /path/to/charm > config.charmdir
# OR define CHARM_DIR via env variable (again, only needs to be done once)
export CHARM_DIR=/path/to/charm
# Run the script
/path/to/configure --enable-wendland=yes --enable-cooling=cosmo
# Do stuff....
# If needed, run the most recent configure command again
./config.sh
# Do more stuff...
# Change the configuration:
/path/to/configure --enable-cooling=planet
```
