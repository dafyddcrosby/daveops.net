# bundles
Bundles

Layout
------

Can be accessed by NSBundle

Contents/
  CodeResources/
  Info.plist     Main package manifest
  MacOS/         Binary contents
  PkgInfo        Eight character identifier of package
  Resources/     GUI + project files
  Version.plist
  _CodeSignature/
CodeResources

Framework layout
----------------

/System/Library/Frameworks (and also /System/Library/PrivateFrameworks)

Contents/
  Headers/    - .h files
  Modules/
  Resources/
  Versions/
A/
Current/  - symlink to current version

TODO check out -framework compiler switch

