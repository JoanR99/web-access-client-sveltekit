<script lang="ts">
	export let href: string;
</script>

<button class="btn">
	<a {href}>
		<p class="text-light"><slot /></p>
	</a>
</button>

<style lang="scss">
	@import '../theme';

	:global(.btn) {
		color: #fff;
		font-size: 1.6rem;
		display: inline-block;
		background-color: $color-action;
		border: none;
		padding: 0.8rem 2.5rem;
		border-radius: 30px;
		box-shadow: 0 5px 10px 0 rgba($color-black, 0.5);
		cursor: pointer;
		margin-top: 2rem;
		transition: all 0.2s;

		&:hover {
			box-shadow: 0 10px 20px 0.5px rgba($color-black, 0.5);
			transform: translateY(-3px);
		}
	}

	.text-light {
		color: white;
	}
</style>
