# Steady state heat/temperature solver in 2d

The provided code implements a specialized solver designed to find the steady-state temperature distribution in cross sections of walls that incorporate capillary heat exchangers. Capillary heat exchangers are widely used in various applications, such as building insulation and heat transfer systems, where they enable efficient use of heat pumps because, if properly set up, these systems require lower heating temperatures to achieve the required heat fluxes.

The solver utilizes a linear system of equations to model the temperature distribution within the wall cross section. It takes into account the geometry of the wall, including the presence of capillary heat exchangers and water regions, as well as boundary conditions such as heat flux, constant temperature or convective heat transfer.

The main function, `fit_water_t`, fits the required water temperature to achieve a target temperature and heat flux specified by the user. It iteratively solves the linear system using the scipy.spsolve function and adjusts the water temperature until convergence is achieved or the maximum number of iterations is reached. The resulting temperature distribution and the adjusted water temperature are returned.
Additional functions, such as `init_Ab` and `init_l`, handle the initialization of the geometry matrix, coefficient matrix (A), and right-hand side vector (b) for the linear system.
