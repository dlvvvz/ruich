<script lang="ts" module>
   import type { Sizes, Appearances } from '$lib/ruich/types.ts';
   export type ButtonSize = Sizes;
   export type ButtonAppearance = Appearances;
</script>

<script lang="ts">
	import '$lib/app.css'
   import type { Snippet } from 'svelte';
	let {
		children,
      onclick = () => {},
		href,
		size = 'medium',
      appearance = 'outline',
	} : {
		children: Snippet,
      onclick: (e : MouseEvent) => void;
		href?: string,
		size?: ButtonSize,
      appearance?: ButtonAppearance;
	} = $props();
</script>
{#if href}
<a href="{href}" class="button {size} {appearance}" onclick={onclick}>
	{@render children()}
</a>
{:else}
<button class="button {size} {appearance}" onclick={onclick}>
	{@render children()}
</button>
{/if}

<style>
	.button{
		font-family: var(--font-family);
	}
	/* Sizes */
	.button{
		&.small{

		}
		&.medium{

		}
		&.large{

		}
	}
   /* Appearances */
   .button{
      &.outline{
         background-color: var(--color-background-box);
         border: 1px solid var(--color-border);
         color: var(--color-text);
      }
      &.theme{
         background-color: var(--color-theme);
         color: var(--color-theme-text);
      }
      &.neutral{
         background-color: var(--color-neutral);
         color: var(--color-neutral-text);
      }
   }
</style>