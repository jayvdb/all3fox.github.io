---
layout: post
title: Use specific Java version in IntelliJ IDEA
---

Recently I had to set up IntelliJ IDEA 2016.2 to use Java 1.7 for my
project. Here is a short summary of what eventually worked for me:

1. Go to `File -> Settings -> Build, Execution, Deployment -> Compiler -> Java Compiler`
2. Choose the bytecode version to be the one you need
3. Go to `File -> Project Structure`, under `Project Settings -> Project` submenu choose Project SDK to be the one you need

At this point, compiling your modules should use the expected java
version. If not, try reading the original IntelliJ IDEA documentation
on the [Java Compiler][1] and [Using multiple JDKs][2], hope it helps.


[1]: https://www.jetbrains.com/help/idea/2016.2/java-compiler.html
[2]: https://www.jetbrains.com/help/idea/2016.2/using-multiple-build-jdks.html