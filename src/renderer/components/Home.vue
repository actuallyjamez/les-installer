<template>
    <div>
        <div class="appbar"><p>Install LES for Mac</p></div>
        <div class="centered">
            <div class="logo">
                <svg width="120px" height="56px" viewBox="0 0 120 56" version="1.1" xmlns="http://www.w3.org/2000/svg"
                     xmlns:xlink="http://www.w3.org/1999/xlink">
                    <defs>
                        <linearGradient x1="0%" y1="61.0946655%" x2="100%" y2="39.1111111%" id="linearGradient-1">
                            <stop stop-color="#DB5BDB" offset="0%"></stop>
                            <stop stop-color="#A384FB" offset="43.9189189%"></stop>
                            <stop stop-color="#41B7C9" offset="100%"></stop>
                        </linearGradient>
                    </defs>
                    <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                        <g id="Artboard" transform="translate(-613.000000, -170.000000)" fill="url(#linearGradient-1)"
                           fill-rule="nonzero">
                            <path d="M677,226 L677,218 L733,218 L733,226 L677,226 Z M661,226 L661,170 L669,170 L669,226 L661,226 Z M644.9945,226 L644.9945,170 L653,170 L653,226 L644.9945,226 Z M628.9945,226 L628.9945,170 L636.9945,170 L636.9945,226 L628.9945,226 Z M613,226 L613,170 L621,170 L621,226 L613,226 Z M725,210 L725,201.996 L733,201.996 L733,210 L725,210 Z M700.9955,210 L700.9955,201.996 L693,201.996 L693,193.996 L701,193.996 L701,186 L709,186 L709,194 L717,194 L717,202 L709,202 L709,210 L700.9955,210 Z M677,210 L677,201.996 L685,201.996 L685,210 L677,210 Z M725,193.9945 L725,186 L733,186 L733,194 L725,193.9945 Z M677,193.9945 L677,186 L685,186 L685,194 L677,193.9945 Z M677,177.9945 L677,170 L733,170 L733,178 L677,177.9945 Z"
                                  id="Union_1"></path>
                        </g>
                    </g>
                </svg>
            </div>
            <Lbutton clickable button-text="Install"></Lbutton>
        </div>
        <p id="status"></p>
        <Progress :progress="progress"></Progress>
    </div>
</template>

<script>
  import Progress from './Home/Progress'
  import Lbutton from './Home/Lbutton'

  export default {
    name: 'Home',
    components: {Lbutton, Progress},
    data () {
      return {
        progress: 0,
        installed: false,
        working: false,
        repos: {
          'base': 'Inversil/LESgit',
          '10.14': 'Inversil/LESgit'
        }
      }
    }
  }
</script>

<style scoped>

</style>
