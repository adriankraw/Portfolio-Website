<template>
    <nav id="footer">
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/art">Art</RouterLink>
      <RouterLink to="/about">About</RouterLink>
    </nav>  
</template>

<style scoped>
#footer {
  width: 100%;
  font-size: 12px;
  text-align: center;
}
nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}
</style>