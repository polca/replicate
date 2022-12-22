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

| Database generator | IAM model | IAM scenario                                | Years available | Integrations | Source database       | Url      |
| ------------------ | --------- |---------------------------------------------| --------------- | ------------ | --------------------- |----------|
| premise v.1.4.0    | IMAGE     | SSP2-Base<br/>SSP2-RCP 2.6<br/>SSP2-RCP 1.9 | 2005 - 2100     | electricity  | ecoinvent 3.8 cut-off | [Link](https://doi.org/10.5281/zenodo.7470054) |
| premise v.1.4.0    | REMIND    | SSP2-Base<br/>SSP2-RCP 2.6<br/>SSP2-RCP 1.9 | 2005 - 2100     | electricity  | ecoinvent 3.8 cut-off | Link     |