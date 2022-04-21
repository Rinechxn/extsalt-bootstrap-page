<script lang="ts">
	import { page } from "$app/stores";
	// import logo from './logo.svg';
</script>

<header class="flex justify-between w-full fixed bg-[#0e0e0e]">
	<div class="w-10 h-10 flex items-center justify-center text-white">
		<div class="w-[50%]">
			<a href="/">
				<svg
					xmlns="http://www.w3.org/2000/svg"
					viewBox="0 0 158 196.83"
				>
					<defs>
						<style>
							.cls-1 {
								fill: none;
								stroke: #fff;
								stroke-miterlimit: 10;
								stroke-width: 8px;
							}
							.cls-2 {
								fill: #fff;
							}
							.cls-3 {
								fill: #0affaf;
							}
							.cls-4 {
								font-size: 67.79px;
								font-family: Montserrat-Bold, Montserrat;
								font-weight: 700;
							}
						</style>
					</defs>
					<g id="Layer_2" data-name="Layer 2">
						<g id="Layer_5" data-name="Layer 5">
							<polygon
								class="cls-1"
								points="4 192.83 154 192.83 154 68 124 28 34 28 4 68 4 192.83"
							/>
							<polyline
								class="cls-1"
								points="34 28 4 28 4 4 154 4 154 28 123.86 28"
							/>
							<rect
								class="cls-2"
								x="4"
								y="90.04"
								width="150"
								height="102.78"
							/>
							<polygon
								class="cls-3"
								points="36.09 51.25 40.21 59.6 49.43 60.94 42.76 67.44 44.33 76.62 36.09 72.29 27.85 76.62 29.42 67.44 22.75 60.94 31.97 59.6 36.09 51.25"
							/>
							<polygon
								class="cls-3"
								points="64.92 51.25 69.05 59.6 78.26 60.94 71.59 67.44 73.17 76.62 64.92 72.29 56.68 76.62 58.26 67.44 51.59 60.94 60.8 59.6 64.92 51.25"
							/>
							<polygon
								class="cls-3"
								points="93.08 51.25 97.2 59.6 106.41 60.94 99.74 67.44 101.32 76.62 93.08 72.29 84.83 76.62 86.41 67.44 79.74 60.94 88.95 59.6 93.08 51.25"
							/>
							<polygon
								class="cls-3"
								points="121.91 51.25 126.03 59.6 135.25 60.94 128.58 67.44 130.15 76.62 121.91 72.29 113.67 76.62 115.24 67.44 108.57 60.94 117.79 59.6 121.91 51.25"
							/>
							<text class="cls-4" transform="translate(22.75 168)"
								>&lt;/&gt;</text
							>
						</g>
					</g>
				</svg>
			</a>
		</div>

	</div>

	<nav class="flex justify-center text-white">
		<!-- <svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L1,2 C1.5,3 1.5,3 2,3 L2,0 Z" />
		</svg> -->
		<ul>
			<li class:active={$page.url.pathname === "/"}>
				<a sveltekit:prefetch href="/">Home</a>
			</li>
			<li class:active={$page.url.pathname === "/about"}>
				<a sveltekit:prefetch href="/about">About</a>
			</li>
			<li class:active={$page.url.pathname === "/todos"}>
				<a sveltekit:prefetch href="/todos">Todos</a>
			</li>
		</ul>
		<!-- <svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L0,3 C0.5,3 0.5,3 1,2 L2,0 Z" />
		</svg> -->
	</nav>

	<div class="corner">
		<!-- TODO put something else here? github link? -->
	</div>
</header>

<style>

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	li.active::before {
		--size: 6px;
		content: "";
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--accent-color);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 1em;
		color: var(--heading-color);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--accent-color);
	}
</style>
