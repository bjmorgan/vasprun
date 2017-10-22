# vasprun
This repo is primarily used for extract useful information from vasprun.xml and postprocess data such as
- band gap calculation
- dos plot
- incar/potcar/poscar generation
- force analysys
- eigenvalue analysys

To use

$ python vasprun.py -h
```
Usage: vasprun.py [options]

Options:
  -h, --help            show this help message and exit
  -i incar file, --incar=incar file
                        export incar
  -p poscar file, --poscar=poscar file
                        export poscar
  -c cif file, --cif=cif file
                        export symmetrized cif
  -k kpoints file, --kpoints=kpoints file
                        kpoints list
  -d dos_plot, --dosplot=dos_plot
                        export dos plot
  -v vasprun, --vasprun=vasprun
                        path of vasprun.xml file, default='vasprun.xml'
  -f dos_plot, --showforce=dos_plot
                        dos plot
```

$ python vasprun.py -f yes

```
formula :   Sc4C4
efermi :   5.71888444
energy :   -65.82108919
metal :   True
gap :   -0.4621
+----+---------------------------------------+---------+-----------+
|    | kpoint                                | label   |    values |
|----+---------------------------------------+---------+-----------|
|  0 | [ 0.4375      0.08333333  0.375     ] | CBM     | -0.181984 |
|  1 | [ 0.0625      0.08333333  0.125     ] | VBM     |  0.280116 |
+----+---------------------------------------+---------+-----------+
+----+--------------+----------+-----------+
|    | functional   | labels   |   valence |
|----+--------------+----------+-----------|
|  0 | PBE          | Sc_sv    |        11 |
|  1 | PBE          | C        |         4 |
+----+--------------+----------+-----------+
+----+----------------------+-------------------------+
|    | lattice              | stress                  |
|----+----------------------+-------------------------|
|  0 | [3.478641, 0.0, 0.0] | [-4.62998221, 0.0, 0.0] |
|  1 | [0.0, 4.682565, 0.0] | [0.0, 1.73781963, 0.0]  |
|  2 | [0.0, 0.0, 6.176701] | [0.0, 0.0, 5.81088683]  |
+----+----------------------+-------------------------+
+----+--------------------------+---------------------------------+
|    | atom                     | force                           |
|----+--------------------------+---------------------------------|
|  0 | [0.0, 0.5, 0.606519]     | [0.0, 0.0, 0.02408274]          |
|  1 | [0.0, 0.0, 0.958081]     | [0.0, 0.0, 0.07723516]          |
|  2 | [0.5, 0.5, 0.041919]     | [0.0, 0.0, -0.07723516]         |
|  3 | [0.5, 0.0, 0.393481]     | [0.0, 0.0, -0.02408274]         |
|  4 | [0.5, 0.83775, 0.744469] | [0.0, 0.0691885, -0.00447732]   |
|  5 | [0.5, 0.16225, 0.744469] | [-0.0, -0.0691885, -0.00447732] |
|  6 | [0.0, 0.33775, 0.255531] | [0.0, 0.0691885, 0.00447732]    |
|  7 | [0.0, 0.66225, 0.255531] | [0.0, -0.0691885, 0.00447732]   |
+----+--------------------------+---------------------------------+

```
