## Encoding a mesh as two DataFrames

The input file in the .ts format is converted to two DataFrames using the Save_sorting_pts.ipynb program.
* Inputs:
  - a .ts file, e.g., brain.ts
* Outputs:
  - two .csv files corresponding to the DataFrames $DF_V$ and $DF_T$


## Deriving connectivity relations
### Boundary relations
The TopoRela_boundary.ipynb program is used to extract the boundary relations for a mesh.
* Inputs:
  - the DataFrame $DF_T$
* Outputs:
  - a .parquet file in Spark, which is used to store the derived DataFrame corresponding to the desired boundary relation.
 
### Coboundary relations
The TopoRela_coboundary.ipynb program is used to extract the coboundary relations for a mesh.
* Inputs:
  - the DataFrame $DF_T$
* Outputs:
  - a .parquet file in Spark, storing the extracted DataFrame corresponding to the desired coboundary relation.

### Adjacent relations
The TopoRela_adjacent.ipynb program is used to extract the adjacent relations for a mesh.
* Inputs:
  - the DataFrame $DF_T$
* Outputs:
  - a .parquet file in Spark, storing the extracted DataFrame corresponding to the desired adjacent relation.

## Computing topological features
### Discrete vertex distortion
The Topo_distortion.ipynb is used to compute the discrete distortion for each vertex in a mesh.
* Inputs:
  - the DataFrames $DF_V$ and $DF_T$
* Outputs:
  - a DataFrame storing discrete distortion for each vertex in a mesh.
 
### Critical points
The Topo_CritPts.ipynb is used to extract critical points in a mesh.
* Inputs:
  - the DataFrames $DF_V$ and $DF_T$
* Outputs:
  - a DataFrame storing the critical size of each vertex in a mesh.
 
### Forman gradient
The Topo_Forman.ipynb is used to compute the Forman gradient in a mesh.
* Inputs:
  - the DataFrames $DF_V$ and $DF_T$
* Outputs:
  - a DataFrame storing critical simplices and simplex pairs in a mesh.
