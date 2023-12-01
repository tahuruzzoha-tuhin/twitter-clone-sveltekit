
<script lang='ts'>
	import Sidebar from '$lib/components/comp/Sidebar.svelte';
    import '../app.css';
</script>


<sectio class="flex  mx-auto w-full max-w-6xl">
    <!-- sidebar -->
    <Sidebar/>
    <slot/>
    <!-- rightside -->
</sectio>