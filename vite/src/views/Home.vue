<script setup lang="ts">
  import AMapLoader from '@amap/amap-jsapi-loader'
  
  AMapLoader.load({
    key: '', // 申请好的Web端开发者Key，首次调用 load 时必填
    version: '2.0', // 指定要加载的 JSAPI 的版本，缺省时默认为 1.4.15
    plugins: [
      'AMap.ToolBar',
      'AMap.Scale',
      'AMap.Overview',
      'AMap.MapType',
      'AMap.Geolocation'
    ], // 需要使用的的插件列表，如比例尺'AMap.Scale'等
    Loca: {
      version: '2.0'
    },
    AMapUI: {
      version: '1.1',
      plugins: []
    }
  })
    .then((AMap) => {
      let map = new AMap.Map('map-container')
    })
    .catch((e) => {
      console.log(e)
    })
  </script>
  
  <template>
    <main>
      <!-- <TheWelcome /> -->
      <div>
        222
        <div id="map-container"></div>
      </div>
    </main>
  </template>
  
  <style>
  #map-container {
    width: 800px;
    height: 500px;
  }
  </style>
  