<script lang="ts" module>
	export type ButtonSize = 'small' | 'medium' | 'large';
</script>

<script lang="ts">
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

<button class="button {size}">
	{@render children()}
</button>

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



