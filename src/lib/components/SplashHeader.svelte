<script>
	export let kicker = '';
	export let headline = '';
	export let deck = '';
	export let pubDate = '';
</script>

<div class="story-header">
	<span class="kicker">{kicker}</span>
	<h1>{headline}</h1>
	<hr class="rule" />
	<p class="deck">{deck}</p>
	<p class="byline">{pubDate}</p>
</div>

<style lang="scss">
	@use '$lib/styles' as *;

	.story-header {
		text-align: center;
		padding: var(--spacing-xxl) var(--spacing-md);
	}

	.kicker {
		display: block;
		font-family: var(--font-subheading);
		font-size: var(--font-size-xs);
		text-transform: uppercase;
		letter-spacing: var(--tracking-wide);
		color: var(--color-accent);
		margin-bottom: var(--spacing-sm);
	}

	.story-header h1 {
		font-family: var(--font-headline);
		font-size: var(--font-size-4xl);
		font-weight: 900;
		line-height: var(--leading-tight);
		color: var(--color-dark);
		margin-bottom: var(--spacing-sm);
	}

	.rule {
		border: none;
		border-top: var(--border-width-accent) solid var(--color-accent);
		width: var(--size-rule-short);
		margin: 0 auto var(--spacing-sm);
	}

	.deck {
		font-family: var(--font-body-copy);
		font-size: var(--font-size-lg);
		line-height: var(--leading-normal);
		color: var(--color-text);
		max-width: var(--measure-text-narrow);
		margin: 0 auto var(--spacing-sm);
	}

	.byline {
		font-family: var(--font-subheading);
		font-size: var(--font-size-sm);
		text-transform: uppercase;
		letter-spacing: var(--tracking-normal);
		color: var(--color-medium-gray);
	}

	@include mobile {
		.story-header h1 {
			font-size: var(--font-size-3xl);
		}

		.deck {
			font-size: var(--font-size-lg);
		}
	}
</style>
