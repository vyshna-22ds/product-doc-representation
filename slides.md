---
marp: true
title: Product Documentation (Marp)
author: 22ds3000189
theme: gaia
paginate: true
---

<!-- _class: lead -->
# Product Documentation

**Author:** 22ds3000189  
**Email:** 22ds3000189@ds.study.iitm.ac.in

> Maintainable docs → version control → export to **HTML/PDF/PPTX** with Marp.

---

<!-- Custom styling via Marp directives + inline CSS ("custom theme" spec) -->
<style>
/* "Custom theme" overrides (applies deck-wide) */
section {
  background: #0f172a;  /* slate-900 */
  color: #e2e8f0;       /* slate-200 */
}
h1, h2, h3 { color: #93c5fd; } /* light-blue-300 */
code, pre { background: #111827; border-radius: 8px; padding: 0.25em 0.5em; }
blockquote { border-left: 4px solid #93c5fd; padding-left: .8em; font-style: italic; }
.footer { position: absolute; bottom: 12px; right: 16px; font-size: .8em; opacity: .7; }
</style>

<!-- _header: **Product Docs** -->
<!-- _footer: *Confidential · v1* -->

## Why Marp for Product Docs?

- Write once in **Markdown**
- Track changes in **Git**
- Export: **HTML / PDF / PPTX / images**
- Works great in **VS Code** with the Marp extension

<div class="footer">Docs → Code → Slides</div>

---

<!-- Background image slide -->
![bg cover](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/Fronalpstock_big.jpg/1280px-Fronalpstock_big.jpg)

# Background Image Example

- This slide uses a **background image** via `![bg cover](URL)`
- Works in export (HTML/PDF/PPTX)

---

<!-- _backgroundColor: #111827 -->
<!-- _color: #e2e8f0 -->
<!-- _footer: *Complexity & Math with KaTeX* -->

## Algorithmic Complexity (Math)

Inline math: $O(n \log n)$

Block math:

$$
T(n) = T(n/2) + c n \implies T(n) = O(n \log n)
$$

Another example:

$$
\text{Throughput} = \frac{\text{Requests}}{\text{Latency}}
$$

---

## Code Sample

```python
from typing import List

def binary_search(arr: List[int], target: int) -> int:
    low, high = 0, len(arr) - 1
    while low <= high:
        mid = (low + high) // 2
        if arr[mid] == target:
            return mid
        if arr[mid] < target:
            low = mid + 1
        else:
            high = mid - 1
    return -1
