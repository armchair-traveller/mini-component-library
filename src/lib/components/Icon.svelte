<script>
import { css } from '@stitches/core'
import Search from '@svicons/feather/icons/search.svelte'
import AtSign from '@svicons/feather/icons/at-sign.svelte'
import ChevronDown from '@svicons/feather/icons/chevron-down.svelte'

export let id,
  size = 25,
  strokeWidth = 1

/**
 * We're given this component "for free" since it's really more
 * specific to vite and unplugin-icons. Feel free to read if you're
 * interested, but otherwise you can rely on our docs to learn its
 * API / which props it takes.
 * The reduce is simply creating an obj with kebab-cased keys for the ID.
 */
const icons = [Search, AtSign, ChevronDown].reduce(
  (dict, v) => (dict[v.name.replace(/([a-z0–9])([A-Z])/g, '$1-$2').toLowerCase()] = v) && dict,
  {}
)
if (!icons[id]) throw new Error(`No icon found for ID: ${id}`)
</script>

<svelte:component
  this={icons[id]}
  {...$$restProps}
  class={css({ display: 'block', strokeWidth: `${strokeWidth}px`, width: `${size}px`, height: `${size}px` })}
  color="currentColor"
  {size}
/>
