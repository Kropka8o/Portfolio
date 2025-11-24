<template>
  <div
      class="flex justify-between items-center py-3 px-6 bg-(--primary)"
  >
    <img src="https://i.pinimg.com/736x/2e/6a/ca/2e6aca416a3488415671dbe4f43c9049.jpg" class="size-10" />
  <nav class="flex justify-between items-center w-2/5 font-bold">
    <Button
        link="/"
        content="Home"
        bgColour="#a2f4fd" />
    <Button
      link="/projects"
      content="Projects"
      bgColour="#96f7e4" />
    <Button
        link="/about_me"
        content="About Me"
        bgColour="#a3b3ff" />
    <Button
        link="/pets"
        content="Pets"
        bgColour="#c4b4ff" />
  </nav>
  </div>
</template>
<script setup lang="ts">

</script>