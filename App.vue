<template>
	
  <div id="app">
		<input type="text" v-model="text">
		<button @click="shanchu">按钮</button>
		<ul>
			<li v-for="(a,index) in list" :key="index" @click="asd(index)">
				{{a}}
			</li>
		</ul>
  </div>
	
</template>

<script>
	export default{
		data(){
			return({
				list:[
					"奥斯卡就",
					"51554",
					"5445"
				],
				text:''
			})
			
		},
		methods:{
			shanchu(){
				this.list.push(this.text);
				this.text=""
			},
			asd(index){
				this.list.splice(index,1)
			}
		}
	}
</script>

<style>
		li{
			list-style-type: none;
		}
		#app{
			margin: 0 auto;
			width: 220px;
			height: auto;
			background: #42B983;
			border: 1px solid aqua;
		}
		input{
			background: #00FFFF;
		}
		button{
			background: blueviolet;
			color: white;
		}
		 li{
			border-bottom: 1px solid #00FFFF;
		}
		
</style>
