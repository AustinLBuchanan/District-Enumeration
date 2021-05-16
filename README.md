# District-Enumeration

Some short code for enumerating districts and districting plans. The data originates from the 2010 census.

- [Maine-enumeration.ipynb](https://github.com/AustinLBuchanan/District-Enumeration/blob/main/Maine-enumeration.ipynb) enumerates all feasible districts for Maine at the county level. For a district to be contiguous, it should have population within +/-0.5% of the ideal population and it should be contiguous on the map. Since Maine has 2 congressional districts, this is almost enough to generate all districting plans. We can just see whether the district's complement satisfies these properties.

- [New-Mexico-plan-enumeration.ipynb](https://github.com/AustinLBuchanan/District-Enumeration/blob/main/New-Mexico-plan-enumeration.ipynb) enumerates all feasible districting plans for New Mexico at the county level. The code first enumerates all feasible districts that do not lead to underpopulated enclaves. That is, if district D is to be a plausible choice, then G-D should not have a component whose population is less than L=0.995*(ideal population). Then, the code loops over all choices for district 1 and district 2. If they are disjoint and the other vertices form a feasible district, then it draws the three-district plan.

A video of all 365 New Mexico plans can be [found here](https://www.youtube.com/watch?v=pMJHDoIK8og). The video was made with Blender ([tutorial](https://www.youtube.com/watch?v=LmxaYwmewWs)), using the [365 .png plan files](https://github.com/AustinLBuchanan/District-Enumeration/tree/main/NM-plans).

To speed up the computations, the codes use [vertex orderings](https://github.com/hamidrezavalidi/Political-Districting-to-Minimize-Cut-Edges/blob/master/results/results_for_config-table11-3600-2k/log-file.txt) from a [previous paper](https://github.com/hamidrezavalidi/Political-Districting-to-Minimize-Cut-Edges).


