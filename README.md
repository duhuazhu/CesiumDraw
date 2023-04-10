## 在cesium 中绘制 polygon , polyline , point 
npm i cesiumgraphing
```js
import { polygon, polyline, drawPoint } from 'cesiumgraphing'
let options = {
    point: {
        show: true,
        pixelSize: 10,
        color: '#0008ff',
    },
    polygon: {
        material: Color.fromCssColorString("#33fc05").withAlpha(0.6),
    },
    dataSourceName: 'drawPolygon',
};
polygon(viewer, options, function (dataSource, positions, wgs84) {});

let options = {
    point:{
        show: false,
    },
    polyline:{
        clampToGround: true,
        material: Color.fromCssColorString("#67ADDF").withAlpha(0.7),
    },
    multiple: true,
    dataSourceName: 'drawPolyline',
};
polyline(viewer, options, function (dataSource, positions, wgs84) {});

let options = {
    point: {
        pixelSize: 10,
        color: Color.fromCssColorString("#0008ff"),
    },
    dataSourceName: "drawPoint",
};
drawPoint(viewer, options, function (dataSource, wgs84) {});
  
```
