# About #
This tool aims at grabbing and displaying performance indicators of a gstreamer pipeline to ease bottleneck debugging.

# How it works #

It displays performance indicators such as:
  * queue filling states
  * videorate statistics
  * plugin-relative time reference (using progressreport)

# How to use it #

Just place queues after elements you wish to track the status of, and the colors and statistics will help you understand what is happening. Example reasons of bad performance are:
  * stuck pipeline: an element is blocking the chain (which is often the case with display sinks without queues)
  * cpu is saturated (often encoding elements)

In any case, it is advised to use queue and videorate right after your source.

# Screenshot #
![http://gst-viewperf.googlecode.com/files/gst-viewperf.png](http://gst-viewperf.googlecode.com/files/gst-viewperf.png)

# How to install #

Dependancies:
  * gstreamer python bindings
  * [gstmanager](http://code.google.com/p/gstmanager/)
  * [TouchWizard](http://code.google.com/p/touchwizard/)