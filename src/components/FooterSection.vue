<template>
  <footer class="footer">
    <p>Made with 🤍 in {{ new Date().getFullYear() }}</p>

    <p>awwwards.winner: 😅 let's hope soon!</p>

  </footer>
</template>

<script>
export default {
  name: 'FooterSection',
}
</script>

<style lang="scss">
.footer {
  font-size: 0.8rem;
  text-align: center;
  padding: 1rem;
  position: relative;
  z-index: 999;

  p {
    margin-bottom: 1rem;
  }

  a {
    color: var(--purple);
    font-weight: 700;
    transition: all 0.2s ease-out;

    &:hover {
      text-decoration: underline;
      filter: brightness(1.3);
    }
  }

  .awwwards {
    display: flex;
    justify-content: center;
    gap: 1rem;
  }
}
</style>
