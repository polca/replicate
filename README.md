# replicate
**RE**pository for **P**rospective **LI**fe **C**ycle **A**ssessment da**T**abas**E**s

This repository lists data packages that can be used together with the library [unfold](https://github.com/polca/unfold) 
to reproduce scenario-based or prospective life-cycle assessment databases locally.

Once you have identified the data package of interest (see table below),
you can extract the databases in a `brightway2` project by doing the following:

```python

    from unfold import Unfold
    import bw2data

    # name of the brightway project containing 
    # the source database (e.g., ecoinvent)
    bw2data.projects.set_current("some BW2 project")

    u = Unfold("url to the data package.zip")
    u.unfold()

```

Available data packages

| Database generator | IAM model | IAM scenario | Years available | Integrations | Source database       | Url |
| ------------------ | --------- | ------------ | --------------- | ------------ | --------------------- |-----|
| premise v.1.4.0    | IMAGE     | SSP2-Base    | 2005 - 2100     | electricity  | ecoinvent 3.8 cut-off |     |
| premise v.1.4.0    | REMIND    | SSP2-Base    | 2005 - 2100     | electricity  | ecoinvent 3.8 cut-off |     |