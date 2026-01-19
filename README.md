# plot_inductor

plot_inductor reads S-parameter data with 2 ports (*.s2p) 
for an RFIC inductor and plots the differential mode (symmetric) 
effective L, Q and R over frequency.

It support plotting multiple files, and to debug the reason for possible
differences, the tool plots the extracted effective series and shunt path
elements over frequency. This is really useful to see, for example, if the 
reason for a difference in Q factor is located in series path or shunt path loss.

To run the inductor plot and analysis, specify the *.s2p file(s) as commandline parameter.

example:
```
python plot_inductor.py measured.s2p simulated.s2p simulated2.s2p
```

The tool plots the effective L, Q and R in differential mode operation ...
![plot](./doc/png/RLQ.png)

... and the extracted effective series and shunt path elements over frequency.

![plot](./doc/png/elements.png)



# plot_snp

plot_snp reads one or more S-parameter files with any number of ports (*.s*p) 
and plots magnitude (dB) and phase of all selected parameters.

To run the inductor plot and analysis, specify the *.snp file(s) and the requested S-parameters as commandline parameter. Order does not matter. Default is S11.

example:
```
python plot_snp.py data.s2p S21 

python plot_snp.py measured.s2p simulated.s2p S11 S21

```

The tool plots all files with the specified parameter(s)

![plot](./doc/png/plot_snp.png)




# Prerequisites
The code requires Python3 with the skitkit-rf library.
https://scikit-rf.readthedocs.io/en/latest/tutorials/index.html



