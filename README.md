# replicate
REpository for Prospective LIfe Cycle Assessment daTabasEs

This repository lists data packages that can be used together with the library [unfold](https://github.com/polca/unfold) to reproduce scenario-based or prospective life-cycle assessment databases.

Once you have identified the data package of interest, you can extract the databases in a `brightway2` project by doing the following:

.. code:: python

  from unfold import Unfold
  import bw2data, bw2calc
  bw2data.projects.set_current("some BW2 project") # the project you activate needs to also contain the source (ecoinvent) database.
  
  u = Unfold("url to the data package.zip")
  u.unfold()
