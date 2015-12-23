# PowerShell Module test
A bunch of generic tests and functions to validate PowerShell modules

## Tests (in progress)
different test are catalogues in different 'Describe' and 'Context' sections

### Files
* Files are not saved in unicode
* Uses spaces, not tabs

### Module
* Passes PSScriptAnalyzer
* Has a root module file
* Is valid PowerShell
* Contains a module manifest
* Contains a root module in the manifest
*  **Contains an author (not implemented yet)**
* Help: Non default synopsis is provided
* Help: all exported functions have examples

## Functions
Functions are directly taken from the PowerShell DSCResource.Tests repo.
The purpose of those functions is to:
* Get a list of all files
* Test for file encoding
* Convert to UTF-8
* Replace tabs for spaces (4)
* Create a nuget package

## Sources
More importantly; a list of sources:
* [PowerShell team DSC resource guideliness](https://github.com/PowerShell/DscResources/blob/master/StyleGuidelines.md)
* [PowerShell DSC resource test repo on Github](https://github.com/PowerShell/DscResource.Tests)
* [Kevin Marquette's Pester in Action series](https://github.com/kmarquette/PesterInAction)
* [Publish-module cmdlet info ](https://technet.microsoft.com/en-us/library/dn807163.aspx)

## Sample Appveyor
Also included is a sample appveyor.yml file I use.

* uses an OS with WMF 5 installed
* installs Pester from Chocolatey
* installs nuget
* clones this repo
* creates an environment variable 'APIKEY' (used for publishing the module to the [PowerShell Gallery](https://www.powershellgallery.com))
* invokes all pester tests
* creates a zip appveyor artifact
* creates a nuget appveyor artifact
*  [comment] enable rdp access to the build server
*  [comment] publish to the PowerShell Gallery

### Manual actions
* Deploy the appveyor artifacts to a (configured) appveyor Github environment to push releases to Github




