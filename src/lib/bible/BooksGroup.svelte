<script type="ts">
  export let books: Array<{ name: string; color: string }>;
  import bookName from "$lib/data/names";
</script>

<div class="flex flex-wrap p-5">
  {#each books as book}
    <div class="w-1/5 p-1">
      <a href="/bible/{book.name}" class="text-white">
        <span class="p-1 block cursor-pointer hover:opacity-70 text-sm color-{book.color}">
          <span class="hidden md:block">{bookName(book.name, "cmn-hant")}</span>
          <span class="md:hidden">{bookName(book.name, "cmn-hant-abbr")}</span>
        </span>
      </a>
    </div>
  {/each}
</div>

<style>
  .color-1 {
    @apply bg-violet-500;
  }
  .color-2 {
    @apply bg-violet-600;
  }

  .color-3 {
    @apply bg-violet-800;
  }
</style>
