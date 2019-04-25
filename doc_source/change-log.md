# Change Log for Amazon Corretto 8<a name="change-log"></a>

The following sections describe the changes for each release of Amazon Corretto 8\.

## April 2019 critical patch update: Corretto version 8\.212\.04\.1<a name="changes-2019-04-16"></a>

Release Date: Apr 16, 2019

 The following platforms are updated in this release\. 

**Target Platforms**
+  RPM\-based Linux using glibc 2\.12 or later, x86\_64 
+  Debian\-based Linux using glibc 2\.12 or later, x86\_64 
+  Windows 7 or later, x86, x86\_64 
+  macOS 10\.10 and later, x86\_64 

The following issues and enhancements are addressed in 8\.212\.04\.1\.


| Issue Name | Platform | Description | Link | 
| --- | --- | --- | --- | 
|  Update Corretto to 8\.212\.04\.1\.  |  All  |  Update Corretto 8 patch set to 8\.212\.04\.1\.  |   | 
|  Backport JDK\-8048782: OpenJDK: PiscesCache : xmax/ymax rounding up can cause RasterFormatException  |  All  |  This patch fixes issue where sun\.java2d\.pisces\.PiscesCache constructor that accepts min/max x and y arguments \- the internal 'bboxX1' and 'bboxY1' are set to values one greater than given maximum X and Y values\. This effectively causes an "off by 1" error\.  |  [corretto\-8\#94](https://github.com/corretto/corretto-8/issues/94)  | 
|  Add jinfo file to Corretto Debian package\.  |  Debian\-based Linux  |  This patch fixes Corretto 8 does not provide a \.jinfo file, which used by update\-java\-alternatives to switch all java related symlinks to another distribution\.  |  [corretto\-8\#63](https://github.com/corretto/corretto-8/issues/63)  | 
|  Include /jre/lib/applet directory in rpm and deb packaging  |  RPM\-based Linux，Debian\-based Linux  |  /jre/lib/applet directory is missing in Corretto8 generic Linux deb and rpm, which makes it inconsistent with generic Linux tgz and other artifacts\. This patch adds it back to deb and rpm\.  |   | 

## 8\.202\.08\.2: Amazon Corretto 8 RC\.<a name="changes-2019-01-25b"></a>

Release Date: Jan 25, 2019

 The following platforms are updated in this release\. 

**Target Platforms**
+  RPM\-based Linux using glibc 2\.12 or later, x86\_64 
+  Debian\-based Linux using glibc 2\.12 or later, x86\_64 
+  Windows 7 or later, x86, x86\_64 
+  macOS 10\.10 and later, x86\_64 

The following issues and enhancements are addressed in 8\.202\.08\.2\.


| Issue Name | Platform | Description | Link | 
| --- | --- | --- | --- | 
|  Update java\.vendor/java\.vm\.vendor\.  |  All  |  Vendor\-related metadata has been updated to identify Amazon as the vendor of this OpenJDK distribution\.  |  [corretto\-8\#3](https://github.com/corretto/corretto-8/issues/3)  | 
|  The Windows Installer should set file association for \.jar files\.  |  Windows  |  Windows users will now be able to run executable JARs using the file explorer\.  |  [corretto\-8\#43](https://github.com/corretto/corretto-8/issues/43)  | 
|  Javapackager fails to load DLLs\.  |  Windows  |  The JavaFX Packager on Windows has been fixed to allow bundling of MSVC DLLs\.  |  [corretto\-8\#47](https://github.com/corretto/corretto-8/issues/47)  | 

## 8u202 PSU releases: Corretto version 8\.202\.08\.1 for Amazon Linux 2\.<a name="changes-2019-01-25a"></a>

Release Date: Jan 25, 2019

The following new platforms are supported\.

**New Platforms**
+  Experimental support for aarch64 on Amazon Linux 2\. 

 The following platforms are updated in this release\.

**Target Platforms**
+  Amazon Linux 2 

## 8u202 PSU releases: Corretto version 8\.202\.08\.1<a name="changes-2019-01-23"></a>

Release Date: Jan 23, 2019

 The following platforms are updated in this release\. 

**Target Platforms**
+  RPM\-based Linux using glibc 2\.12 or later, x86\_64 
+  Debian\-based Linux using glibc 2\.12 or later, x86\_64 
+  Windows 7 or later, x86, x86\_64 
+  macOS 10\.10 and later, x86\_64 

The following issues and enhancements are addressed in this release\.


| Issue Name | Platform | Description | Link | 
| --- | --- | --- | --- | 
|  Remove DIZ files in Windows distribution\.  |  Windows  |  Previous releases of Corretto on Windows contained debugging\-related DIZ files\. We received feedback that removing these files would benefit resource\-constrained environments\.  |  [corretto\-8\#33](https://github.com/corretto/corretto-8/issues/33)  | 
|  Improvements to JAVA\_HOME\-related variables on Windows\.  |  Windows  |  Two fixes that will improve the ability for Windows applications to detect and use Amazon Corretto\.  |  [corretto\-8\#39](https://github.com/corretto/corretto-8/issues/39) and [corretto\-8\#40](https://github.com/corretto/corretto-8/issues/40)  | 

## New platform releases: Version 1\.8\.0\_192\-amazon\-corretto\-preview2\-b12 and 1\.8\.0\_192\-amazon\-corretto\-preview2\_1\-b12<a name="changes-2019-01-16"></a>

Release Date: Jan 16, 2019

The following new platforms are supported\.

**New Platforms**
+  RPM\-based Linux using glibc 2\.12 or later, x86\_64 
+  Debian\-based Linux using glibc 2\.12 or later, x86\_64 

 The following platforms are compatible with this release\. 

**Target Platforms**
+  RPM\-based Linux using glibc 2\.12 or later, x86\_64 
+  Debian\-based Linux using glibc 2\.12 or later, x86\_64 
+  Windows 7 or later, x86, x86\_64 
+  macOS 10\.10 and later, x86\_64 

The following issues and enhancements are addressed in this release\.


| Issue Name | Platform | Description | Link | 
| --- | --- | --- | --- | 
|  Support distribution via tar\.gz/ZIP archives  |  Linux  |  To support other distribution systems \(eg: Docker images, SDKMan\), Corretto should also be offered in "plain" archives \(tar\.gz, ZIP\)\.  |  [corretto\-8\#2](https://github.com/corretto/corretto-8/issues/2) and [corretto\-8\#10](https://github.com/corretto/corretto-8/issues/10)  | 
|  Debian Package distribution  |  Linux  |  Corretto should be offered in Debian package format in favor of customers using Debian\-based Linux\.  |  [corretto\-8\#16](https://github.com/corretto/corretto-8/issues/16)  | 
|  Support older versions of GLIBC  |  Linux  |  Current RPM for Amazon Linux 2 contains binaries that require GLIBC\_2\.26\.  |  [corretto\-8\#20](https://github.com/corretto/corretto-8/issues/20)  | 
|  File javafx\-src\.zip missing: source code debugging for OpenJFX not enabled  |  Windows  |  The preview release is missing file javafx\-src\.zip with the compressed source code of OpenJFX\.  |  [corretto\-8\#19](https://github.com/corretto/corretto-8/issues/19)  | 
|  Easy identification x86/x64 in Apps & Features of Windows  |  Windows  |  The Windows installer/uninstaller of Corretto should clearly display the architecture \(x86/x64\) information\.  |  [corretto\-8\#37](https://github.com/corretto/corretto-8/issues/37)  | 
|  macOS Corretto installer without root access  |  macOS  |  Corretto Mac installer requires root access during the installation however some environments will require Corretto to be installed without necessarily having root access\.  |  [corretto\-8\#31](https://github.com/corretto/corretto-8/issues/31)  | 

## Bug fix releases: Version 1\.8\.0\_192\-amazon\-corretto\-preview2\-b12<a name="changes-2018-12-17"></a>

Release Date: Dec 17, 2018

 The following platforms are compatible with this release\. 

**Target Platforms**
+  Windows 7 or later, x86, x86\_64 
+  macOS 10\.10 and later, x86\_64 

 The following are the bugs and enhancements addressed in this release\. 


| Issue Name | Platform | Description | Link | 
| --- | --- | --- | --- | 
|  libfreetype\.dylib is incorrectly packaged  |  macOS  |  The libfontmanager in Corretto is linked to the libfreetype in X11 and breaks when X11 is not installed\.  |  [corretto\-8\#6﻿](https://github.com/corretto/corretto-8/issues/6﻿)  | 
|  Eclipse and Eclipse\-installer fail to run when using Amazon Corretto 8  |  macOS  |  The libjli\.dylib under `amazon-corretto-8.jdk/Contents/MacOS` should be a symlink to `../Home/jre/lib/jli/libjli.dylib` but was dereferenced\. This causes the native JVM invoker in Ecplise failed to locate the JRE\.  |  [corretto\-8\#18](https://github.com/corretto/corretto-8/issues/18)  | 
|  Enhance Installer to add standard registry keys on Windows for compat  |  Windows  |  Enhance the Windows installer to add registry keys for Corretto during the installation process\.  |  [corretto\-8\#14](https://github.com/corretto/corretto-8/issues/14)  | 
|  Allow JAVA\_HOME and PATH to be configured from installer  |  Windows  |  Enhance the Windows installer to add `JAVA_HOME` environment variable and also update the `PATH` environment variable with the Corretto installation location\.  |  [corretto\-8\#15](https://github.com/corretto/corretto-8/issues/15)  | 
|  Support Windows 32bit binaries  |  Windows  |  Provide certified build for Windows 32bit OS\.  |  [corretto\-8\#22](https://github.com/corretto/corretto-8/issues/22)  | 

## Initial Release: Version 1\.8\.0\_192\-amazon\-corretto\-preview\-b12<a name="changes-2018-11-14"></a>

Release Date: Nov 14, 2018

 The following platforms are compatible with this release\. 

**Target Platforms**
+  Amazon Linux 2, x86\_64 
+  Windows 7 or later, x86\_64 
+  macOS 10\.10 and later, x86\_64 

 The following are the changes for this release\. 


| Patch | Description | Release Date | 
| --- | --- | --- | 
|   \[C8\-1\] Prevent premature OutOfMemoryException when G1 GC invocation is suspended by a long\-running native call\.   |   Programs that use the G1 GC could experience spurious out\-of\-memory \(OOM\) exceptions even when the Java heap was far from filling up\. This happened when a spin loop that waited for long\-running native calls gave up after only two rounds\. This small patch makes this loop wait as long as it takes\. Typically a few more rounds suffice\. Worst case, a full GC would eventually occur \(thanks to JDK\-8137099\) and also resolve the situation\. The patch includes a unit test that provokes needing more than two rounds and succeeds only if the patch is in place\. See JDK\-8137099 for discussion\.  |  2018\-11\-14  | 
|  \[C8\-2\] Back port from OpenJDK 10, fixing JDK\-8177809: “File\.lastModified\(\) is losing milliseconds \(always ends in 000\)”\.  |  This patch removes inconsistencies in how the last\-modified timestamp of a file is reported\. It standardizes the behavior across build platforms and Java methods so that the user receives second\-level precision\.   |  2018\-11\-14  | 
|   \[C8\-3\] Back port from OpenJDK9, fixing JDK\-8150013, “ParNew: Prune nmethods scavengable list”\.   |   This patch reduces pause latencies for the Parallel and the CMS garbage collector\. GC “root scanning” speeds up by up to three orders of magnitude by reducing redundant code inspections\.   |  2018\-11\-14  | 
|   \[C8\-4\] Back port from OpenJDK 9, fixing JDK\-8047338: “javac is not correctly filtering non\-members methods to obtain the function descriptor”\.   |   This patch fixes a compiler bug that caused compile\-time errors when a functional interface threw an exception that extended Exception\.   |  2018\-11\-14  | 
|   \[C8\-5\] Back port from OpenJDK 10, fixing JDK\-8144185: “javac produces incorrect RuntimeInvisibleTypeAnnotations length attribute”\.   |   This problem made Findbugs, JaCoCo, and Checker Framework fail on some well\-formed input programs\.   |  2018\-11\-14  | 
|   \[C8\-6\] Trigger string table cleanup in G1 based on string table growth\.   |   This patch triggers “mixed” G1 collections needed to clean out the string table entries based on string table growth, not just Java heap usage\. The latter is an independent measurement and can trigger too rarely or even never, in some applications\. Then the string table can grow without bounds, which is effectively a native memory leak\. See JDK\-8213198\.  |  2018\-11\-14  | 
|   \[C8\-7\] Backport from OpenJDK 9, fixing JDK\-8149442: “MonitorInUseLists should be on by default, deflate idle monitors taking too long”\.   |   This patch makes removing a performance bottleneck for highly thread\-intensive applications the default setting\. Enabling MonitorInUseLists allows more efficient deflation of only potentially in\-use monitors, instead of the entire population of monitors\.   |  2018\-11\-14  | 
|   \[C8\-8\] Back port from OpenJDK 11, fixing JDK\-8198794: “Hotspot crash on Cassandra 3\.11\.1 startup with libnuma 2\.0\.3”\.   |   This patch prevents Cassandra 3\.11\.1 from crashing at startup\.   |  2018\-11\-14  | 
|   \[C8\-9\] Back port from OpenJDK 11, fixing JDK\-8195115: “G1 Old Gen MemoryPool CollectionUsage\.used values don't reflect mixed GC results”\.   |   Without this patch, it's impossible to determine how full the heap is by means of JMX when using the G1 GC\.   |  2018\-11\-14  | 
|   \[C8\-10\] Speed up Class\.getSimpleName\(\) and Class\.getCanonicalName\(\)\.   |   Memorization greatly speeds up these functions\. This patch includes correctness unit tests\. See JDK\-8187123\.   |  2018\-11\-14  | 
|   \[C8\-11\] Back port of JDK\-8068736 from OpenJDK9, fixing “Avoid synchronization on Executable/Field\.declaredAnnotations”\.   |   Improves the performance of Executable/Field\.declaredAnnotations\(\) by result caching that avoids thread synchronization\.   |  2018\-11\-14  | 
|   \[C8\-12\] Back port from OpenJDK 9, fixing JDK\-8077605: “Initializing static fields causes unbounded recursion in javac”\.   |   N/A   |  2018\-11\-14  | 
|   \[C8\-13\] Fixed JDK\-8130493: “javac silently ignores malformed classes in the annotation processor”\.   |   javac silently swallowed malformed class files in an annotation processor and returned with exit code 0\. With this patch, javac reports an error message and returns with a non\-zero exit code\.   |  2018\-11\-14  | 
|   \[C8\-14\] Improved error message for the jmap tool\.   |   Suggests additional approaches when the target process is unresponsive\. See JDK\-8213443\.   |  2018\-11\-14  | 
|   \[C8\-15\] Fixed JDK\-8185005: “Improve performance of ThreadMXBean\.getThreadInfo\(long ids\[\], int maxDepth\)”\.   |   This patch improves the performance of a JVM\-internal function that looks up a Java Thread instance from an OS thread ID\. This benefits several ThreadMXBean calls such as getThreadInfo\(\), getThreadCpuTime\(\), and getThreadUserTime\(\)\. The relative performance improvement increases with the number of threads in the JVM, as linear search is replaced by a hash table lookup\.   |  2018\-11\-14  | 
|   \[C8\-16\] Back port from OpenJDK 12, fixing JDK\-8206075: “On x86, assert on unbound assembler Labels used as branch targets”\.   |   Label class instances \(used to define pseudo\-assembly code\) can be used incorrectly in both the C1 and Interpreter\. The most common mistake for a label is being "branched to" but never defined as a location in code via bind\(\)\. An assert was added to catch these and thus triggered 106 jtreg/hotspot and 17 jtreg/jdk test failures\. We then determined that the label backedge\_counter\_overflow was not bound when UseLoopCounter was True but UseOnStackReplacement was False\. This is now fixed and guarded by the above tests\.   |  2018\-11\-14  | 
|   \[C8\-17\] Improve portability of JVM source code when using gcc7\.   |   This patch places up\-to\-date type declarations in all places where the gcc switch “\-Wno\-deprecated\-declarations” would flag problems\. It also enables the switch to catch future related issues\. This makes the source code compile on all present Amazon Linux versions\. This is a combination of much of JDK\-8152856, JDK\-8184309, JDK\-8185826, JDK\-8185900, JDK\-8187676, JDK\-8196909, JDK\-8196985, JDK\-8199685, JDK\-8200052, JDK\-8200110, JDK\-8209786, JDK\-8210836, JDK\-8211146, JDK\-8211370, JDK\-8211929, JDK\-8213414, and JDK\-8213575\.   |  2018\-11\-14  | 
|   \[C8\-18\] Back port from JDK 10, fixing JDK\-8195848: “JTREG test for StartManagementAgent fails”\.   |   See [http://serviceability\-dev\.openjdk\.java\.narkive\.com/cDFwZce9](http://serviceability-dev.openjdk.java.narkive.com/cDFwZce9) for more details\.   |  2018\-11\-14  | 
|   \[C8\-19\] Re\-enables a legacy/disabled cipher suite to pass two TCK tests that would otherwise fail\.   |   N/A   |  2018\-11\-14  | 