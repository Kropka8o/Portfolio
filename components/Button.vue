<template>
  <div :style="{'display': isLinkATag ? 'none' : 'block'}">
    <NuxtLink
        :href="linkURL"
        :style="{backgroundColor: isLinkATag ? 'black' : 'white', 'color': colour, 'border': '3px solid', 'border-color': borderColour, 'border-radius': radius + 'px'}"
        class="px-3 py-2">
      {{ content }}
    </NuxtLink>
  </div>

  <div :style="{'display': isLinkATag ? 'block' : 'none'}">
    <a
        :href="linkURL"
        :style="{ backgroundColor: isLinkATag ? 'red' : 'pink', 'color': colour, 'border': '3px solid', 'border-color': borderColour, 'border-radius': radius + 'px'}"
        class="px-3 py-2">
      {{ content }}
    </a>
  </div>

</template>

<script setup lang="ts">
  import {NuxtLink} from "#components";

  const props = defineProps({
    linkURL: String,
    isLinkATag: {
      type: Boolean,
      default: false
    },
    content: String,
    bgColour: String,
    colour: {
      type: String,
      required: false,
      default: '212e42'},
    borderColour: {
      type: String,
      required: false,
      default: '#212e42',
    },
    radius: {
      type: Number,
      required: false,
      default: 8,
      },
  })
</script>
<script setup lang="ts">
</script>