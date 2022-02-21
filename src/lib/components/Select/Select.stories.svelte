<script>
import { Meta, Story } from '@storybook/addon-svelte-csf'
import Select from './Select.svelte'

let value = 'newest'
</script>

<Meta title="Select" component={Select} />

<h1>Select</h1>

<Story name="Default">
  <Select label="Sort" bind:value>
    <option value="newest">Newest Releases</option>
    <option value="price">Price</option>
    <option value="curated">Curated</option>
  </Select>
</Story>
