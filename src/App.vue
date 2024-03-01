<script>
import { RouterView } from 'vue-router';

export default{
  components: { RouterView },
  name: '',
}
</script>

<template>
		<main>
			<router-view></router-view>
		</main>
</template>

<style lang='scss'>
@use '@/assets/styles/font' as f;

*{
  transition: .2s;
}

</style>