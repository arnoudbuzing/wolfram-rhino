# wolfram-rhino
Experiments with the Wolfram Language + Rhino3D

Using: https://github.com/WolframResearch/RhinoLink

## Software and hardware requirements

1. Windows operating system
2. Mathematica (or Wolfram Desktop; version 11 or higher)
3. Rhino (version 6)
4. Recommended: Graphics card for rendering

## Setup instructions

The commands for step 1. through 3. can be found in this [setup.nb](https://github.com/arnoudbuzing/wolfram-rhino/blob/master/setup.nb) notebook.

1. Install the paclet for the Wolfram Language:
```
PacletInstall["https://github.com/WolframResearch/RhinoLink/releases/download/v0.9/RhinoLink-0.9.0.paclet"]
```

2. Load the package:
```
Needs["RhinoLink`"]
```

3. Run the following command to install the Wolfram Language plugin into Rhino:
```
InstallRhinoPlugin[]
```

4. Quit Mathematica

5. Start Rhino

6. In Rhino's command line window, evaluate the command below:
```
WolframConnect
```
![rhino](https://github.com/arnoudbuzing/wolfram-rhino/blob/master/images/setup-01.png "rhino")

7. Start Mathematica. Step 8. through 10. are also in the [example.nb](https://github.com/arnoudbuzing/wolfram-rhino/blob/master/example.nb) notebook.

8. Using `Evaluation > Notebook's Kernel` set the notebook's kernel to `RhinoAttach`:

![menu](https://github.com/arnoudbuzing/wolfram-rhino/blob/master/images/setup-02.png "menu")

9. Load the package:
```
Needs["RhinoLink`"]
```

10. Run the following command to deploy a sphere from the Wolfram Language to Rhino:
```
RhinoShow @ ToRhino @ BoundaryDiscretizeGraphics @ Sphere[]
```

11. View the result in Rhino:
![output](https://github.com/arnoudbuzing/wolfram-rhino/blob/master/images/output-01.png "output")

12. Render the result in Rhino:
![output](https://github.com/arnoudbuzing/wolfram-rhino/blob/master/images/output-02.png "output")

13. Now you can work with more complicated scenes and renderings:
![spheres](https://github.com/arnoudbuzing/wolfram-rhino/blob/master/images/spheres-01.jpg)
