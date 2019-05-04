<!-- Need to add font-awesome lib to lib/fa with fa.css and webfonts -->
<template>
<div class='radio-button-styles'>

<input type="radio" id="header1" value="h1" v-model="picked">
<label for="header1" class="label-text">header 1</label>
<br>
<input type="radio" id="header2" value="h2" v-model="picked">
<label for="header2" class="label-text">header 2</label>
<br>
<input type="radio" id="paragraph" value="p" v-model="picked">
<label for="paragraph" class="label-text">paragraph</label>
<br>
<span>Selected: {{ picked }}</span>
</div>
</template>

<script>
export default {
    name: 'RadioButton',
    data() {
        return {
            picked: 'h1'
        }
    }
}
</script>

<style scoped>
@import '../lib/fa/webfonts/fa.css';

.radio-button-styles {
	width: 175px;
	display: flex; 
	flex-direction: column; 
	align-items: flex-start; 
	border: 1px solid black; 
	padding-top: 10px;
	padding-bottom: 10px;
	padding-left: 10px; 
}

input[type="radio"] + .label-text:before{
	content: "\f111";
	font-family: "Font Awesome 5 Free";
	speak: none;
	font-style: normal;
	font-variant: normal;
	text-transform: none;
	line-height: 1;
	-webkit-font-smoothing:antialiased;
	width: 1em;
	display: inline-block;
	margin-right: 5px;
}

input[type="radio"]:checked + .label-text:before{
	content: "\f192";
	color: #007bff;
	animation: effect 250ms ease-in;
}

input[type="radio"]:disabled + .label-text{
	color: #aaa;
}

input[type="radio"]:disabled + .label-text:before{
	content: "\f111";
	color: #ccc;
}

/*Radio Toggle*/
label{
	position: relative;
	cursor: pointer;
	color: #666;
	font-size: 25px;
}

input[type="checkbox"], input[type="radio"]{
	position: absolute;
	right: 9000px;
}

.toggle input[type="radio"] + .label-text:before{
	content: "\f204";
	font-family: "Font Awesome 5 Free";
	speak: none;
	font-style: normal;
	font-weight: 900;
	font-variant: normal;
	text-transform: none;
	line-height: 1;
	-webkit-font-smoothing:antialiased;
	width: 1em;
	display: inline-block;
	margin-right: 10px;
}

.toggle input[type="radio"]:checked + .label-text:before{
	content: "\f205";
	color: #16a085;
	animation: effect 250ms ease-in;
}

.toggle input[type="radio"]:disabled + .label-text{
	color: #aaa;
}

.toggle input[type="radio"]:disabled + .label-text:before{
	content: "\f204";
	color: #ccc;
}
</style>
