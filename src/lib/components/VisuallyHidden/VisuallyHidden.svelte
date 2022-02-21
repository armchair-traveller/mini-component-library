<script>
import { css } from '@stitches/core'
let forceShow = false

const cssWrapper = css({
  position: 'absolute',
  overflow: 'hidden',
  clip: 'rect(0 0 0 0)',
  height: '1px',
  width: '1px',
  margin: '-1px',
  padding: '0',
  border: '0',
})
</script>

<svelte:window on:keydown={(ev) => ev.key === 'Alt' && (forceShow = true)} on:keyup={() => (forceShow = false)} />

{#if forceShow}
  <slot />
{:else}
  <div class={cssWrapper} {...$$restProps}>
    <slot />
  </div>
{/if}
