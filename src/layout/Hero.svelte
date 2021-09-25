<script>
	import {fade,fly} from 'svelte/transition'
</script>
<h1 in:fly="{{x:600}}" ><span class="mark"><slot/></span></h1>
<style>
</style>