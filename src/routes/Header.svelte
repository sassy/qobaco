<script>
	import { page } from '$app/stores';
</script>

<header>
	<nav class="flex space-x-4">
		<div class="rounded-md px-3 py-2 text-sm font-bold">Qobaco</div>
		<ul class="flex space-x-4">
			<li class="rounded-md px-3 py-2 text-sm font-medium" 
				aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Home</a>
			</li>
			<li class="rounded-md px-3 py-2 text-sm font-medium" 
			aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
				<a href="/about">About</a>
			</li>
		</ul>
	</nav>
</header>
