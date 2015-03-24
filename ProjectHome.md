# Maven Overview Plugin #

Maven plugin, creating a diagram of all dependencies, dependency graph. (The entire transitive closure.)
It supports inclusions/exclusions. Generates reports.

&lt;wiki:gadget url="http://www.ohloh.net/p/11311/widgets/project\_users\_logo.xml" height="43"  border="0" /&gt;

## Still Maintained? ##

Maven Overview Plugin is looking for new maintainer: http://stillmaintained.com/neotyk/maven-overview-plugin

## Install ##
Instruction on how to use plugin can be found in [here](http://code.google.com/p/maven-overview-plugin/wiki/Install) and [plugin information](http://maven-overview-plugin.googlecode.com/svn/site/plugin-info.html) of [generated site](http://maven-overview-plugin.googlecode.com/svn/site/index.html).

## Documentation ##
Maven generated site is [here](http://maven-overview-plugin.googlecode.com/svn/site/index.html).

## What is it? ##
For the plugin itself, it creates the diagram shown below. The color indicates if the dependency distance. The artifact for which the diagram is created is rendered as a red dot. Direct dependencies are rendered orange. Brightness will increase if you start moving to the edges of the dependency graph.

![http://maven-overview-plugin.googlecode.com/files/overview.png](http://maven-overview-plugin.googlecode.com/files/overview.png)