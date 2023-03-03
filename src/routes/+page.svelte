<script lang="ts">
	import { goto } from '$app/navigation';

	function navigateToDetail(id: number) {
    	goto(`/questions/${id}`);
  	}

	let questions = [
	{id: 1, title: "最初の質問"},
	{id: 2, title: "2番目の質問"},
	{id: 3, title: "3番目の質問"},
	{id: 4, title: "4番目の質問"},
	{id: 5, title: "5番目の質問"},
	];
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<h1>
		Qobaco
	</h1>

	<h2>
		みんなから質問を集める、質問箱サービス
	</h2>
	<ul class="flex flex-col">
		{#each questions as question}
			<!-- svelte-ignore a11y-click-events-have-key-events -->
			<li 
				class="mx-5 my-2 py-5 border-2 rounded-sm"
				on:click={() => navigateToDetail(question.id)}>
				{question.title}
			</li>
		{/each}
	</ul>
</section>
