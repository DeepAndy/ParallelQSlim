# QSlim
Parallel mesh simplification algorithm

```
Usage:
     nv_simplify_mesh --in <fine_mesh> --out <simplified_mesh> [options]

Allowed options:
  -h [ --help ]                    Produce help message
  --in arg                         Path fine input mesh
  --out arg                        Output path of simplified mesh
  -v [ --verbose ]                 Show debug output
  -f [ --force ]                   Enable file overwrite
  -s [ --smooth ]                  Smooth the mesh using Taubin
  -w [ --weight ] arg (=0)         Quadric error weighting strategy
                                    0 = none
                                    1 = area
                                   
  -r [ --reduction ] arg (=0)      The percentage reduction which we want to 
                                   achieve; e.g. 10 of the input mesh
  -i [ --max-iter ] arg (=1)       Max iterations to perform
  -t [ --threads ] arg (=1)        Number of threads
  -q [ --quadric ] arg (=3)        Type of quadric metric
                                    3 = [geometry]
                                    6 = [geometry, color]
                                    9 = [geometry, color, normal]
                                   
  -c [ --clusters ] arg (=1)       Number of clusters e.g.
                                    2 will be 2x2x2=8, 3x3x3=27 clusters
  -m [ --attributes ] arg (=1)     Input mesh attributes
                                    1 = [geometry]
                                    2 = [geometry, color, normal]
  -a [ --aggressiveness ] arg (=3) Aggressiveness (directly relates to the 
                                   maximum permissive error) [1.0-10.0]
```