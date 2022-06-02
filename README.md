# napari-sc3D-viewer

<!-- [![License](https://img.shields.io/pypi/l/napari-sc3D-viewer.svg?color=green)](https://raw.githubusercontent.com/GuignardLab/napari-sc3D-viewer/main/LICENSE)
[![PyPI](https://img.shields.io/pypi/v/napari-sc3D-viewer.svg?color=green)](https://pypi.org/project/napari-sc3D-viewer)
[![Python Version](https://img.shields.io/pypi/pyversions/napari-sc3D-viewer.svg?color=green)](https://python.org)
 -->
 [![tests](https://github.com/GuignardLab/napari-sc3D-viewer/workflows/tests/badge.svg)](https://github.com/GuignardLab/napari-sc3D-viewer/actions)
[![codecov](https://codecov.io/gh/GuignardLab/napari-sc3D-viewer/branch/main/graph/badge.svg)](https://codecov.io/gh/GuignardLab/napari-sc3D-viewer)
[![napari hub](https://img.shields.io/endpoint?url=https://api.napari-hub.org/shields/napari-sc3D-viewer)](https://napari-hub.org/plugins/napari-sc3D-viewer)

A plugin to visualize 3D single cell omics

----------------------------------

This [napari] plugin was generated with [Cookiecutter] using [@napari]'s [cookiecutter-napari-plugin] template.

## Installation

You can install `napari-sc3D-viewer` via [pip]:

    pip install .
(from the correct folder)
or

    pip install napari-sc3D-viewer

To install latest development version :

    pip install git+https://github.com/GuignardLab/napari-sc3D-viewer.git

To install the surface computation enabled version it is necessary to use Python 3.9 (until [VTK] is ported to Python 3.10) and you can run one of the following commands:

    pip install '.[pyvista]'
from the correct folder or
    
    pip install napari-sc3D-viewer[pyvista]

to install directly from pip or

    pip install 'napari-sc3D-viewer[pyvista] @ git+https://github.com/GuignardLab/napari-sc3D-viewer.git'

to install the latest version

## Usage

`napari-sc3D-viewer` allows to easily visualize and navigate 3D spatial single-cell transcriptomics using napari.

### Opening your dataset

<!-- To test your the plugin you can download the following dataset composed of a id to tissue name file located [there](https://github.com/GuignardLab/sc3D/tree/main/data) and a scanpy h5ad dataset [there](https://figshare.com/s/1c29d867bc8b90d754d2). The dataset is from the following publication: [pub] -->

The expected dataset is a [scanpy]/[anndata] h5ad file together with an optional json file that maps cluster id numbers to actual tissue/cluster name.

The json file should look like that:
```json
{
    "1": "Endoderm",
    "2": "Heart",
    "10": "Anterior neuroectoderm"
}
```
If no json file or a wrong json file is given, the original cluster id numbers are used.

The h5ad file should be informed in (1) and the json file in (2).
![images/1.loading.png]

## Contributing

Contributions are very welcome. Tests can be run with [tox], please ensure
the coverage at least stays the same before you submit a pull request.

## License

Distributed under the terms of the [MIT] license,
"napari-sc3D-viewer" is free and open source software

## Issues

If you encounter any problems, please [file an issue] along with a detailed description.

[napari]: https://github.com/napari/napari
[Cookiecutter]: https://github.com/audreyr/cookiecutter
[@napari]: https://github.com/napari
[MIT]: http://opensource.org/licenses/MIT
[BSD-3]: http://opensource.org/licenses/BSD-3-Clause
[GNU GPL v3.0]: http://www.gnu.org/licenses/gpl-3.0.txt
[GNU LGPL v3.0]: http://www.gnu.org/licenses/lgpl-3.0.txt
[Apache Software License 2.0]: http://www.apache.org/licenses/LICENSE-2.0
[Mozilla Public License 2.0]: https://www.mozilla.org/media/MPL/2.0/index.txt
[cookiecutter-napari-plugin]: https://github.com/napari/cookiecutter-napari-plugin

[file an issue]: https://github.com/GuignardLab/napari-sc3D-viewer/issues

[napari]: https://github.com/napari/napari
[tox]: https://tox.readthedocs.io/en/latest/
[pip]: https://pypi.org/project/pip/
[PyPI]: https://pypi.org/
[VTK]: https://vtk.org/
[scanpy]: https://scanpy.readthedocs.io/en/latest/index.html
[anndata]: https://anndata.readthedocs.io/en/latest/