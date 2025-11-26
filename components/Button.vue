<template>
  <NuxtLink v-if="!isLinkATag"
            :to="linkURL"
            :style="baseStyle">
    <template v-if="imgSrc">
      <img :src="imgSrc" :alt="imgAlt ?? ''" :style="imgStyle" />
    </template>
    <template v-else>{{ props.content }}</template>
  </NuxtLink>

  <a v-else
     :href="linkURL"
     :style="baseStyle">
    <template v-if="imgSrc">
      <img :src="imgSrc" :alt="imgAlt ?? ''" :style="imgStyle" />
    </template>
    <template v-else>{{ props.content }}</template>
  </a>

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
    imgSrc: String,
    imgAlt: String,
    imgSize: {
      type: Number,
      required: false,
      default: 24,
    },
  })

  const baseStyle = computed(() => ({
    backgroundColor: props.bgColour ?? 'transparent',
    color: props.colour,
    border: props.imgSrc ? 'none' : '3px solid',
    borderColor: props.borderColour,
    borderRadius: `${props.radius}px`,
    padding: props.imgSrc ? '0' : '0.75rem 0.5rem'
  }))

  const imgStyle = computed(() => ({
    width: `${props.imgSize}px`,
    height: `${props.imgSize}px`,
    objectFit: 'contain',
    display: 'block',
    padding: '0',
    margin: '0',

  }))
</script>