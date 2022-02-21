<script>
import { COLORS } from '../../constants'
import Icon from '$components/Icon.svelte'
export let label, value
</script>

<select bind:value>
  <slot />
</select>
