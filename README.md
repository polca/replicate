# replicate
**RE**pository for **P**rospective **LI**fe **C**ycle **A**ssessment da**T**abas**E**s

This repository lists data packages that can be used together with the library [unfold](https://github.com/polca/unfold) 
to reproduce scenario-based or prospective life-cycle assessment databases locally.

Once you have identified and downloaded the data package of interest (see table below),
you can extract the databases in a `brightway2` project by doing the following:

```python

    from unfold import Unfold
    import bw2data

    # name of the brightway project containing 
    # the source database (e.g., ecoinvent)
    bw2data.projects.set_current("some BW2 project")

    u = Unfold("filepath to the data package.zip")
    u.unfold()
```

You do not have to unfold all the scenario databases contained in the data package:

```python
    # unfold only the first and third scenario databases
    u.unfold(scenarios=[0, 2])
```

Available data packages
-----------------------

* Database generator: software or script used to generate the databases
* IAM model: integrated assessment model
* IAM scenario: socio-economic scenario (SSP) - climate scenario (RCP) combination
* Years available: years for which the databases are available
* Integrations: the sectoral modifications that are applied
* Source database: the source database
* Url: url to the data package


| Database generator | IAM model | SSP scenario | Climate scenario                                                                     | Years available | Sector      | Source database       | Url      |
| ------------------ | --------- |--------------|--------------------------------------------------------------------------------------|-----------------|-------------| --------------------- |----------|
| premise v.1.4.0    | IMAGE     | SSP2         | Base (RCP 6.0)<br/>RCP 2.6<br/>RCP 1.9                                               | 2005 - 2100     | electricity | ecoinvent 3.8 cut-off | [Link](https://doi.org/10.5281/zenodo.7470054) |
| premise v.1.4.0    | REMIND    | SSP2         | Base (RCP 6.0)<br/>NDC<br/>NPi<br/>PkBudg11500 (~RCP 2.6)<br/>PkBudg500 (~RCP 1.9)   | 2005 - 2100     | electricity | ecoinvent 3.8 cut-off | Link     |