<script>
import { Meta, Story, Template } from '@storybook/addon-svelte-csf'
import ProgressBar from './ProgressBar.svelte'
</script>

<Meta
  title="ProgressBar"
  component={ProgressBar}
  argTypes={{
    value: {
      control: {
        type: 'number',
        min: 0,
        max: 100,
      },
    },
    size: {
      control: {
        type: 'select',
        options: ['small', 'medium', 'large'],
      },
    },
  }}
/>

<h1>ProgressBar</h1>
<Template let:args>
  <ProgressBar {...args} />
</Template>

<Story name="Default" args={{ value: 50, size: 'medium' }} />
