<script context="module">
  import { browser } from "$app/env";
  import books from "$lib/data/books";
  import BooksGroup from "$lib/bible/BooksGroup.svelte";

  // ...but if the client-side router is already loaded
  // (i.e. we came here from elsewhere in the app), use it
  export const router = browser;

  // since there's no dynamic data here, we can prerender
  // it so that it gets served as a static asset in prod
  export const prerender = true;
</script>

<svelte:head>
  <title>Bible</title>
</svelte:head>

<div class="content">
  <BooksGroup books={books.hebrew} />
  <BooksGroup books={books.greek} />
</div>

<style>
  .content {
    width: 100%;
    max-width: var(--column-width);
    margin: var(--column-margin-top) auto 0 auto;
  }
</style>
