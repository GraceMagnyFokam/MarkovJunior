# MarkovJunior Implementation for the Procedural Generation of EBSDs
MarkovJunior is a probabilistic programming language where programs are combinations of rewrite rules and inference is performed via constraint propagation. MarkovJunior is named after mathematician [Andrey Andreyevich Markov](https://en.wikipedia.org/wiki/Andrey_Markov,_Jr.), who defined and studied what is now called [Markov algorithms](https://en.wikipedia.org/wiki/Markov_algorithm).
<p align="center">
<img src="images/top-iso.gif"/>
<img src="images/top-mv.gif"/>
</p>



## How to build
MarkovJunior interpreter is a console application that depends only on the standard library. Get [.NET Core](https://dotnet.microsoft.com/download) for Windows, Linux or macOS and run
```
dotnet run --configuration Release MarkovJunior.csproj
```
Alternatively, download and run the latest [release](https://github.com/mxgmn/MarkovJunior/releases) for Windows.

Generated results are put into the `output` folder. Edit `models.xml` to change model parameters. Open `.vox` files with [MagicaVoxel](https://ephtracy.github.io/).

## Additional Information



## Acknowledgments


This research was funded by the Army Educational Outreach Program (AEOP) and the Hopkins Extreme Materials Institute (HEMI) at Johns Hopkins University.

