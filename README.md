# Vistribute
Vistribute is a framework for automatically distributing visualizations across dynamic device setups. It was published as a research paper at ACM CHI conference in May 2019:

>Tom Horak, Andreas Mathisen, Clemens N. Klokmose, Raimund Dachselt, and Niklas Elmqvist. 2019. Vistribute: Distributing Interactive Visualizations in Dynamic Multi-Device Setups. In Proceedings of the 2019 CHI Conference on Human Factors in Computing Systems (CHI '19). ACM, New York, NY, USA, Paper 616, 13 pages. DOI: https://doi.org/10.1145/3290605.3300846

For a quick overview, see our project page at [imld.de/vistribute](https://imld.de/vistribute) or read [our Medium blog post](https://medium.com/@tomhorak/automatically-arranging-charts-with-vistribute-e99125b59d13?source=friends_link&sk=efbc281f3b723a56c532b03b71edbbe3).

## Vistribute System
The Vistribute system is an example implemenation of our core ideas. It builds upon [Vistrates](http://vistrates.org) (a visualization component model) as well as [Codestrates](http://codestrates.org)/[Webstrates](https://webstrates.net). Our implementation automatically analyzes all existing Vistrates visualization components as well as all devices connected to the webstrates document. Based on their properties and relationships, a distribution is calculated and applied.

## Installation
In order to use Vistribute, you need to setup a server with Webstrates and Codestrates first. See the also [Codestrates GitHub repo](https://github.com/Webstrates/Codestrates) as well as the [Webstrates documentation](https://webstrates.github.io/#doc-2019-05-16-gigwrdtxkn) for more details.

### Installing the Vistribute package
Vistribute itself is implemented as Vistrates package. As we have slightly adapted Vistrates itself, please use the version provided in the repo here.
The Codestrates package management offers a *Import Packages* option, where you can upload the zip-file or directly link to this repo.

This repo's Vistribute folder contains three packages: `Vistribute`, `Vistribute_Study_Utilities`, and `signaling`. The latter two where used for running the user study and are not required for running Vistribute itself.

Please note that you still need to manually install and configure visualizations [from the Vistrates framework](https://github.com/karthikbadam/Vistrates). Alternatively, you can install a ready-to-use example as described in the next section.

### Quick Install / Demo
In order to instantiate a ready-to-use example (including visualizations), you can create a pre-configured document via the following URL scheme:
```
https://yourserver.com/new?prototypeUrl=https://imld.de/docs/projects/vistribute/vistribute-webstrates-demo.zip
```
Replace the `yourserver.com` with the URL of you Webstrates/Codestrates server.

You can also [access a demo on the official Webstrates demo server](https://demo.webstrates.net/new?prototypeUrl=https://imld.de/docs/projects/vistribute/vistribute-webstrates-demo.zip). Clicking the link creates a new instance of the demo; to connect other devices simply enter the displayed URL (e.g., `demo.webstrates.net/verb-animal-00/`) on them.

### Usage
When opening the application, all visualizations are loaded and automatically placed on the interface. As soon as devices join/leave or visualizations are created/removed, the distribution updates again.

The overlaid interface can be toggled by pressing `Ctrl`+`O`. The blue Vistribute button in the bottom right allows to access the control panel, showing all connected devices and available visualizations.
