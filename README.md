# hessff

`hessff` is a Windows desktop application for deriving bonded force-field parameters from external quantum-chemistry Hessians.

It currently supports:

- Gaussian `.fch` / `.fchk`
- ORCA `.hess`
- CP2K vibrational output plus bonded geometry
- Geometry + external Cartesian Hessian
- `DRIH`, `IHF`, `FHF`, and `PHF`
- GROMACS `.itp`, `.top`, `.gro`
- LAMMPS `.data`, `.params`

## What It Does

The app reads a structure and a Cartesian Hessian, derives harmonic bond, angle, and rigid-dihedral parameters, and writes:

- `parameters.json`
- GROMACS `.itp`, `.top`, `.gro`
- LAMMPS `.data`, `.params`

## Supported Geometry Files

- `.xyz`
- `.mol2`
- `.pdb`
- `.cif`

## Included Binary

- `hessff-gui.exe`

## Notes

There are two modes for CP2K: `weighted` and `unweighted`. The hessian files from CP2k are most probably unweighted. I tested this using hessian files for several molecules from both ORCA and CP2K and found that they both match assuming the hessian from CP2K to be unweighted. 
 

## License

This release is intended to be distributed under the MIT License.

- See `LICENSE` for the full license text.
