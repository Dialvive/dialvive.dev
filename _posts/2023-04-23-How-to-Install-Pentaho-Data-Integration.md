---
title: How to Install Pentaho Data Integration
tags: [Pentaho]
style: border
color: pentaho
comments: false
description: Learn to install any version of PDI
---

# How to Install Pentaho Data Integration

## Contents

- [Introduction](#Introduction)
- [Which version should I use?](#Version)
- [How to install PDI](#Install)
- [Conclusion](#Conclusion)
- [References](#References)

## Introduction <a name="Introduction"></a>

Pentaho Data Integration, or PDI, is a powerful open-source ETL tool. It extracts, transforms, and loads data for many applications. PDI has a visual interface to create data integration jobs. Users define data sources, manipulate data through functions, and specify the load location. In real-life, PDI combines data from various sources for analysis, reporting, or warehousing.

Examples of PDI usages include:

- migrating legacy systems to modern databases,
- financial reporting automation,
- creating data feeds for web apps,
- consuming and generating message queues,
- creating and managing Big Data jobs,
- and even machine learning.

One important  note, there are two main versions of PDI available. Pentaho Enterprise Edition, and community Pentaho Data Integration. Some key differences between the two versions include:

- Support: Paid PDI version comes with technical support, and the community version relies on community forums.
- Features: Paid PDI includes advanced features such as big data integration with Hadoop, Spark, and NoSQL databases, job orchestration, and workflow automation, which are not available in the community version.
- Scalability: Paid PDI is designed to handle larger volumes of data and can scale to meet the needs of larger enterprises, while the community version is suitable for smaller-scale projects.
- Security: Paid PDI includes enhanced security features such as data encryption, user authentication, and access controls, which are not available in the community version.
- Licensing: The community version is open-source and free to use, while the paid version requires a license fee.

In this blog I will focus only in PDI community version. It is worth mentioning that PDI community version is enough for many enterprise uses. You don't need the enterprise version for most use-cases, there's always a workaround for CE limitations.

## Which version should I use? <a name="Version"></a>

As any big application, PDI has Long-Term-Support and Short-Term-Support versions. I would suggest you always use an LTS version. Unless you are working with a legacy PDI implementation. Or you want to have the cutting-edge features.

You can check the [support policy per version here.](https://support.pentaho.com/hc/en-us/articles/205789159-Pentaho-Product-Version-End-of-Life-Policy)

## How to install PDI <a name="Install"></a>

If you don't have java installed, download the required Java version from your preferred JDK provider:

- For PDI version 3.x and 4.x, use Java 1.6.
- For PDI version 5.x, use Java 1.7.
- For PDI version 6.x and later, use Java 1.8.

Note that PDI may not work properly with later versions of Java, so it's recommended to use the specific Java version required for each version of PDI.

1. Head over to [SourceForge Pentaho Community Edition site](https://sourceforge.net/projects/pentaho/files/),
2. Select the version you wish to install (`Pentaho-X.X`),
3. Select client-tools,
4. Click on `pdi-ce-X.X.x.x-xxx.zip` to download,
5. Before extracting the zip file, open a file explorer and go to your desired installation path,
6. Create a folder called pentaho, and then a design-tools folder within,
7. Extract the zip on a folder with the zip name, within the design-tools folder,
8. Your installation path might look like:
   - Linux: `~/pentaho/design-tools/pdi-ce-X.X.x.x-xxx`
   - Windows: `C:\Program Files\pentaho\design-tools\pdi-ce-X.X.x.x-xxx`
   - Mac:  `Applications/pentaho/design-tools/pdi-ce-X.X.x.x-xxx`
9. \[Optional\] If you have or plan to have other Java versions, add to your environment variables:
   - `PENTAHO_JAVA_HOME`: put the path to the required Java installation folder.
10. \[Optional\] There will be a data-integration folder within your installation directory. Open it, and create a shortcut to spoon.sh if you are using Linux or Mac, or to spoon.bat if using Windows. Rename it to "PDI ce X.X" where ce is community edition, and X.X it's version. Drag it to your desired location.
    - In Windows, you might want to copy the shortcut to `C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Pentaho` for it to appear in your startup menu.
    - If you are a terminal enthusiast, you might want to add the path to the appropriate spoon file to your PATH environment variable, or to your bash profile.

You should be able to open Pentaho Data Integration, by executing your shortcut, or the spoon file.

## Conclusion <a name="Conclusion"></a>

Not having an official installer, and having to install PDI manually might seem daunting. But as you now know, it'll only take a few minutes. Feel free to install multiple PDI versions using this same post.

Now you are able to explore PDI and play with it to get to know the interface and components. As you explore, it might seem like there's a steep learning curve to start using PDI, but that is far from the truth.  With Pentaho Data Integration at your disposal, you'll be well-equipped to handle even the most complex data integration challenges,  it's a valuable tool that can help you streamline your data integration processes and improve your overall ETL workflow.

Coming next on this blog series, we will learn the PDI inner workings and components. Keep an eye for the next posts.

## References <a name="References"></a>

- Hitachi Vantara (Dec/2022). *Installing Pentaho Data Integration CE*. <https://www.hitachivantara.com/en-us/pdf/implementation-guide/three-steps-to-install-pentaho-data-integration-ce.pdf>
- Hitachi Vantara (No date). *Pentaho Community Edition (CE) Installation Guide for Windows - Whitepaper*. <https://www.hitachinext.com/en-us/pdf/white-paper/pentaho-community-edition-installation-guide-for-windows-whitepaper.pdf>
- Hitachi Vantara (Jun/22). *Install the PDI tools and plugins*. <https://help.hitachivantara.com/Documentation/Pentaho/9.3/Setup/Install_the_PDI_tools_and_plugins#cp_pentaho_perform_manual_install_of_pdi_design_tools_and_plugins>
