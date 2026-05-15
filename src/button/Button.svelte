<script lang="ts" module>
	export type ButtonSize = 'small' | 'medium' | 'large';
</script>

<script lang="ts">
	import '$lib/app.css'
	let {
		children,
		href,
		size = 'medium' as ButtonSize,
	} : {
		children: any,
		href? string,
		size?: ButtonSize,
	} = $props();
</script>
{#if href}
<a href="{href}" class="button">
	{@render children()}
</a>
{:else}
<button class="button {size}">
	{@render children()}
</button>
{/if}

<style>
	.button{
		
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
</style>



