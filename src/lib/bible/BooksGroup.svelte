<script type="ts">
	export let books;
	import bookName from '$lib/data/names';
</script>

<div class="flex flex-wrap p-5">
	{#each books as book}
		<div class="w-1/5 p-1">
			<div class="p-1 bg-violet-600 text-white cursor-pointer hover:opacity-70 ">
				<span class="sm:md:hidden">{bookName(book.name, 'cmn-hant')}</span>
				<span class="lg:xl:2xl:hidden">{bookName(book.name, 'cmn-hant-abbr')}</span>
			</div>
		</div>
	{/each}
</div>
