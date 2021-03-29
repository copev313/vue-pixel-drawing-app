<template>
	<div>
		<Pixel
			isInColorPicker
			color="white"
			:current="color == 'white' ? true : false"
		/>
		<Pixel
			isInColorPicker
			color="lightblue"
			:current="color == 'lightblue' ? true : false"
		/>
		<Pixel
			isInColorPicker
			color="blue"
			:current="color == 'blue' ? true : false"
		/>
		<Pixel
			isInColorPicker
			color="darkblue"
			:current="color == 'darkblue' ? true : false"
		/>
		<Pixel
			isInColorPicker
			color="darkerblue"
			:current="color == 'darkerblue' ? true : false"
		/>
		<Pixel
			isInColorPicker
			color="darkestblue"
			:current="color == 'darkestblue' ? true : false"
		/>
		<Pixel
			isInColorPicker
			color="grey"
			:current="color == 'grey' ? true : false"
		/>
		<Pixel
			isInColorPicker
			color="greyer"
			:current="color == 'greyer' ? true : false"
		/>
		<Pixel
			isInColorPicker
			color="greyest"
			:current="color == 'greyest' ? true : false"
		/>
		<Pixel
			isInColorPicker
			color="brown"
			:current="color == 'brown' ? true : false"
		/>
		<Pixel
			isInColorPicker
			color="black"
			:current="color == 'black' ? true : false"
		/>
	</div>
</template>

<script>
import Pixel from "./Pixel";

export default {
	name: "ColorPicker",
	props: {
		color: String
	},
	methods: {
		changeColor: function (color) {
			alert(color);
		}
	},
	components: {
		Pixel
	}
};
</script>