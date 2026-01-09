# plot_inductor

plot_inductor reads S-parameter data with 2 ports (*.s2p) 
for an RFIC inductor and plots the differential mode (symmetric) 
effective L, Q and R over frequency.

It support plotting multiple files, and to debug the reason for possible
differences, the tool plots the extracted effective series and shunt path
elements over frequency. This is really useful to see, for example, if the 
reason for a difference in Q factor is located in series path or shunt path loss.


# Prerequisites
The code requires Python3 with the skitkit-rf library.
https://scikit-rf.readthedocs.io/en/latest/tutorials/index.html

# Usage
Ro run the inductor plot and analysis, specify the *.s2p file(s) as commandline parameter.

example:
```
python plot_inductor.py measured.s2p simulated.s2p simulated2.s2p
```

The tool plots the effective L, Q and R in differential mode operation ...
![plot](./doc/png/RLQ.png)

... and the extracted effective series and shunt path elements over frequency.

![plot](./doc/png/elements.png)



