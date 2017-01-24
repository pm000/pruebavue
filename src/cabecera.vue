<template>
	<div class="cabecera">
		<span @click="hola" class="titulo">{{ msg }}</span>
		<span @click="chau" class="titulo">Chau</span>
	</div>
</template>
<script>
	import Moment from 'moment'

	export default {
		name: 'cabecera',
		data() {
			return {
				msg: Moment().add(7, 'days')
			}
		},
		methods: {
			hola() {
				console.log("HOLA");
			},
			chau() {
				console.log("CHAU");
			}
		}
	}
</script>
<style>
	.cabecera {
		position: fixed;
		top: 0;
		left: 0;
		background-color: #F00;
		width: 100%;
	}

	.titulo {
		display: inline-block;
		margin: 10px;
	}
</style>