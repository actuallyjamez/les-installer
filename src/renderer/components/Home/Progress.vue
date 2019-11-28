<template>
    <div id="progress" :style="{width: `${progress}%`}" class="loading"></div>
</template>

<script>
  export default {
    name: 'Progress',
    props: {
      progress: {
        default: [0, 0, 0, 0],
        type: Array
      }
    }
  }
</script>

<style scoped>
    @-webkit-keyframes loading {
        0% {
            background-position: 0 52%
        }
        50% {
            background-position: 100% 49%
        }
        100% {
            background-position: 0 52%
        }
    }

    @-moz-keyframes loading {
        0% {
            background-position: 0 52%
        }
        50% {
            background-position: 100% 49%
        }
        100% {
            background-position: 0 52%
        }
    }

    @keyframes loading {
        0% {
            background-position: 0 52%
        }
        50% {
            background-position: 100% 49%
        }
        100% {
            background-position: 0 52%
        }
    }

    #progress {
        position: absolute;
        height: 5px;
        width: 0;
        box-shadow: 0 0 40px 1px #A384FB;
        background: #41B7C9 linear-gradient(to right, #DB5BDB 0%, #A384FB 50%, #41B7C9 100%);
        bottom: 0;
        /*transition: width 1s ease-in-out;*/
        transition: width 1s cubic-bezier(.785, .135, .15, .86)
    }
</style>
