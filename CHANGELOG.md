### 1.3.0

* Upgraded to puppeteer 1.14.0 (1.1.0 previous)
* Added the --header option to set additional headers for the main request

### 1.2.0

* Upgraded to puppeteer 1.1.0 (1.0.0 previous)

### 1.1.0

* Upgraded to puppeteer 1.0.0 (0.10.2 previous)
* Added support for the header and footer templates
* The new navigation wait mechanism was used (load, domcontentloaded,
  networkidle2)
* The --network-timeout option was deprecated in favor of --delay
* A new --timeout specifies now the overall navigation timeout (page load)
* The media type now defaults to nothing, to overcome some Chromium gliches
  (pdf's look like the 1.0 ones)
* A new general --margin was added, all specific directions falls back to
  this value
* All commandline options now have a short version (-h)
* The error handling was improved, we do not print usage hints on
  errors anymore

### 1.0.4

* Added a post installation hook to fix the local Chromium file permissions
  (downloaded and installed by puppeteer) This adds file permissions for
  read and execute for group and others. With the new fixup script the
  pdfgen utility should work flawless when installed by root and used
  by a regular user.

### 1.0.3

* Moved the millis dev dependency to non-dev list
  This fix the pdfgen utility usage on production installations.
* Make use of the travis_retry utility to stabilize CI builds

### 1.0.2

* Corrected the pdfgen binary configuration on the package.json
  This should fix the `npm install -g pdfgen` command.

### 1.0.1

* Corrected the license on the package.json

### 1.0.0

* First public release of the pdfgen utility
