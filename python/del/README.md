# Summary

##  url 
https://docs.python.org/3.6/reference/datamodel.html#object.__del__




# Usage

Note

 `del x` doesn’t directly call `x.__del__()` — the former decrements the reference count for `x` by one, and the latter is only called when `x`’s reference count reaches zero.

翻译：

`del x`不直接调用`x.__del__()`，前者对x的引用计数减1；后者只有在引用计数变为0的时候才调用。