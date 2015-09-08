---
layout: page
title: PL/SQL Functions
permalink: /basics/functions/
---

### Functions


The syntax for a function is as follows:

    CREATE [OR REPLACE] FUNCTION [Function Name] [Parameter List]
    RETURN [Data type]
    [AUTHID DEFINER | CURRENT_USER]
    [DETERMINISTIC | PARALLEL_ENABLED | PIPELINES]
    [RESULT_CACHE [RELIES_ON (table name)]]
    IS
      [Declaration Statements]
    BEGIN
      [Executable Statements]
      RETURN [Value]
    EXCEPTION
      [Exception handlers]
    END [Function Name];
