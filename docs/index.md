# Roma: GV-race detector on mobile apps
Roma is a framework to automatically detect the GV-race on android apps. 
Roma extracts the GUI and VUI related call graph through static program analysis, and generates a GV interaction graph using our pre-defined highly abstract primitives to represent the GUI and VUI behavior of the app.
It introduces happen-before constraints to formally specify the freeness of GV-race with respect to the GV interaction graph, so that the property can be reduced to constraint solving with off-the-shelf SMT solvers.

## Files Tree

```text
├── README.md
├── src
│   ├── Main.java
│   ├── callGraphAnalyze
│   │   └── ...
│   ├── modelConstruct
│   │   └── ...
│   └── Solver
│       └── ...
├── config
│   ├── AndroidCallbacks.txt
│   └── SourcesAndSinks.txt
├── libs
│   └── dependencies for Roma
└── VUIConflict.jar
```

* src: contains the source code of Roma
* libs: contains the dependencies of Roma
* config: configuration files required by FlowDroid. Here, ``SourcesAndSinks.txt`` define the functions of GUI & VUI sinks mentioned in the paper.
* VUIConflict.jar: the executable jar package of Roma

## Requirements

1. Java 8
2. Android SDKs
3. [Microsoft z3](https://github.com/z3prover/z3)

## How to run Roma
```shell
java -jar VUIConflict.jar -a <path to the Apk file> -p <path to the Android platform directory> -c config/AndroidCallbacks.txt -s config/SourcesAndSinks.txt -o <path to the output directory>
```

for example:

```shell
java -jar VUIConflict.jar -a /home/xxx/Documents/dataset/com.voicenotebook.voicenotebook.apk -p /home/xxx/Android/Sdk/platforms -c config/AndroidCallbacks.txt -s config/SourcesAndSinks.txt -o /home/xxx/Documents/output/
```

## Result
* apksWithRace(step1).txt: file names of apps with GV co-access
* apksWithRace(step2).txt: file names of apps with GV-race
* tested.txt: file names of apps under tests
* time.txt: file names and analysis time of apps that terminate in 30 minutes


## Case Study

See the detailed information [here](case.md).

## Download
* [Roma](tool/Roma.zip) See the Roma directory for running Roma.
* [Dataset](dataset/dataset.zip) The 215 apks' app ids are listed here. The mutated third-party apps are also provided.
* [Output](output/output.zip) Roma's analysis results of 215 apps are saved here.
* [Validation] Some of the validation videos can be found [here](validation/video1.zip) and [here](validation/video2.zip).