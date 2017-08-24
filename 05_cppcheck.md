
#Cppcheck

##Brief

Cppcheck is an analysis tool for C/C++ code. Unlike C/C++ compilers and many other analysis tools, it doesn’t detect syntax errors. Instead, Cppcheck detects the types of bugs that the compilers normally fail to detect. In order to establish a realistic overview of errors in Contiki, The goal is to avoid false positives; concentrating instead on critical flaws affect- ing its core stability. The developers behind Cppcheck lay out some key points regarding its use:

To find out additional information regarding the usage of Cppcheck in this project, the directory <a href = "Static_Analysis/Open_source_tools/cppcheck">`Static_Analysis/Open_source_tools/cppcheck`</a> contains the complete documentation and results of the tool, including screenshots, test outputs and help files.

Additionally, consult <a href = "/Statistics/">Statistics</a> for an overview of general tool results, many of which involve reportings from Cppcheck. 

Within this report, you can also read more about Cppcheck under the [Static Analysis](#static-analysis) section.

##Features



* Recursively checks directories for C/C++ code.
* Evaluates code using an error system.
* Makes programming suggestions to aid prevention of bugs.
* Capable of evaluating an entire project at once.
* Integrated into several programming IDEs as plugins e.g. Eclipse.


Below is a breakdown on the types of errors that Cppcheck is capable of reporting on. For the duration of this project, we were interested in documenting, locating and patching security bugs associated with the Contiki operating system. As such, our main interests were related to the "error" bracket of the tool's reportage, with less emphasis being focused on "warning" or "style" which mostly relayed stylistic information about the code. As such, in our statistical findings, we report only on the number of "errors" in our figures, particularly when comparing this tool with the others at our disposal.

<br>

<center>

Category | Description
---------|------------
error | Used when legitimate bugs are found.
</center>

##Images

Cppcheck is run as a command line tool, and is suitable for recursively checking multiple directories of a complex project. Below are some screenshots of the tool being executed.

####Scanning directories for bugs

![Total Errors](Images/Cppcheck_run1.png)

####Sample output of the "apps" directory

![Total Errors](Images/Cppcheck_output1.png)

##Limitations
* From the Cppcheck manual: “Please understand that there are limits of Cppcheck. Cppcheck is rarely wrong about reported errors. But there are many bugs that it doesn’t detect”.
* No focus on detecting unsafe function usage. By implementing a pattern matching based approach

##Conclusion
