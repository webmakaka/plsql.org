---
layout: page
title: PL/SQL Packages
permalink: /basics/packages/
---

### Packages


The syntax for creating a package is as follows:

    CREATE [OR REPLACE] PACKAGE [NAME] IS
      [PRAGMA]
      [PUBLIC CONSTRUCTS]
    END;

<br/>

    CREATE [OR REPLACE] PACKAGE BODY [NAME] IS
      [LOCAL CONSTRUCTS]
      [SUBPROGRAM DEFINITION]
      [BEGIN...END]
    END;
