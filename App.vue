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
					"123",
					"456",
					"789"
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
			background:gray;
		}
		input{
      height: 25px;;
			background: white;
		}
		button{
			background:white;
			color:black;
		}	
</style>