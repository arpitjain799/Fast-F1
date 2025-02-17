####################
FastF1 documentation
####################

For the passionate F1 nerds.


To get a quick overview over how to use FastF1, check out
:doc:`examples/index` or the :doc:`examples_gallery/index`.


Furthermore, there are some great articles and examples written by other people. They
provide a nice overview about what you can do with FastF1 and might help you
to get started.

  - `Accessing Formula-1 Race's historical data using Python (medium.com) <https://pandeyparul.medium.com/accessing-formula-1-races-historical-data-using-python-b7c80e544f50>`_
  - `Formula 1 Data Analysis Tutorial - 2021 Russian GP: "To Box, or Not to Box?" (medium.com) <https://medium.com/@jaspervhat/formula-1-data-analysis-tutorial-2021-russian-gp-to-box-or-not-to-box-da6399bd4a39>`_
  - `How I Analyze Formula 1 Data With Python: 2021 Italian GP (medium.com) <https://medium.com/@jaspervhat/how-i-analyze-formula-1-data-with-python-2021-italian-gp-dfb11db4b73>`_


============
Introduction
============

FastF1 gives you access to F1 lap timing, car telemetry and position,
tyre data, weather data, the event schedule and session results.

The module is designed around Pandas, Numpy and Matplotlib. This makes it easy
to use while offering lots of possibilities for data analysis and
visualization.

FastF1 handles big chunks of data (~50-100mb per session). To improve performance
data is per default cached locally as requests (be aware). The default placement
of the cache is operating system specific. A custom location can be set if desired.
For more information see :class:`~fastf1.api.Cache`.

All data is downloaded from two sources:

    - The official f1 data stream ->
      `f1-live <https://www.formula1.com/en/f1-live.html>`_
    - Ergast web api -> `ergast.com <http://ergast.com/mrd/>`_

Have fun!

============
Installation
============

It is recommended to install FastF1 using `pip`:

.. code-block:: bash

   pip install fastf1

Note that Python 3.8 or higher is required.
(The live timing client does not support Python 3.10, therefore full
functionality is only available with Python 3.8 and 3.9)

Alternatively, a wheel or a source distribution can be downloaded from Pypi.

You can also install using `conda`:

.. code-block:: bash

  conda install -c conda-forge fastf1


.. toctree::
   ← Back to Github <https://github.com/theOehrly/Fast-F1>

.. toctree::
   :maxdepth: 1
   :caption: Contents:

   examples/index
   examples_gallery/index
   fastf1
   core
   events
   api
   ergast
   utils
   plotting
   livetiming
   logging
   legacy

.. toctree::
   :maxdepth: 1
   :caption: Information:

   time_explanation
   howto_accurate_calculations
   known_bugs
   troubleshooting
   contributing/index
   changelog/index


==============
Available Data
==============

The following is a short overview over the available data with some references
to functions and objects used to work with this data.

- The event schedule for past seasons and the current season, including
  upcoming events. The schedule provides event names, countries, locations,
  dates, scheduled starting times and more.
  See :func:`fastf1.get_event_schedule`, :class:`~fastf1.events.EventSchedule`

  This data is also available for individual events.
  See :func:`fastf1.get_event`, :class:`~fastf1.events.Event`

- Driver information and session results, including driver names, team names,
  finishing and grid positions, points, and more.
  See :class:`~fastf1.core.SessionResults`, :class:`~fastf1.core.DriverResult`

- Lap timing data including sector times, lap times, pit stops, tyre data and
  more.
  See :class:`~fastf1.core.Laps`

- Telemetry data including speed, rpm, gear and more.
  See :class:`~fastf1.core.Telemetry`


==================
Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`


========================================================
Questions, Contacting the Maintainer and Code of Conduct
========================================================

For questions that may be of interest to the whole community, please use the
Github Discussions section to ask for help.

In case of questions that you prefer to discuss privately, feel free to contact
me via email at oehrly@mailbox.org. Any requests to this address will be
treated with confidentiality if desired.

FastF1 has a Code of Conduct. Complaints about a perceived breach of this code
of conduct should be sent to the above email address as well, in almost all
cases. Please refer to the Code of Conduct, available through the main page of
the GitHub repository, for information on how breaches are reported, how the
Code of Conduct is enforced and what values FastF1 encourages.


Notice
------

FastF1 and this website are unofficial and are not associated in any way with
the Formula 1 companies. F1, FORMULA ONE, FORMULA 1, FIA FORMULA ONE WORLD
CHAMPIONSHIP, GRAND PRIX and related marks are trade marks of Formula One
Licensing B.V.

