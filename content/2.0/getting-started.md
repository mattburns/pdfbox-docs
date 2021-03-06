---
license: Licensed to the Apache Software Foundation (ASF) under one
         or more contributor license agreements.  See the NOTICE file
         distributed with this work for additional information
         regarding copyright ownership.  The ASF licenses this file
         to you under the Apache License, Version 2.0 (the
         "License"); you may not use this file except in compliance
         with the License.  You may obtain a copy of the License at

           http://www.apache.org/licenses/LICENSE-2.0

         Unless required by applicable law or agreed to in writing,
         software distributed under the License is distributed on an
         "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
         KIND, either express or implied.  See the License for the
         specific language governing permissions and limitations
         under the License.

layout:  default
title:   Getting Started
---

# Getting Started

This content is under construction.

## Maven

To use the latest 2.0 snapshot release from the SVN trunk, you'll need to add the following dependency:

    <dependency>
      <groupId>org.apache.pdfbox</groupId>
      <artifactId>pdfbox</artifactId>
      <version>2.0.0</version>
    </dependency>

## PDFBox and Java 8 ##

<p class="alert alert-warning">Important notice when using PDFBox with Java 8
</p>
Due to the change of the java color management module towards "LittleCMS", users can experience slow performance in color operations.
Solution: disable LittleCMS in favour of the old KCMS (Kodak Color Management System):

- start with ``-Dsun.java2d.cmm=sun.java2d.cmm.kcms.KcmsServiceProvider``or call
- ``System.setProperty("sun.java2d.cmm", "sun.java2d.cmm.kcms.KcmsServiceProvider");``

Sources:  
http://www.subshell.com/en/subshell/blog/Wrong-Colors-in-Images-with-Java8-100.html  
https://bugs.openjdk.java.net/browse/JDK-8041125