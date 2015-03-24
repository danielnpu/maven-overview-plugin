# Introduction #

This document describes how dependencies have been cleaned in maven-overview-plugin with
support of maven-overview-plugin itself.


# Details #

So here we go. We'll clean some dependencies here.
Initial dependency has been like that:

![http://maven-overview-plugin.googlecode.com/files/start.png](http://maven-overview-plugin.googlecode.com/files/start.png)

## Step 1 ##
This looks quite messy, but taking a closer look and it can be seen that `doxia-site-renderer` is referenced by our project and also by `maven-reporting-impl` that is also our 1<sup>st</sup> degree dependency. So we don't need to have explicit dependency for `doxia-site-renderer` (but we want this particular version of it take a look at: [Dependency Management](http://maven.apache.org/pom.html#Dependency_Management)).

Here is our Dependency overview after removing `doxia-site-renderer`:

![http://maven-overview-plugin.googlecode.com/files/step1.png](http://maven-overview-plugin.googlecode.com/files/step1.png)

## Step 2 ##
Next one to remove is `maven-project`.
New overview:

![http://maven-overview-plugin.googlecode.com/files/step2.png](http://maven-overview-plugin.googlecode.com/files/step2.png)

## More steps ##
Next dependency removed was `maven-model':

![http://maven-overview-plugin.googlecode.com/files/step3.png](http://maven-overview-plugin.googlecode.com/files/step3.png)

After that `maven-plugin-api` was gone:

![http://maven-overview-plugin.googlecode.com/files/step4.png](http://maven-overview-plugin.googlecode.com/files/step4.png)

And `maven-artifact-manager`:

![http://maven-overview-plugin.googlecode.com/files/step5.png](http://maven-overview-plugin.googlecode.com/files/step5.png)

Also `doxia-core` was transitively included:

![http://maven-overview-plugin.googlecode.com/files/step6.png](http://maven-overview-plugin.googlecode.com/files/step6.png)

Than I used `mvn dependency:analyze` to discover that `maven-settings` have been included for no particular reason:

![http://maven-overview-plugin.googlecode.com/files/step7.png](http://maven-overview-plugin.googlecode.com/files/step7.png)

As well as `plugin-support` after removing witch we ended up with clean dependencies, at least those that are under our control:

![http://maven-overview-plugin.googlecode.com/files/stop.png](http://maven-overview-plugin.googlecode.com/files/stop.png)