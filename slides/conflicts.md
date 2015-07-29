## Conflicts

Two similar applications, 'C' and 'D', contain some files with the same exact name that need to go in the same location.
<!--.element: class="fragment"-->

They can't be installed at the same time, because the files literally conflict with each other.
<!--.element: class="fragment"-->

If 'C' and 'D' are distributed as packages, at least one of them should have metadata that indicates it conflicts with the other.
<!--.element: class="fragment"-->

A request to install both causes an error.
<!--.element: class="fragment"-->

## C conflicts with D

* if C is installed, D cannot be installed
* if D is installed, C cannot be installed

