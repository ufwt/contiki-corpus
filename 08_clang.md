
#Clang Analyzer


Additionally, consult <a href = "/Statistics/">Statistics</a> for an overview of general tool results, many of which involve reportings from Clang-Analyzer. 

Within this report, you can also read more about Clang-Analyzer under the [Static Analysis](#static-analysis) section. In the corpus directory, there are also files related to the reports which the tool generates. These can be viewed in an output of your choice, but the most visually useful would be as HTML reports. 
* Can be run as a standalone tool, or through XCode.
* Can also be run as a project is built, allowing for error checking on the fly. Using this feature, Clang Analyzer also has a graphical user interface (GUI), which can be used to visually relay the location of areas with explicit steps in control flow.
* Built into many existing static analysis tools.
* Produce results in HTML/XML/CSV format for database storage and viewing.

Clang-Analyzer is a command line driven tool with an external GUI option for viewing reports. The following screenshots demonstrate how it can be run from the command line, and the various formats that its results can be observed in.

####Executing build analysis of cc26xx-web-demo

![Total Errors](Images/cc26xx-web-demo_output.png)

####Clang-Analyzer Bug Categories

![Total Errors](Images/clang_bug_categories.png)

####Output of build analysis

![Total Errors](Images/cc26xx-web-demo_scan-view_output.png)

####GUI example of a null pointer dereference bug in mqtt.c

![Total Errors](Images/cc26xx-web-demo_null_pointer_dereference_report.png)

* Since the tools performs deep analysis of the code, using it for static analysis can be much slower than compilation.
* Suffers from very high false positive rates.
* Whilst it seems to discover a larger number of errors than similar tools such as Cppcheck, it isn’t so easy to distinguish between those which are stylistic compared to legitimate errors that affect Contiki’s stability.
* A large emphasis on "dead code" related bugs, which may be viewed as false positives.
* No clear distinction of bug types. There are two main categories of "Logic Error" and "Dead Store" but a lack of granularity in terms of error severity.


