polypermclass
=============

### Implements algorithm found in *link to paper* to enumerate polynomial permutation classes


Installation
------------

The easiest way is to use 

    git clone https://github.com/cheyneh/permpy.git

This will copy the package into the current directory. 
If you don't have a git client, you can download the package 
as a zip file from 
[here](http://github.com/cheyneh/permpy/zipball/master/).

Then just use 

    import polypermclass

or

    from polypermclass import *

Examples:
--------
```python
>>>
>>> from polypermclass import *
>>> 
>>> 
>>> # Compute the class of permutations which are at most two 
>>> # block transposes from the identity:
>>> C = PolyClass.block_transpose(2)
>>> 
>>> C.genfcn()
 -(x**6 - 2*x**5 + 23*x**4 - 22*x**3 + 16*x**2 - 6*x + 1)/(x - 1)**7
>>> 
>>> C.sequence(10)
[(1, 1),
 (2, 2),
 (3, 6),
 (4, 23),
 (5, 89),
 (6, 295),
 (7, 827),
 (8, 2017),
 (9, 4405),
 (10, 8812)]
>>>
>>>
>>> p = Permutation([4,3,2,1])
>>> C.is_member(p)
 False
>>> 
>>>
>>> C.polynomial()
polynomial works from at least length 13
1 + -1/15n^1 + -53/360n^2 + 7/48n^3 + 19/144n^4 + -19/240n^5 + 11/720n^6
```
