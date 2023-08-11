<script>
export default {
	name: 'Section',
}
</script>

<script setup>

</script>

<template>
	<!--A grid with 2 big cols-->
	<div class="grid grid-cols-2">
		<!--A big col-->
		<div>
			<slot name="col1" />
		</div>
		<!--A big col-->
		<div>
			<slot name="col2" />
		</div>
	</div>
</template>