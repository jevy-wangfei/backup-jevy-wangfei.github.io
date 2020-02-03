---
layout: default
title: Add an image layer to react mapbox gl
dd: image-layer-to-react-mapbox-gl
category: timeline
tags: article
---

Images could be added to mapbox using a `Layer` and a `Source` component.

## Layer configuration
Prepare a source configuration by referenceing (this document)[https://docs.mapbox.com/mapbox-gl-js/style-spec/#sources-image]

```json
const Image_SOURCE_OPTIONS = {
    "type": "image",
    "url": "https://docs.mapbox.com/mapbox-gl-js/assets/radar.gif",
    "coordinates": [
        [-80.425, 46.437],
        [-71.516, 46.437],
        [-71.516, 37.936],
        [-80.425, 37.936]
    ] 
};
```
For base64 image, the url could be `data:image/png;base64,` + base64 image data:
```json
const Image_SOURCE_OPTIONS = {
    "type": "image",
    "url": "data:image/png;base64,...",
    "coordinates": [
        [-80.425, 46.437],
        [-71.516, 46.437],
        [-71.516, 37.936],
        [-80.425, 37.936]
    ] 
};
```

# Create a Source

```html
<Source id="source_id" tileJsonSource={RASTER_SOURCE_OPTIONS} />
```

## Create a Layer
Reference (react-mapbox-gl document)[https://github.com/alex3165/react-mapbox-gl/blob/master/docs/API.md#layer], the type could only be `symbol`, `line`, `raster`, ... 
```html
 <Layer type="raster" id="layer_id" sourceId="source_id" />
```