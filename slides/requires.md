## Requires

An application called 'A' needs a library called 'B' to run.
<!--.element: class="fragment"-->

If 'A' and 'B' are distributed as packages, the metadata of 'A' would indicate that it requires 'B'.
<!--.element: class="fragment"-->

A request to install 'A' would result in 'B' being installed as well.  We call this dependency resolution.
<!--.element: class="fragment"-->

## A requires B

* A needs B in order to function properly
* asking package manager to install A will install both A and B
* asking package manager to install B will only install B

