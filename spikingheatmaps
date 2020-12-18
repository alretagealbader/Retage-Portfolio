## Working with single unit data

This loop yields heat maps that visually represent neural spiking in 3 different neurons from a list ['m1_6' 'm3_11' 'm6_3a2'] 
in response to a visual input in varying conditions (CTL/ADAPT)

The y axis shows the number of spikes and the x axis shows the time (ms) during the experimental trial. 

```python
fig = plt.figure(figsize = [10,10])
subplot_counter = 1 # used to track subplots

for neuron in neuron_labels: #neuron_labels is a list of neuron names
    for cond in cond_labels: #con_labels is a list of condition names 
        ax = fig.add_subplot(len(neuron_labels), len(cond_labels), subplot_counter)
        aa = plt.imshow(psth_df3.loc[neuron, cond, :], origin = 
              'lower', cmap = 'magma', interpolation = 'bilinear', aspect = 5)
        
        cb = fig.colorbar(aa, shrink=0.5)
        cb.ax.set_ylabel('Number of Spikes')

        plt.title('Neuron ' + neuron + ': ' + cond)

        xticks = range(0, len(time_bins), 10)
        plt.xticks(xticks,
                   time_bins[xticks])
        if neuron == neuron_labels[-1]:
            plt.xlabel('Time (ms)')

        plt.yticks([x for x,y in enumerate(contr_labels)],
                   [x for x in contr_labels])

        if cond == cond_labels[0]:
            plt.ylabel('Stimulus Contrast')
        subplot_counter += 1

plt.show()
```
< width = '300' src = 'spikepicture.png' >

[Go to main page](https://alretagealbader.github.io/RetagePortfolio/)

