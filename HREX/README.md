## Electrolyte-Osmotic-Coefficients
Jupyter notebook code called particle_nuber_calc.ipynb is used for calculating the required number of salt molecules for each desired concentration.

After performing alchemical calculations in GROMACS:

Using dhdl$.xvg files from alchemical calculations (where $ is the number of the corresponding alchemical state for that run) as input, python code 3nm_HREX.py is used to perform alchemical data analysis. To run the following flags are required:  
\' -f ' - File path for xvg file ex: output/dhdl0.xvg and output/dhdl1.xvg--> output/dhdl\
' -n ' - Number of Replicates\
' -s ' - Which Estimators should be used? (TI or MBAR or BAR or all)\
' -t ' - Temperature Simulations Run (K)\
' -r ' - Total Run Time(ps)\
' -e ' - Time at Which equilibrium was reached (ps)\
\
(example: $ python ../3nm_HREX.py -f dhdl -n 8 -s all -t 300 -r 10000 -e 1000)\
\
An output file called "FE_estimates.csv" will be generated for each concentration of salt. These are used as inputs for the jupyter notebook code called results_plots.ipynb to calculate and plot the corresponding chemical potentials and osmotic coefficients.

