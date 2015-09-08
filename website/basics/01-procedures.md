---
layout: page
title: PL/SQL Procedures
permalink: /basics/procedures/
---

### Procedures

The syntax for a procedures is as follows:


    CREATE [OR REPLACE] PROCEDURE [Procedure Name] [Parameter List]
    [AUTHID DEFINER | CURRENT_USER]
    IS
      [Declaration Statements]
    BEGIN
      [Executable Statements]
    EXCEPTION
      [Exception handlers]
    END [Procedure Name];
