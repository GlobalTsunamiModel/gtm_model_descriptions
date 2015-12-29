
# GeoClaw Input Data Formats

### Topography / Bathymetry

GeoClaw can read in multiple "topo files" that may overlap and be at different resolutions, but are all assumed to be rectangular gridded data with values of topography at the vertices. Several different formats are supported, e.g. `x,y,z` data or a header describing the grid followed by only the `z` values, or a NetCDF file.  These are described at <http://www.clawpack.org/topo.html>.

The finite volume method of GeoClaw requires cell averages of topography.  These are computed by integrating over each grid cell a piecewise bilinear function constructed using the best available (finest resolution) `topo` file(s) that cover the grid cell.

Topography files are assumed to be referenced to the same vertical datum, e.g. MHW, in which case `z = 0` corresponds to MHW.  There is also a GeoClaw paramter `sea_level` that controls the initial water level: the depth is initialized to be `z = sea_level` (which is thus relative to the vertical datum of the topo files).  

### Tsunami Sources

In addition to `topo` files, the user can also provide one or more "dtopo files" to specify moving topography, e.g. resulting from an earthquake or landslide.  These files consist of `x, y, dz` data where `dz` is the change in topography, and these values may also be provided at multiple times for dynamically moving topography.  Several different formats are supported, as described at <http://www.clawpack.org/topo.html#topography-displacement-files>.


### Earthquake Models

The Okada model is implemented in GeoClaw and can be used to generate `dtopo` files in the form required by GeoClaw.  

Several formats are supported for specifying a subfault model for an earthquake.  These are currently not well described in the GeoClaw documentation, but see

 - <http://www.clawpack.org/okada.html>
 - [Jupyter notebook examples](http://nbviewer.ipython.org/url/clawpack.github.io/notebooks/dtopotools_examples.ipynb)