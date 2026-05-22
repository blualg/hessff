# hessff

`hessff` is a Windows desktop application for deriving bonded force-field parameters from external quantum-chemistry Hessians.

It currently supports:

- Gaussian `.fch` / `.fchk`
- ORCA `.hess`
- CP2K vibrational output plus bonded geometry
- Geometry + external Cartesian Hessian
- `DRIH`, `IHF`, `FHF`, and `PHF`
- GROMACS `.itp`
- LAMMPS data + parameter files

## What It Does

The app reads a structure and a Cartesian Hessian, derives harmonic bond, angle, and rigid-dihedral parameters, and writes:

- `parameters.json`
- GROMACS topology fragments
- LAMMPS data and parameter files

## Supported Geometry Files

- `.xyz`
- `.mol2`
- `.pdb`
- `.cif`

## Notes

- `.mol2` is the best choice when you already have bonded connectivity.
- `.pdb` and `.cif` can carry periodic cell information.
- For CP2K, use the dedicated `CP2K Output` mode with a geometry file.
- The app includes in-app help for accepted formats and method descriptions.

## Included Binary

- `hessff-gui.exe`

## License

This release is intended to be distributed under the MIT License.

- See `LICENSE` for the full license text.
