<template>
  <div
      class="flex justify-between items-center py-3 px-6 bg-(--primary)"
  >
    <div class="flex justify-between w-full">
      <div class="w-7/8">
        <p>&copy; 2025 Cheryl</p>
      </div>
      <div class="flex justify-between items-center w-1/8">
        <Button
            id="snoesje-button"
            linkURL="/"
            imgSrc="https://i.pinimg.com/736x/2e/6a/ca/2e6aca416a3488415671dbe4f43c9049.jpg"
            imgAlt="Snoesje"
        />
        <Button
            isLinkATag
            linkURL="https://github.com/Kropka8o"
            imgSrc="/img/github-mark.svg"
            imgAlt="Github Logo"/>
        <Button
            isLinkATag
            linkURL="https://www.linkedin.com/in/cheryl-de-wijs"
            imgSrc="/img/LI-In-Bug.png"
            imgAlt="LinkedIn Logo"
            :imgSize="28"
        />
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">

</script>