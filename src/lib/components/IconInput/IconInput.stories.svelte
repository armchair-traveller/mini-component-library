<script>
import { Meta, Story, Template } from '@storybook/addon-svelte-csf'
import IconInput from './IconInput.svelte'
</script>

<Meta
  title="IconInput"
  component={IconInput}
  argTypes={{
    placeholder: {
      control: {
        type: 'text',
      },
    },
    icon: {
      control: {
        type: 'select',
        options: ['search', 'at-sign'],
      },
    },
    size: {
      control: {
        type: 'select',
        options: ['small', 'large'],
      },
    },
    label: {
      control: {
        type: 'text',
      },
    },
  }}
/>

<h1>IconInput</h1>
<Template let:args>
  <IconInput {...args} />
</Template>

<Story
  name="Default"
  args={{
    placeholder: 'Search…',
    label: 'Search',
    icon: 'search',
    size: 'small',
  }}
/>
