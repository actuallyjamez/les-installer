<template>
    <div id="app">
        <router-view></router-view>
    </div>
</template>

<script>
  export default {
    name: 'les-installer'
  }
</script>

<style>

    @import url("https://rsms.me/inter/inter-ui.css");

    @supports (font-variation-settings: normal) {
        html {
            font-family: 'Inter UI var alt', sans-serif;
        }
    }

    *,
    *::after,
    *::before {
        margin: 0;
        padding: 0;
        border: 0;
        box-sizing: inherit;
        transition: all 0.1s ease;
    }

    html {
        font-size: 16px;
        box-sizing: border-box;
        font-family: 'Inter UI', sans-serif;
        background-color: #0B0C11;
    }

    .download {
        display: flex;
        align-items: center;
        height: 56px;
    }

    .download button {
        align-items: center;
        justify-content: center;
        display: flex;
        padding: 16px 24px;
        background: #41B7C9 linear-gradient(to right, #DB5BDB 0%, #A384FB 50%, #41B7C9 100%);
        font-size: 1.3125em;
        font-weight: 600;
        border-radius: 8px;
        color: rgba(255, 255, 255, 0.9);
        box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.1);
        font-family: "Inter UI", sans-serif;
        transition: 200ms ease all;
        filter: hue-rotate(0deg) brightness(1);
        transform: scale(1, 1);
        width: 100%;

    }

    .loading button {
        background-size: 200% 200%;
        -webkit-animation: loading 1s ease infinite;
        -moz-animation: loading 1s ease infinite;
        animation: loading 1s ease infinite;

    }

    .clickable button:hover {
        filter: hue-rotate(-40deg) brightness(1.2);
        transform: scale(1.01, 1.01);
        cursor: pointer;

    }

    .download button svg {
        margin-right: 8px;
        line-height: 58px;
    }

    .download button svg path {
        fill: rgba(255, 255, 255, 0.9);
    }

    .download ul {
        list-style: none;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        margin-left: 16px;
        border-left: 1px solid #6B7187;
    }

    .download ul li {
        display: flex;
        align-items: center;
        color: #6B7187;
        font-size: 12px;
        font-weight: 500;
        line-height: 16px;
    }

    .download ul li svg {
        height: 16px;
        width: auto;
        margin-right: 4px;
    }

    .download ul li svg path {
        fill: #6B7187;
    }

    .download ul li:before {
        content: '';
        /*position: inline-block;*/
        border-bottom: 1px #6B7187 solid;
        -webkit-transform: translateY(-50%);
        transform: translateY(-50%);
        width: 8px;
        height: 1px;
        margin-right: 8px;
    }

    .download ul a {
        color: #6B7187;
        display: flex;
        align-items: center;
        line-height: 16px;
    }

    .download ul a svg {
        height: 16px;
        width: auto;
        margin-right: 4px;
    }

    .download ul a svg path {
        fill: #6B7187;
    }

    .download ul #beta {
        cursor: not-allowed;
        color: #6B7187 !important;
        text-decoration: line-through;
    }

    .centered {
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
        text-align: center;
    }

    button:focus {
        outline: 0;
    }

    .logo {
        margin-bottom: 50px;
    }

    #status {
        position: absolute;
        bottom: 75px;
        width: 100vw;
        /*background-color: #000000;*/
        padding: 5px;
        font-weight: 500;
        text-align: center;
        color: #6B7187;
    }

    .appbar {
        position: absolute;
        top: 0;
        width: 100vw;
        text-align: center;
        color: rgba(255, 255, 255, 0.70);
        font-weight: 500;
        padding: 5px;
        font-size: 14px;
        -webkit-app-region: drag;
    }

    #progress {
        position: absolute;
        height: 5px;
        width: 0%;
        box-shadow: 0px 0px 40px 1px #A384FB;
        background: #41B7C9 linear-gradient(to right, #DB5BDB 0%, #A384FB 50%, #41B7C9 100%);
        bottom: 0;
        /*transition: width 1s ease-in-out;*/
        transition: width 1s cubic-bezier(.785, .135, .15, .86)
    }

</style>
