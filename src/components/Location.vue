<template>
  <div class="position">
      {{loading}}
	<div v-if="loading!=='正在定位中....'" v-text="text"></div>
  </div>
</template>

<script>
	export default {
		data(){
			return {
				loading:'正在定位中....',
				text:''
			}
		},
		created(){
			this.dingwei();
		},
		methods: {
			dingwei(){
				var geolocation=new BMap.Geolocation();
				var that=this;
				geolocation.getCurrentPosition(function(r){
					if(this.getStatus()==BMAP_STATUS_SUCCESS){
						var province=r.address.province //返回当前省份
						var city=r.address.city//返回当前城市
						that.loading='定位成功';
						that.text=`你所在的省份是:${province},你所在的城市是:${city}`;
					}
				})
			}
		},
	}
</script>

<style>

</style>