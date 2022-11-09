<header>
	<nav>
		<ul>
			<li><a href="/">🏠</a></li>
			<li><a href="/corpus">Corpus</a></li>
			<li><a href="/sinas">Sinas</a></li>
			<li><a href="/logs">Logs</a></li>
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
