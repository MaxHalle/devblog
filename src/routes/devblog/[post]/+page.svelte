<script>
  /** @type {import('./$types').PageData} */
	const { data } = $props();
  	import BlogCard from '$lib/components/blog-card.svelte';

</script>


<BlogCard {...data}>

</BlogCard>
