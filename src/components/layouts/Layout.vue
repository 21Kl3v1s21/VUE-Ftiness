<script setup lang="ts">
defineProps<{
  handleChangeDisplay: (view: number) => void
}>()
</script>


<template>
    <header>
        <h1 class="text-gradient">THIEFGAINZ</h1>
    </header>
  <main>
    <slot />
  </main>
  <footer>
    <small>Created by</small>
    <a href="https://github.com/21Kl3v1s21" target="_blank">
        <img src="https://bondiwash.eu/cdn/shop/articles/Hnet.com-image.png?v=1624887252" alt="pfp">
        <p>Klevis</p>
        <i class="fa-brands fa-github"></i>
    </a>
  </footer>
</template>

<style scoped>
    header, footer, main {
        padding: 1rem;
        width: 100%;
        max-width: 700px ;
        margin: 0 auto;
    }

    main {
        flex: 1;
    }

    footer {
        display: flex;
        flex-direction: column;
        gap: 0.5rem;
        align-items: center;
        padding: 3rem 0;
        padding-bottom: 4rem;
    }

    footer a {
        display: flex;
        align-items: center;
        gap: 0.5rem;
        padding: 0.3rem;
        padding-right: 0.5rem;
        background: var(--background-muted);
        border-radius: 4rem;
        border: 1px solid transparent;
        transition-duration: 200ms;
        text-decoration: none;
    }

    footer a:hover {
        border-color: var(--color-link);
    }

    footer a img {
        max-width: 30px;
        aspect-ratio: 1 / 1;
        border-radius: 100%;
    }
</style>