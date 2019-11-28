<template>
    <div id="button" class="download" :class="{clickable: clickable}">
        <button>
            {{buttonText}}
        </button>
    </div>
</template>

<script>
  export default {
    name: 'Lbutton',
    props: {
      clickable: Boolean,
      buttonText: String
    }
  }
</script>

<style scoped>

</style>
