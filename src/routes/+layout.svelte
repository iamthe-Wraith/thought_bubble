<script lang="ts">
  import './style.css';
  import dayjs from 'dayjs';

  const now = dayjs();
</script>

<header>
  <a href="/">Thought Bubble</a>
</header>

<main>
  <slot />
</main>

<footer>
  <div>© {now.format('YYYY')}</div>
</footer>

<style>
  header,
  footer {
    display: flex;
    align-items: center;
    height: 5rem;
    padding: 1rem;
  }

  header {
    background: var(--primary);
  }

  main {
    min-height: calc(100vh - 10rem);
    padding: 1rem;
  }

  footer {
    border-top: 1px solid var(--primary);
  }
</style>