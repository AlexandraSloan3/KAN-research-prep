# Ch 2 - Preliminaries

Data manipulation basics from D2L — tensor creation, operators, broadcasting, indexing/slicing, memory-efficient in-place ops, and NumPy interop.

## Notebooks

- [`2.1-data-manipulation.ipynb`](2.1-data-manipulation.ipynb) — Section 2.1 walked through sentence-by-sentence with extensions (faster slicing methods, `torch.from_numpy` vs `torch.tensor`, `reshape` vs `view`, autograd caveats on in-place ops)

## Takeaway

`reshape`/`.numpy()` share memory with the original tensor when possible, but `torch.tensor(array)` always copies — a subtle gotcha the textbook glosses over. In-place ops are essential for memory efficiency but can break autograd on leaf tensors later.
