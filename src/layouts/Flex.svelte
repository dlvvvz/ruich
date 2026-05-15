<script lang="ts" module>
   export type FlexBlock = 'div' | 'main' | 'header' | 'section' | 'nav' | 'footer' | 'aside' | 'article';
   export type FlexDirection = 'col' | 'row' | 'col-reverse' | 'row-reverse';
   export type FlexItems = 'baseline' | 'center' | 'end' | 'start' | 'stretch';
   export type FlexContent = 'baseline' | 'center' | 'end' | 'start' | 'between' | 'around' | 'evenly' | 'stretch';

   export interface FlexProps {
      children: any;
      block?: FlexBlock;
      direction?: FlexDirection;
      items?: FlexItems;
      content?: FlexContent;
      padding?: string;
      gap?: string;
      wrap?: 'nowrap' | 'wrap' | 'wrap-reverse';
      class?: string;
   }
</script>

<script lang="ts">

   let {
      children,
      block = 'div',
      direction = 'col',
      items = 'start',
      content = 'start',
      padding = '0',
      gap = '0',
      wrap = 'nowrap',
      class: className = '',
   }: FlexProps = $props();
</script>

<svelte:element this={block} class="flex {direction} {wrap} {className}">
   {@render children()}
</svelte:element>

<style>
   .flex {
      display: flex;
      align-items: var(--items, start);
      justify-content: var(--content, start);
      padding: var(--padding, 0);
      gap: var(--gap, 0);
      flex-wrap: var(--wrap, nowrap);
   }

   .col {
      flex-direction: column;
   }
   .row {
      flex-direction: row;
   }
   .col-reverse {
      flex-direction: column-reverse;
   }
   .row-reverse {
      flex-direction: row-reverse;
   }

   .nowrap {
      flex-wrap: nowrap;
   }
   .wrap {
      flex-wrap: wrap;
   }
   .wrap-reverse {
      flex-wrap: wrap-reverse;
   }
</style>