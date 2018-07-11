# Official Supplementary Homepage for Models

* **please visit http://www.se-rwth.de/materials/ema_compiler/**
    * there you can browse online through our models we used for our measurements
    * there you can also execute the running `Spectral clusterer` example directly in the web browser (when it supports WebAssembly and JavaScript is activated)
    * this site contains videos to see the generator in actions with different middle-ware plugins

# Supplemenatry Material for Generator

* please download the files from figshare to repeat the experiments:

(Notice: Only Win 10 64-bit is officially supported by our tools)
Note that for all measurements only the execution times were considered

Files are inside the "generator" folder.

In the "generator" folder is a "generateAll.bat". 

This file uses the emam2cpp generator to create executable cpp code out of the models that are stored in the "model" folder. 

This code can then be copied into the "benchmark/src" folder.

(The "benchmark/src" folder does also contain pre-generated code if you do not want to generate everything from scratch.)

After this you can just execute the "measureAll.bat".

This will then automatically compile the C++ code that is inside of the "src" folder and execute it afterward.

The resulting execution times are then stored in "resultsBLAS" and "resultsOpenBLAS".

Taking a look inside of the resultsBLAS folder, one can see the folders "Clusterer", "ClustererNoKMeans", "ClustererNoKMeansOpt", "ClustererOpt"
and "MatrixModifier". 

Inside of these folders are files that contain the execution times.

"timesL0.txt" contains the execution time for when no optimizations were enabled.

"timesL1.txt" contains the execution time for when algebraic optimizations were enabled.

"timesL2.txt" contains the execution time for when threading optimizations were enabled.

"timesL3.txt" contains the execution time for when algebraic&threading optimizations were enabled.

Note that this process may take some time.

Everything that is needed for the generator should be included with it.

## Webassembly (wasm)

Files are inside the "wasm" folder.

You just have to execute the "compile_allClustererLight.bat". 

If you want to compile the files to use the ClustererManOpt use "compile_allClustererManOpt.bat"

If you want to compile the files to use the Clusterer no opt use "compile_allClustererNoOpt.bat"

(The MatrixModifier will be compiled in all cases the same way)


It will open the portable chrome version with the relevant webpages that use the generated webassembly files.

Before pressing the execute model on a page it is advised to open the javascript console.

(Ctrl + Shift + J in google chrome)

So you can see the execution time, in case the website crashes when it tries to fill the fields with all output numbers.

The execution can be done without input values.
As in C++ the matrix values are what was stored in the allocated ram before.(So more or less pseudo-random)
You can set matrix values as input. In "\wasm\node\benchmark_sites" a "matrixModifierInputValues.html" is present. 
You can use this to execute it with different values.(Opened by accessing "127.0.0.1:8080/matrixModifierInputValues.html")
However, this will take a very long time, as the javascript to c++ value conversion is extremely slow.
(The other webpages can also be changed to accept input values again, by uncommenting the setXXX methods in the execute function)
(You have to execute a compile_*.bat again so the changes take effect and a node server is running)

Clusterer: A nice cluster website can also be accessed at https://embeddedmontiarc.github.io/ClusterFiddle/index.html.
There you can directly upload or select images for clustering. And see the result once it is done.(No time measurements)

Note: A portable version of chrome is inside of the folder. For some reason the objectDetector4.html example does not work 
in the portable version of chrome on one of the tested systems. However, the system installed(non-portable) version of chrome worked in this case.


## Java Projects

Files are inside the "java" folder.

For opening these projects IntelliJ is required.

Only the main method needs to be executed. It will then report the execution time in the console.

## MathJS 

Files are inside the "mathjs" folder.

The MathJS code for the "ClustererNoKMeansOpt" example is inside of the "ClustererNoKMeansOpt.txt". You can copy it into a JSFiddle or something similar for execution.

The MathJS code for the "MatrixModifier" example is inside of the "MatrixModifier.txt". You can copy it into a JSFiddle or something similar for execution.


Required for execution:

We used JSFiddle: 

ClustererNoKMeansOpt: https://jsfiddle.net/m1dn7z0v/152/

MatrixModifier: https://jsfiddle.net/m1dn7z0v/154/

Note: Site not responding messages can be ignored, the execution is continued non the less.

## Matlab

Files are inside the "Matlab" folder.

Required for execution:

We used MATLAB R2018a(64-bit).

## Octave

Files are inside the "Octave" folder.

Required for execution:

We used Octave 4.2.1 (64-bit).

## OpenModelica

Files are inside the "OpenModelica" folder.

Required for execution:

We used OpenModelica v1.12.0 (64-bit).

## Simulink

Files are inside the "Simulink" folder.

Required for execution:

We used MATLAB R2018a(64-bit).
