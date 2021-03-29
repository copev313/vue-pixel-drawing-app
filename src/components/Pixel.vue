<template>
	<div
		@click="handleClick"
		:class="['pixel', color, current ? 'current' : '']"
	></div>
</template>

<script>
export default {
	name: "Pixel",
	props: {
		color: String,
		current: Boolean,
		isInColorPicker: Boolean,
		isInCanvas: Boolean,
		index: Number
	},
	methods: {
		handleClick: function () {
			if (this.isInColorPicker) {
				this.$root.$emit("updatecolor", this.color);
			}
			if (this.isInCanvas) {
				this.$root.$emit("clickedpixel", this.index);
			}
		}
	}
};
</script>

<style scoped>
.pixel {
	border: 1px solid lightgray;
	width: 30px;
	height: 30px;
	box-sizing: border-box;
}
.pixel.current {
	border: 4px solid black;
}
.white {
	background-color: white;
}
.lightblue {
	background-color: rgb(0, 188, 212);
}
.blue {
	background-color: rgb(3, 169, 244);
}
.darkblue {
	background-color: rgb(33, 150, 243);
}
.darkerblue {
	background-color: rgb(18, 83, 136);
}
.darkestblue {
	background-color: rgb(19, 63, 99);
}
.grey {
	background-color: grey;
}
.greyer {
	background-color: rgb(86, 88, 90);
}
.greyest {
	background-color: rgb(53, 54, 56);
}
.brown {
	background-color: rgb(87, 59, 23);
}
.black {
	background-color: black;
}
</style>