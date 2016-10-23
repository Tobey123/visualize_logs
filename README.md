# visualize_logs

A Python library and command line tools to provide log visualization. 

# Gallery

When you view these plots you will need JavaScript turned on.  The plots are interactive and you can
select borders around the pieces you would like to zoom into.  You can double click to zoom out.  You can also
hover over nodes and more information will be displayed.  The plot controls will be in the upper right hand corner of the plot.

The plot will look different depending on your browser (Chrome, Firefox, etc...) and the size
of your browser.  I typically use Chrome on a Mac with a very large size to see everything I want to see.
The smaller your browser is, the more crunched it will be.  If you change your browser size, be sure to click
'Reload'.

The "focused" views were generated by selecting just the PIDs I wanted to show with ProcMon before
saving the data to a CSV.

## Ransomware 

SHA256: [9b462800f1bef019d7ec00098682d3ea7fc60e6721555f616399228e4e3ad122](https://www.virustotal.com/en/file/9b462800f1bef019d7ec00098682d3ea7fc60e6721555f616399228e4e3ad122/analysis/)

- [Example 1](https://keithjjones.github.io/visualize_logs.github.io/gallery/procmoncsv/ransomware_example1.html)
  - Ransomware showing processes only (Focused)
  - `plotprocmoncsv -sp -t "Ransomware Example 1" -f ransomware_example1.html Ransomware_focused.csv`
- [Example 2](https://keithjjones.github.io/visualize_logs.github.io/gallery/procmoncsv/ransomware_example2.html)
  - Ransomware showing processes only (All)
  - `plotprocmoncsv -sp -t "Ransomware Example 2" -f ransomware_example2.html Ransomware_focused.csv`
- [Example 3](https://keithjjones.github.io/visualize_logs.github.io/gallery/procmoncsv/ransomware_example3.html)
  - Ransomware showing processes and network only (All)
  - `plotprocmoncsv -sp -pt -pu -t "Ransomware Example 3" -f ransomware_example3.html Ransomware_focused.csv`
- [Example 4](https://keithjjones.github.io/visualize_logs.github.io/gallery/procmoncsv/ransomware_example4.html)
  - Ransomware showing file writes/renames/deletes (Focused)
  - `plotprocmoncsv -t "Ransomware Example 4" -pfw -pfd -pfn -sp -f ransomware_example4.html Ransomware_focused.csv`
  - Notice it is very clear that this is ransomware based upon all the file writes!
- [Example 5](https://keithjjones.github.io/visualize_logs.github.io/gallery/procmoncsv/ransomware_example5.html)
  - Ransomware showing file writes/renames/deletes (All)
  - `plotprocmoncsv -t "Ransomware Example 5" -pfw -pfd -pfn -sp -f ransomware_example5.html Ransomware.csv`
  - Notice it is very clear that this is ransomware based upon all the file writes!
- [Example 6](https://keithjjones.github.io/visualize_logs.github.io/gallery/procmoncsv/ransomware_example6.html)
  - Ransomware showing Registry writes and deletes (Focused)
  - `plotprocmoncsv -t "Ransomware Example 6" -prw -prd -sp -f ../gallery/procmoncsv/ransomware_example6.html /Source/Procmon\ CSV/Ransomware_focused.csv`

## wwwlgoogle dot com Adware

SHA256: [e64910e3549a6c6e01be814b40e0f1fca02db45d5d19e2882a90914cef1c799e](https://www.virustotal.com/en/file/e64910e3549a6c6e01be814b40e0f1fca02db45d5d19e2882a90914cef1c799e/analysis/)

This sample came from wwwlgoogle dot com.

- [Example 1](https://keithjjones.github.io/visualize_logs.github.io/gallery/procmoncsv/wwwlgoogle_example1.html)
  - wwwlgoogle showing processes only (Focused)
  - `plotprocmoncsv -sp -t "wwwlgoogle.com Example 1" -f wwwlgoogle_example1.html wwwlgoogle_focused.csv`
- [Example 2](https://keithjjones.github.io/visualize_logs.github.io/gallery/procmoncsv/wwwlgoogle_example2.html)
  - wwwlgoogle showing processes only (All)
  - `plotprocmoncsv -sp -t "wwwlgoogle.com Example 2" -f wwwlgoogle_example2.html wwwlgoogle.csv`
- [Example 3](https://keithjjones.github.io/visualize_logs.github.io/gallery/procmoncsv/wwwlgoogle_example3.html)
  - wwwlgoogle showing processes and network only (Focused)
  - `plotprocmoncsv -sp -pt -pu -sh -t "wwwlgoogle.com Example 3" -f wwwlgoogle_example3.html wwwlgoogle_focused.csv`
- [Example 4](https://keithjjones.github.io/visualize_logs.github.io/gallery/procmoncsv/wwwlgoogle_example4.html)
  - wwwlgoogle showing processes and network only (All)
  - `plotprocmoncsv -sp -pt -pu -sh -t "wwwlgoogle.com Example 4" -f wwwlgoogle_example4.html wwwlgoogle.csv`
- [Example 5](https://keithjjones.github.io/visualize_logs.github.io/gallery/procmoncsv/wwwlgoogle_example5.html)
  - wwwlgoogle showing processes and file writes/renames/deletes (Focused)
  - `plotprocmoncsv -sp -pfw -pfd -pfn -t "wwwlgoogle.com Example 5" -f wwwlgoogle_example4.html wwwlgoogle_focused.csv`
- [Example 6](https://keithjjones.github.io/visualize_logs.github.io/gallery/procmoncsv/wwwlgoogle_example6.html)
  - wwwlgoogle showing processes and file writes/renames/deletes (All)
  - `plotprocmoncsv -sp -pfw -pfd -pfn -t "wwwlgoogle.com Example 6" -f wwwlgoogle_example4.html wwwlgoogle.csv`
- [Example 7](https://keithjjones.github.io/visualize_logs.github.io/gallery/procmoncsv/wwwlgoogle_example7.html)
  - wwwlgoogle showing processes and Registry writes/deletes (Focused)
  - `plotprocmoncsv -sp -prw -prd -t "wwwlgoogle.com Example 7" -f wwwlgoogle_example4.html wwwlgoogle_focused.csv`


# Log Type Support

This package currently supports the following types of logs:
  - ProcMon CSV
    - Be sure to either turn on all columns or use [DetailedProcmonConfiguration.pmc](ProcMon/Configuration File/DetailedProcmonConfiguration.pmc)

More logs types are coming...

# Requirements

Graphviz must be installed and available in your path (dot, neato, etc..)
  - http://www.graphviz.org/

To install Graphviz correctly on a Mac, you will probably want to run the following command:

```
brew install graphviz --with-gts
```

This program was written with Python 3 on a Mac and Windows 7.  It should work with Python 2 and other OS's, but it has not been tested
extensively.  Please file an issue if you have problems running it somewhere.  I use Windows less than I use a Mac, so your Windows mileage may
vary.

# Installation

```
# pip install visualize_logs
```

... or you can clone and ...

```
# python setup.py install
```

# Usage

This package can be used as a library.  Use the information in the documentation section below to use it this way.
This package also contains command line tools which are outlined below.

## ProcMon CSV Command Line Tool

The best use case is if you start your ProcMon capture before you run the file you are analyzing.  If a process 
is not started the associated network connections may not be connected to the process in the plot.  I also could
not get ProcMon to capture TCP data when WinPCAP was installed.  You may not want to install WinPCAP if you are
interested in TCP data.

This this library feels like it is taking a long time, it is likely that you are trying to import a lot of ProcMon
data.  You can always filter your data and save it as a CSV showing just the events you want to graph.

```
# plotprocmoncsv -h
usage: plotprocmoncsv [-h] [-f HTMLFile] [-pa] [-pf] [-pu] [-pt] [-pr] [-pfw]
                      [-pfr] [-pfd] [-pfn] [-ptcp] [-pus] [-pur] [-prr] [-prw]
                      [-prd] [-sa] [-sp] [-st] [-su] [-sf] [-sh] [-sr]
                      [-ignpaths IgnPathsFile.txt]
                      [-inclpaths InclPathsFile.txt]
                      ProcMonCSVFile

Application to graph ProcMon CSV files

positional arguments:
  ProcMonCSVFile        ProcMon CSV file

optional arguments:
  -h, --help            show this help message and exit
  -f HTMLFile, --file HTMLFile
                        Create the log file. Default name is procmoncsv.html
  -pa, --plotall        Plot all aspects
  -pf, --plotfile       Plot all file aspects
  -pu, --plotudp        Plot all UDP aspects
  -pt, --plottcp        Plot all TCP aspects
  -pr, --plotreg        Plot all Registry aspects
  -pfw, --plotfilewrites
                        Plot file writes
  -pfr, --plotfilereads
                        Plot file reads
  -pfd, --plotfiledeletes
                        Plot file deletes
  -pfn, --plotfilerenames
                        Plot file renames
  -ptcp, --plottcpconnects
                        Plot TCP connects
  -pus, --plotudpsends  Plot UDP sends
  -pur, --plotudprecvs  Plot UDP receives
  -prr, --plotregreads  Plot Registry reads
  -prw, --plotregwrites
                        Plot Registry writes
  -prd, --plotregdeletes
                        Plot Registry deletes
  -sa, --showalllabels  Show all labels
  -sp, --showproclabels
                        Show process labels
  -st, --showtcplabels  Show TCP labels
  -su, --showudplabels  Show UDP labels
  -sf, --showfilelabels
                        Show file labels
  -sh, --showhostlabels
                        Show host labels
  -sr, --showreglabels  Show Registry labels
  -ignpaths IgnPathsFile.txt, --ignorepathsfile IgnPathsFile.txt
                        File containing regular expressions to ignore in the
                        Path column. One RE per line.
  -inclpaths InclPathsFile.txt, --includepathsfile InclPathsFile.txt
                        File containing regular expressions to include in the
                        Path column. Overrides ignores. One RE per line.
```

You can run it like this:

```
# plotprocmoncsv -pa -sp -st -sh wwwlgoogle.CSV 
Reading log: wwwlgoogle.CSV
Plotting log: wwwlgoogle.CSV
```

... and then your plot appears in your web browser!  It is also saved to `procmoncsv.html`.

# Sample data:

You can find some sample CSV from ProcMon in the [ProcMon/Sample Data] (ProcMon/Sample Data/) directory.
There are four traces:

- wwwlgoogle.com malware:
  - Focused just shows the process I ran, filtered by the ProcMon process tree tool.
  - All data without the focus.
- Ransomware:
  - Focused just shows the process I ran, filtered by the ProcMon process tree tool.
  - All data without the focus.

# Documentation

The library documentation can be found at:  https://keithjjones.github.io/visualize_logs.github.io/

# Resources

- ProcMon
  - https://technet.microsoft.com/en-us/sysinternals/processmonitor.aspx

# Similar Projects

These projects are very similar to this one and are worth trying if you are
unfamiliar with them.  They were the inspiration behind this project.  This project
was meant to compliment these tools, not replace them.  This is just a different way to
get to the same goal, with the goal being to support numerous log types in one Python
package in the future.

- Noriben
  - https://github.com/Rurik/Noriben
- ProcDot
  - http://www.procdot.com/

# License:

This application is covered by the Creative Commons BY-SA license.

- https://creativecommons.org/licenses/by-sa/4.0/
- https://creativecommons.org/licenses/by-sa/4.0/legalcode

# Contributing:

If you would like to contribute you can fork this repository, make your changes, and
then send me a pull request to my "dev" branch.