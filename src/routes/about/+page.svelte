<script>
	let title = 'About Me';
	let desc = 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam, mollitia laborum. Molestias.';
	let image = {
		src: 'https://i.imgur.com/iO8RUVr.jpeg',
		alt: 'myself',
	};
</script>

<svelte:head>
	<title>{title}</title>
	<meta property="og:title" content={title} />
	<meta name="twitter:title" content={title} />
	<meta name="description" content={desc} />
	<meta property="og:description" content={desc} />
	<meta name="twitter:description" content={desc} />
	<meta property="og:image" content={image.src} />
	<meta name="twitter:image" content={image.src} />
</svelte:head>

<h1 class="text-center">{title}</h1>
<div class="mx-auto max-w-prose">
	<p class="text-center">{desc}</p>

	<img class="h-96 w-full object-cover object-top" src={image.src} alt={image.alt} />

	<p class="">
		Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ipsum, amet placeat atque dolore
		eaque est quam maiores cupiditate recusandae provident itaque libero adipisci dolor. Iusto
		blanditiis ducimus doloribus perspiciatis tenetur! <a href="/blog/ipsum">Lorem, ipsum</a>.
	</p>
	<ul class="">
		<li>
			Lorem ipsum dolor sit. <a href="/">Lorem</a>.
		</li>
		<li>Lorem ipsum dolor sit, amet consectetur adipisicing.</li>
	</ul>
	<h4 class="text-right">Signature</h4>
	<h2 class="text-right">Lorem, ipsum.</h2>
</div>
