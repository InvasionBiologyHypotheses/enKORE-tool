<script>
  import { page } from "$app/stores";
</script>

<header>
  <nav>
    <ul>
      <li><a href="/sinas/qs">QuickStatements</a></li>
      <li><a href="/sinas/taxa">taxa</a></li>
    </ul>
  </nav>
</header>

<slot />

<style>
  ul {
    display: flex;
    gap: 2rem;
  }
  li {
    list-style-type: none;
  }
</style>
