## Skill #7 - Working with Biomedical Image Analysis

The following code allows me to view multiple slices of brain images from functional magnetic resonance imaging (fMRI). Given that there were a total of 160 slices of images, I used a loop to show every 10th slice in a 4 x 4 array. 

I also show the images from different angles: top transverse plane and a saggital plane, respectively

```python
fig = plt.figure(figsize = [8, 12])
subplot_counter = 1
# Looping through subplots and drawing image
for ii in range(0, 160, 10):
    fig.add_subplot(4, 4, subplot_counter)
    plt.imshow(vol[ii], cmap = 'gray')
    plt.axis('off')
    plt.tight_layout()
    subplot_counter += 1
plt.show()
```

```python 
fig = plt.figure(figsize = [8, 12])
subplot_counter = 1
# Looping through subplots and drawing image
for ii in range(0, 160, 10):
    fig.add_subplot(4, 4, subplot_counter)
    plt.imshow((ndi.rotate(vol[:,:,ii], angle = 180)) , cmap = 'gray')
    plt.axis('off')
    plt.tight_layout()
    subplot_counter += 1
plt.show()
```
In this example, I was trying to locate areas within the brain that respond to certain visual stimuli more strongly. By statistical thresholding (applying a threshold of p < .0001), this code allows me to identify these prominent areas within the brain, indicated by the red color.

A thresholded Z map is overlayed on the underlying grayscale brain image. 'thresh_zstat' is a mask, whereby voxels above a threshold in thresh_zstat would take the values of fmri_zstat_data (), and values below the threshold will be np.nan.

```python 
thresh_zstat = np.where(fmri_zstat_data > z_thresh, fmri_zstat_data, np.nan)
fig = plt.figure(figsize = [6, 10])
subplot_counter = 1
# Loop through subplots and draw image
for ii in range(0, 27, 3):
    fig.add_subplot(3, 3, subplot_counter)
    plt.imshow(underlay[ :, :, ii], cmap = 'gray')
    plt.imshow(thresh_zstat[ :, :, ii], vmin = -8, vmax = 8, cmap = 'seismic')
    plt.axis('off')
    plt.tight_layout()
    subplot_counter += 1
# Render the figure
plt.show()

```


[Go to Skill #6]

[Go to Skill #8]

[Go to Main Page](https://alretagealbader.github.io/RetagePortfolio/)

