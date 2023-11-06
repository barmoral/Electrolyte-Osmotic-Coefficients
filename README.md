## Electrolyte-Osmotic-Coefficients
Using dhdl$.xvg files from alchemical calculations (where $ is the number of the corresponding lambda for that run) as input, python code 3nm_HREX.py is run to perform alchemical data analysis. To run the following flags are required:  
\' -f ' - File path for xvg file ex: output/dhdl0.xvg and output/dhdl1.xvg--> output/dhdl\
' -n ' - Number of Replicates\
' -s ' - Which Estimators should be used? (TI or MBAR or BAR or all)\
' -t ' - Temperature Simulations Run (K)\
' -r ' - Total Run Time(ps)\
' -e ' - Time at Which equilibrium was reached (ps)\
\
(example: $ python ../3nm_HREX.py -f dhdl -n 8 -s all -t 300 -r 10000 -e 1000)\
\
After obtaining MBAR free energy for water and a solution of salt, use these numbers as input for the jupyter code osm_coef.ipynb to calculate the corresponding osmotic coefficients.

