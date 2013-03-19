---
layout: post
title: "Everyday Gaelyk: Living on the edge with Gaelyk snapshots"
description: "How to setup Gaelyk Gradle build to use latest snapshots"
category: Everyday Gaelyk
tags: [gaelyk 2.0, gradle]
---

I've setup [Gaelyk Continuous Integration Server](https://gaelyk.ci.cloudbees.com/) on [CloudBees](http://www.cloudbees.com) few months ago so each time
the change is pushed to Gaelyk repository and the tests are passing then the new JARs are pushed to the snapshot repository currently hosted at
[SonaType OSS](https://oss.sonatype.org/content/repositories/snapshots/). If you like living on the edge and using the latest features you can 
use these in your application.

<!--more-->

Updating [Gradle](http://www.gradle.org) build is pretty easy. Only thing you need to do is to declare
[SonaType snapshot repository](https://oss.sonatype.org/content/repositories/snapshots/) in `repositories` configuration closure

*Repositories configuration*

    repositories {
        ...
        mavenRepo url: 'https://oss.sonatype.org/content/repositories/snapshots/'
    }

and change the version of your [Gaelyk](http://gaelyk.appspot.com) dependency to the snapshot version, `2.0-SNAPSHOT` at the time of writing.

*Dependencies configuration*

    dependencies {
        ...
        compile 'org.gaelyk:gaelyk:2.0-SNAPSHOT'
    }

Here you go, you're now using the latest version of [Gaelyk](http://gaelyk.appspot.com) available.

{% include JB/setup %}
