<script lang="ts">
	import { page } from '$app/stores';

	$: isEvaluation = $page.url.pathname == '/evaluation';
	$: isContrast = $page.url.pathname == '/contrast';

	function isRef(ref: boolean) {
		if (ref) return 'navbar__link active';
		else return 'navbar__link';
	}
</script>

<header class="header">
	<nav class="navbar container">
		<a href="/"><span class="main-logo">WEBACCESS</span></a>
		<ul class="navbar__list">
			<li class="navbar__item">
				<a href="evaluation" class={isRef(isEvaluation)}><span>Evaluation</span></a>
			</li>
			<li class="navbar__item">
				<a href="contrast" class={isRef(isContrast)}><span>Contrast</span></a>
			</li>
		</ul>
	</nav>
</header>

<style lang="scss">
	@import '../theme';

	.header {
		height: 6rem;
		display: flex;
		align-items: center;
	}

	.navbar {
		width: 100%;
		display: flex;
		justify-content: space-between;
		align-items: center;
		z-index: 100;

		&__list {
			display: flex;
			list-style: none;
			column-gap: 2rem;
		}

		&__link {
			font-family: $font-heading;
			font-size: 1.6rem;
			text-decoration: none;
			color: $color-black;
			transition: all 0.2s;

			&:hover {
				color: $color-action;
			}
		}
	}

	.main-logo {
		font-family: $font-heading;
		font-size: 2.4rem;
		color: $color-primary;
		font-weight: 900;
		text-decoration: none;
	}

	.active {
		color: $color-action;
	}
</style>
