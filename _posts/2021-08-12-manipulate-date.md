---
layout: posts
title: "Business Central - Manipulate date fields for reports or filters"
categories: ['Dynamics Business Central', 'Administration']
classes: wide
excerpt: "Explain how to manipulate date in reports or filter."
---

### Objective
I will show you how to manipulate date fields for reports or filters. Not that complicated but it has its own syntax.
### Syntax
1. Between date:
    * Example: From 01/04/21 to 30/04/21 will be ***01/04/21..30/04/21***

2. Transations on or before the date
    * Example: Before 01/04/21 will be ***..01/04/21***

3. Transactions on or after the date
    * Example: After 01/04/21 will be ***01/04/21..***

4. Transactions on either or these days
    * Example: Either 01/04/21 or 08/04/21 will be ***01/04/21|08/04/21***

<div class="notice">NOTICE - date is in dd/mm/yy format.</div>