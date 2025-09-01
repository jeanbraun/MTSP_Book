# Glacial erosion law

The main glacial erosion law that is used in many numerical models assumes that erosion rate is proportional to a power of the sliding velocity:
```{math}
:label: glacial
\dot\epsilon=K_gu_s^l
```
where $\dot\epsilon$ is erosion rate, $u_s$ the sliding velocity, and $K_g$ and $l$ two parameters. This law is derived from the work of {cite:t}`bernard1979theoretical-637` on glacial abrasion.

The main issue in glacial erosion model is to compute the sliding velocity. For this one must reconstruct the geometry and flow of ice on a given landscape (natural or synthetic). Various approaches have been used as we will now describe.