<template>
  <header>
    <img src="@/assets/logo.svg" alt="Logo" class="logo" width="125" height="125" />
    <div class="wrapper">
      <h1>Hello World!</h1>
    </div>
  </header>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    color: #f2f2f2;
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>