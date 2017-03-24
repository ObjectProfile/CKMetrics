# CKMetrics

Chidamber & Kemerer object-oriented metrics are a metric suite intended to monitor software quality. This repository describes the implementation of CKMetrics for VisualWorks. 

## Where to get CKMetrics for VisualWorks

* In VisualWorks connect to the publick repository in cincom 
* Load Store >> Published Items...
* Load ckmetrics-full, to get the report calculator, and the visualizer, or load ckmetrics-core to get the report calculator with the basic metrics

## Use example

For generate a report you can use the next script 

.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=
	| calculator |
	calculator := CKCalculator new.
	calculator addPackagesMatching: 'CKMetric*'.
	^ calculator printResultOnDisk: 'myckmetricreport'
.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=

The method #addPackagesMatching: uses regular expresion to find the packages that you may want to measure.
The previous code should generate a file with this output

.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=
CC	1.28421	Cyclomatic Complexity	Returns the cyclomatic complexity....
LOC	1059	Number of Lines of Code	Returns the number of lines of code, ...
LOCxC	34.1613	Number of Lines of Code per Class	Returns the average number of lines of code per class
LOCxM	4.26842	Number of Lines of Code per Method	Returns the average number of lines of code per method
LOCxP	176.5	Number of Lines of Code per Package	Returns the average number of lines of code per package
NIV	65	Number of Instance Variables	Returns the number of instance variables defined in the system
NOBugs	0	Number of Bugs	Returns the number bugs(check comment of class CKNOBugsLED)
NOC	31	Number of Classes	Returns the number of classes defined in the system
NOCom	63	Number of Commentaries	Return the number of commentaries in the system. Comments for packages, classes, and methods are considered.
NOCriticis	7	Number of code critics	Returns the number code critics(check comment of class CKNOCodeCriticsLED)
NOCxP	5.16667	Number of Classes per Package	Returns the number of classes defined per package in the system
NOIntRev	4	Number of Intention revealing	Returns the number of intention revealing(check comment of class CKNOIntentionLED)
NOM	190	Number of Methods	Returns the number of methods defined in the system (instance methods only)
NOMiscellaneous	2	Number of Miscellaneous	Returns the number of miscellaneous(check comment of class CKNOMiscellaneousLED)
NOMxC	6.12903	Number of Methods per Class	Returns the number of methods per class
NOMxP	31.6667	Number of Methods per Package	Returns the number of methods per package
NOP	6	Number Of Packages	Returns the number of packages defined in the analyzed system.
NOPossibleBugs	0	Number of Possible Bugs	Returns the number of possible bugs(check comment of class CKNOPossibleBugsLED)
NOUnnecessaryCode	1	Number of Unnecesary code	Returns the number of Unncessary code(check comment of class CKNOUnnecessaryCodeLED)
.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=.=

With the visualizer, you can use the menu Tools>>Visualize CKMetrics Reports, to get a graph that shows all the reports that you previously created. And check the evolution of your app with lines of code, number of classes, by version.

## Get in touch with us


## Platform

CKMetrics has been designed to work on Cincom VisualWorks Smalltalk, starting from version 7.4 until the most recent ones

## License

The CKMetric code for VisualWorks is under the MIT License. Code belongs to Object Profile and Lam Research. The full license is available on: https://github.com/ObjectProfile/CKMetrics/blob/master/LICENSE

Website of copyright holders
http://objectprofile.com
http://www.lamresearch.com
