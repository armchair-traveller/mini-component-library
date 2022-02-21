<script>
import { Meta, Story } from '@storybook/addon-svelte-csf'
import VisuallyHidden from './VisuallyHidden.svelte'
import Icon from '$components/Icon.svelte'
</script>

<Meta title="VisuallyHidden" component={VisuallyHidden} />

<h1>VisuallyHidden</h1>

<Story name="Default">
  <Icon id="search" />
  <VisuallyHidden>Search</VisuallyHidden>
</Story>
