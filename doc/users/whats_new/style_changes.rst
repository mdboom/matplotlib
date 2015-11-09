Changes to the default style
----------------------------

The most important feature in matplotlib 2.0 are the changes to the
default style.

While it is impossible to select the best default for all cases, these
are designed to work well in the most common cases.

These changes include:

- The default figure background color is now white.

- The limits are scaled to exactly the dimensions of the data, plus 5%
  padding.  The old behavior was to scale to the nearest "round"
  numbers.  To use the old behavior, set the ``rcParam``
  ``axes.autolimit_mode`` to ``round_numbers``.

- The default cycle of colors to draw lines, markers and other content
  has been changed.  It is based on the Dark2 qualitative color
  palette from `colorbrewer <http://colorbrewer2.org/>`__.

- For markers and scatter plots, there is no longer a black outline
  around filled markers by default.

- The default date formats are now all based on ISO format, i.e., with
  the slowest-moving value first.  The date formatters are still
  changeable through the ``date.autoformatter.*`` rcParams.  Python's
  ``%x`` and ``%X`` date formats may be of particular interest to
  format dates based on the current locale.

- Grid lines are light grey solid 1pt lines.  They are no longer dashed by
  default.

- By default, the number of points displayed in a legend is now 1.

- The default legend location is ``best``, so the legend will be
  automatically placed in a location to obscure the least amount of
  data possible.

- By default, caps on the ends of errorbars are not present.

- The ''Blues'' colormap has been adjusted to be perceptually uniform.  The old
  ``blues`` colormap is available under the name ``legacy_Blues``.
