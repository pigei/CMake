CMAKE_FIND_PACKAGE_SORT_ORDER
-----------------------------

The default order for sorting packages found using :command:`find_package`.
It can assume one of the following values:

* ``NONE`` (default): no attempt is done to sort packages.
  The first valid package found will be selected.
* ``NAME`` : sort packages lexicographically before selecting one.
* ``NATURAL``: sort packages using natural order,
  e.g. such that contiguous digits are compared as whole numbers

Natural sorting can be employed to return the highest version
when multiple versions of the same library are found by :command:`find_package`:

E.g. suppose that the following libraries have been found::

  libX-1.1.0
  libX-1.2.9
  libX-1.2.10

By setting ``NATURAL`` order we can select the one with the highest
version number ``libX-1.2.10``::

  SET(CMAKE_FIND_PACKAGE_SORT_ORDER NATURAL)
  FIND_PACKAGE(libX CONFIG)

The sort direction can be controlled using
:variable:`CMAKE_FIND_PACKAGE_SORT_DIRECTION`
(by default decrescent, e.g. lib-B will be tested before lib-A)