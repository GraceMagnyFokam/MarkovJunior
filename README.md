# MarkovJunior
MarkovJunior is a probabilistic programming language where programs are combinations of rewrite rules and inference is performed via constraint propagation. MarkovJunior is named after mathematician [Andrey Andreyevich Markov](https://en.wikipedia.org/wiki/Andrey_Markov,_Jr.), who defined and studied what is now called [Markov algorithms](https://en.wikipedia.org/wiki/Markov_algorithm).
MarkovJunior is written in `C#` and `XML` and runs using the `.NET framework.`

<p align="center">
<img src="images/top-iso.gif"/>
<img src="images/top-mv.gif"/>
</p>


For a more in-depth deconstruction of how the MarkovJunior algorithm works, please refer to the [original repository](https://github.com/mxgmn/MarkovJunior) by Maxim Gumin (mxgmm).

## How to build
MarkovJunior interpreter is a console application that depends only on the standard library. Get [.NET Core](https://dotnet.microsoft.com/download) for Windows, Linux or macOS and run
```
dotnet run --configuration Release MarkovJunior.csproj
```
Alternatively, download and run the latest [release](https://github.com/mxgmn/MarkovJunior/releases) for Windows.

Generated results are put into the `output` folder. Edit `models.xml` to change model parameters. Open `.vox` files with [MagicaVoxel](https://ephtracy.github.io/).

## Additional Information
The first step in using MarkovJunior to recreate EBSDs is to choose a reference EBSD. The one I chose was a stainless steel EBSD from [a paper by C.J. Todaro](https://doi.org/10.1016/j.addma.2020.101632), it's pictured below. 

<p align="center">
<img src="Research Project/Reference Stainless Steel EBSD map.jpg" height="100"/>
</p>

The next step is to extract information, such as the volume fraction, # of centroids, and orientation fraction from the reference. 
The folder labeled `Stats Extraction` (its a subfolder of "Research Project") contains 2 stats extraction files (they are both the same program, but one is a python file and the other is a jupyter notebook).
Either file can be used to get these values from the reference.

The 3rd step is to use the MarkovJunior algorithm to input the statistics to generate a tessalation.
The `Voronoi.xml` model, when ran, produces a tessalation from the growth of 2000+ centroids, each with one of 8 distinct colors. The colors that are represented by each letter can be found in `palette.xml.` 

The 8 centroid colors used were Emerald, Gray, Blue ,Red, Yellow, Brown, Purple, and Orange.

In the Voronoi model, the 2 instances of the probability variables can be used to control the orientation fraction and volume fraction, respictively.

In the algorithm, `models.xml` can be used to generate both a 2D and 3D voronoi tessalation.

<p align="center">
<img src="Research Project/2D Generated Tessalation.png" height="200"/>
<img src="Research Project/3D Generated Tessalation.png" height="200"/>
</p>

The last step is to use the 2D tessalation to generate an EBSD. This can be done using either of the `Stats Extraction` files. The `final EBSD` generated is pictured below, as well as the comparisons in stats between the reference and generated.

<p align="center">
<img src="Research Project/Generated Stainless Steel EBSD map.png" height="250"/>
</p>
<p align="center">
<img src="Research Project/Orientation Fraction Comparison.png" height="200"/>
<img src="Research Project/Volume Fraction Comparison.png" height="200"/>
</p>

## Acknowledgments


This research was funded by the Army Educational Outreach Program (AEOP) and the Hopkins Extreme Materials Institute (HEMI) at Johns Hopkins University.

