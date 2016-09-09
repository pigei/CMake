find_package-dir-sort
---------------------

* The :command:`find_package` command gained the possibility of
  sorting compatible libraries by ``NAME`` or by ``NATURAL`` sorting by
  setting the two new variables :variable:`CMAKE_FIND_PACKAGE_SORT_ORDER`
  and :variable:`CMAKE_FIND_PACKAGE_SORT_DIRECTION`

* New variable :variable:`CMAKE_FIND_PACKAGE_SORT_ORDER` controls the sorting mode of
  :command:``find_package``. New variable :variable:`CMAKE_FIND_PACKAGE_SORT_DIRECTION`
  controls the sorting direction instead