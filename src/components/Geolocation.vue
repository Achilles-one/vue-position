<template>
  <div class="geo">
    <button @click="Geo()">点击获取位置</button>
    <div id="out"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      options: {
        enableHighAccuracy: true,
        timeout: 5000,
        maximumAge: 0,
      },
    };
  },
  methods: {
    Geo() {
      var output = document.getElementById("out");

      if (!navigator.geolocation) {
        output.innerHTML = "<p>您的浏览器不支持地理位置</p>";
        return;
      }

      navigator.geolocation.getCurrentPosition(
        (position) => {
          let lat = position.coords.latitude;
          let lng = position.coords.longitude;
          const pointBak = new BMap.Point(lng, lat);
          const convertor = new BMap.Convertor();
          convertor.translate([pointBak], 1, 5, function (resPoint) {
            if (resPoint && resPoint.points && resPoint.points.length > 0) {
              lng = resPoint.points[0].lng;
              lat = resPoint.points[0].lat;
            }
            const point = new BMap.Point(lng, lat);
            const geo = new BMap.Geocoder();
            geo.getLocation(point, (res) => {
                console.log(res);
            });
          });
        },
        () => {
          output.innerHTML = "无法获取您的位置";
        },this.options
      );
    },
  },
};
</script>

<style>
</style>