# oXygen-FOP-completion

This is project will gather the following third party libraries for use with Apache FOP in oXygen XML and provide a routine for automatically installing them:

- offo hyphenation
- the JIMI or JAI libraries for include PNG images in the final PDF document
- For PDF images you need the fop-pdf-images library

The Oxygen XML Editor installation package is distributed with the Apache FOP that is a Formatting Objects processor for rendering your XML documents to PDF. FOP is a print and output independent formatter driven by XSL Formatting Objects. FOP is implemented as a Java application that reads a formatting object tree and renders the resulting pages to a specified output.

To include PNG images in the final PDF document you need the JIMI or JAI libraries. For PDF images you need the fop-pdf-images library. These libraries are not bundled with Oxygen XML Editor but using them is very easy. You need to download them and create an external FO processor based on the built-in FOP libraries and the extension library. The external FO processor created in Preferences will have a command line like:

java -cp "${oxygenInstallDir}/lib/xercesImpl.jar:
${oxygenInstallDir}/lib/fop.jar:${oxygenInstallDir}/lib/
avalon-framework-4.2.0.jar:
${oxygenInstallDir}/lib/batik-all-1.7.jar:${oxygenInstallDir}/lib/
commons-io-1.3.1.jar:
${oxygenInstallDir}/lib/xmlgraphics-commons-1.3.1.jar:
${oxygenInstallDir}/lib/commons-logging-1.0.4.jar:
${oxygenInstallDir}/lib/saxon9ee.jar:${oxygenInstallDir}/lib/
saxon9-dom.jar:
${oxygenInstallDir}/lib/xalan.jar:${oxygenInstallDir}/lib/
serializer.jar:
${oxygenInstallDir}/lib/resolver.jar:${oxygenInstallDir}/lib/
fop-pdf-images-1.3.jar:
${oxygenInstallDir}/lib/PDFBox-0.7.3.jar" 
org.apache.fop.cli.Main -fo ${fo} -${method} ${out}You need to add to the classpath JimiProClasses.zip for JIMI and jai_core.jar, jai_codec.jar and mlibwrapper_jai.jar for JAI. For the JAI package you can include the directory containing the native libraries (mlib_jai.dll and mlib_jai_mmx.dll on Windows) in the PATH system variable.

The OS X version of the JAI library can be downloaded from http://www.apple.com/downloads/macosx/apple/java3dandjavaadvancedimagingupdate.html. In order to use it, install the downloaded package.

Other FO processors can be configured in the Preferences dialog.

Parent topic: XSL-FO Processors
Previous topic: XSL-FO Processors
Next topic: Add a Font to the Built-in FOP - The Simple Version
## building

## installation

