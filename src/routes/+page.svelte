<script>
  export let data;
	let title = 'Train Travel',
	excerpt = 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
	thumbnail = {
		src: ''
	},
	date = ''
</script>

<h1 class="text-center">{title}</h1>
<p class="text-center">{excerpt}</p>
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
	{#each data.blogs as { category, date, excerpt, thumbnail, title, slug }, index (index)}
		<div>
			<img
				class="w-full object-cover h-48 md:h-56 lg:h-72"
				src={thumbnail.src}
				alt={thumbnail.alt}
			/>
			<h2>{title}</h2>
			<blockquote>
				<b>Date</b> {date} <b>Category</b> <a href="/#">{category}</a>
			</blockquote>
			<p>{excerpt}</p>
			<p>
				<a href={`/blog/${slug}`}>
					Read more
				</a>
			</p>
		</div>
	{/each}
</div>