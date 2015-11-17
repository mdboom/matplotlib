Changes to the default style
----------------------------

The most important feature in matplotlib 2.0 are the changes to the
default style.

While it is impossible to select the best default for all cases, these
are designed to work well in the most common cases.

These changes include:

Colors
``````

- The default figure background color has changed from grey to white.

- The default cycle of colors to draw lines, markers and other content
  has been changed.  It is based on the `Vega category10 palette
  <https://github.com/vega/vega/wiki/Scales#scale-range-literals>`__.

- The default color map used for images and pcolor meshes, etc., has
  changed from ``jet`` to ``viridis``.

- For markers, scatter plots, bar charts and pie charts, there is no
  longer a black outline around filled markers by default.

- Grid lines are light grey solid 1pt lines.  They are no longer dashed by
  default.

- The ''Blues'' colormap has been adjusted to be perceptually uniform.
  The old ``blues`` colormap is available under the name
  ``legacy_Blues``.

Plot layout
```````````

- The limits are scaled to exactly the dimensions of the data, plus 5%
  padding.  The old behavior was to scale to the nearest "round"
  numbers.  To use the old behavior, set the ``rcParam``
  ``axes.autolimit_mode`` to ``round_numbers``.

- Ticks now point outward by default, and are 1pt longer.  To have
  ticks pointing inward, use the ``rcParams`` ``xtick.direction`` and
  ``ytick.direction``.

- By default, caps on the ends of errorbars are not present.

Images
``````

- The default mode for image interpolation is now ``nearest``.

Fonts
`````

- The default font has changed from "Bitstream Vera Sans" to "DejaVu
  Sans".  "DejaVu Sans" is an improvement on "Bistream Vera Sans" that
  adds more international and math characters, but otherwise should
  have the same appearance.

- The default math font when using the built-in math rendering engine
  (mathtext) has changed from "Computer Modern" (i.e. LaTeX-like) to
  "DejaVu Sans".  To revert to the old behavior, set the ``rcParam``
  ``mathtext.fontset`` to ``cm``.  This change has no effect if the
  TeX backend is used (i.e. ``text.usetex`` is ``True``).

Dates
`````

- The default date formats are now all based on ISO format, i.e., with
  the slowest-moving value first.  The date formatters are still
  changeable through the ``date.autoformatter.*`` rcParams.  Python's
  ``%x`` and ``%X`` date formats may be of particular interest to
  format dates based on the current locale.

Legends
```````

- By default, the number of points displayed in a legend is now 1.

- The default legend location is ``best``, so the legend will be
  automatically placed in a location to obscure the least amount of
  data possible.
