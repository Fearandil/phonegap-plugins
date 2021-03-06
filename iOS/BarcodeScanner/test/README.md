Cordova BarcodeScanner test applications
=========================================

This directory contains a set of test applications
for the Cordova BarcodeScanner plugin.  It consists
of two pieces:

* desktop app
* Cordova device app

Running the tests
-----------------

To run the tests,

* build the tests (see below)
* create a new Cordova app using [the Cordova app](phonegap-app/index.html).  This
is just a standard Cordova app that uses the barcode scanner plugin.
* fire up the desktop app by opening [the desktop app](desktop-app/index.html)
in your desktop browser.
* run the Cordova app
* the Cordova app will prompt you to scan an image currently displayed in the
desktop app.  Presumably, it will scan, and check the scan output.  Once
scanned, or if you cancel, it will move to the next image to test.  The final
tally is displayed when all the images have been scanned.

Building the tests
-----------------

Run `make build` in this directory.  It will:

* copy the `desktop-app/images` files to `phonegap-app/images`
* create a `.json` file with the image scan results, copying it
into `desktop-app` and `phonegap-app`