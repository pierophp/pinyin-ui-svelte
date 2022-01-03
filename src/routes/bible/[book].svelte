<script type="ts">
  export let chapters = [
    1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 1,
    2, 3, 4, 5, 6, 7, 8, 9, 10, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10,
  ];
</script>

<div class="flex space-x-2">
  {#each chapters as chapter}
    <a href="#" class="text-white">
      <span
        class="block bg-gray-400 gap-1 w-[45px] h-[45px] text-center leading-[45px] hover:bg-sky-800"
        >{chapter}</span
      >
    </a>
  {/each}
</div>
