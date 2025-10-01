Note that due to an [issue](https://github.com/scikit-image/scikit-
image/issues/6346) (now fixed) in the canny edge detector for a specific
skimage version, your code might find a line on the _camera_ image that
corresponds to one of the image edges, which is different than my results. To
avoid this problem, use this keyword argument:

imedges = skimage.feature.canny(im, **mode="nearest"**)