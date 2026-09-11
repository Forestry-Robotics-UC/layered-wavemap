# Layered Wavemap
<a href="https://github.com/Forestry-Robotics-UC/layered-wavemap/actions/workflows/cpp.yml"><img src="https://img.shields.io/github/actions/workflow/status/Forestry-Robotics-UC/layered-wavemap/cpp.yml?label=C%2b%2b&logo=C%2b%2b&logoColor=white" alt="C++"/></a>
<a href="https://github.com/Forestry-Robotics-UC/layered-wavemap/actions/workflows/python.yml"><img src="https://img.shields.io/github/actions/workflow/status/Forestry-Robotics-UC/layered-wavemap/python.yml?label=Python&logo=python&logoColor=white" alt="Python"/></a>
<a href="https://github.com/Forestry-Robotics-UC/layered-wavemap/actions/workflows/ros1.yml"><img src="https://img.shields.io/github/actions/workflow/status/Forestry-Robotics-UC/layered-wavemap/ros1.yml?label=ROS1&logo=ros&logoColor=white" alt="ROS1"/></a>
<a href="https://github.com/Forestry-Robotics-UC/layered-wavemap/actions/workflows/docs.yml"><img src="https://img.shields.io/github/actions/workflow/status/Forestry-Robotics-UC/layered-wavemap/docs.yml?label=Docs&logo=sphinx&logoColor=white" alt="Docs"/></a>
<a href="https://github.com/ethz-asl/wavemap/releases"><img src="https://img.shields.io/github/v/tag/ethz-asl/wavemap?label=Version&logo=semver" alt="Version"/></a>
<a href="https://github.com/Forestry-Robotics-UC/layered-wavemap/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-BSD%203-blue?logo=bsd" alt="License"/></a>

Layered Wavemap extends Wavemap's compressed multi-resolution occupancy map with typed environmental attributes. Continuous fields such as reflectivity, signal, near-infrared intensity, and RGB share the wavelet hierarchy with occupancy. Categorical fields such as semantic classes use aligned sparse side layers with lossless majority-with-exceptions compression.

[Get started](docs/pages/tutorials/layered_wavemap.rst) · [Run the RGB demo](#try-the-layered-rgb-demo) · [Original Wavemap documentation](https://ethz-asl.github.io/wavemap/)

[![Layered Wavemap demo](https://i.ytimg.com/vi/l24QWAxm7Zw/hqdefault.jpg)](https://youtu.be/l24QWAxm7Zw)

*Watch the Layered Wavemap demo on YouTube.*

## Try the layered RGB demo

The synthetic forest demo needs no sensor data. On Ubuntu 20.04 with ROS Noetic:

```bash
cd ~/catkin_ws
catkin build wavemap_all
source devel/setup.bash
roslaunch wavemap_ros synthetic_rgb_layered_map.launch
```

The launch file opens RViz and progressively builds a colored layered map. Docker setup, native installation, real Ouster usage, map persistence, and a layer-extension walkthrough are in the [Layered Wavemap guide](docs/pages/tutorials/layered_wavemap.rst).

## Documentation

The [Layered Wavemap guide](docs/pages/tutorials/layered_wavemap.rst) covers
installation, examples, map persistence, layer schemas, update policies, and
extension points. Documentation for the inherited Wavemap APIs and tools remains
available in the [original Wavemap documentation](https://ethz-asl.github.io/wavemap/).

## Acknowledgements

Layered Wavemap is built on and derived from
[Wavemap](https://github.com/ethz-asl/wavemap), originally developed by Victor
Reijgwart and contributors at the Autonomous Systems Lab, ETH Zurich. The
original project provides the wavelet-based multi-resolution occupancy mapping
framework on which this extension is based. This repository adds typed
continuous and discrete layers, their integration and storage policies, ROS1
support, persistence, visualization, and sensor examples.

The original Wavemap paper is:

> Victor Reijgwart, Cesar Cadena, Roland Siegwart, and Lionel Ott. “Efficient
> Volumetric Mapping of Multi-Scale Environments using Wavelet-Based
> Compression.” *Robotics: Science and Systems XIX*, 2023.
> [https://doi.org/10.15607/RSS.2023.XIX.065](https://doi.org/10.15607/RSS.2023.XIX.065)

Please cite the original work when using Wavemap or Layered Wavemap in research.
The upstream copyright and BSD 3-Clause license are preserved in
[LICENSE](LICENSE).
