<h1 align="center">northstar-git-dedicated</h1>

**Testing Docker image for the [Northstar](https://northstar.tf) dedicated server using latest git commit of NorthstarMods** 

The goal of this image is to offer a version of pg9182's [`northstar-dedicated` image](https://github.com/pg9182/northstar-dedicated/) that uses the newest git master of [NorthstarMods](https://github.com/R2Northstar/NorthstarMods).

This image is designed mainly for testing new releases, so using it in production is discouraged!

It is however intended to work as a drop-in replacement for `northstar-dedicated`, simply updating the contents of the folder containing the Northstar mods. Therefore instructions on its usage and system requirements can be found in [pg9182's repo](https://github.com/pg9182/northstar-dedicated/).
