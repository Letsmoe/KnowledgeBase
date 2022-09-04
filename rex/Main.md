# tessract
Reactive server-side compiled template engine.

```
#lang gyro
#define max 100
#if PRODUCTION
% include("production_header.tess");
#endif

<script>
let x = 5;
$: doubled = x * 2;
</script>

<%
title = "Main Page";
%>

{{ title }}

<h1>{( x )}</h1>
<h2>{( doubled )}</h1>
```