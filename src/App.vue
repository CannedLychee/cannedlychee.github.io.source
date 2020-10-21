<template>
<div id="page" @click="enter">
    <p id="welcome">CannedLychee</p>
    <svg xmlns="http://www.w3.org/2000/svg" class="icon" viewBox="0 0 1024 1024" t="1603245447559" p-id="1967" version="1.1" id="arrow">
        <path d="M 312.889 995.556 c -17.0667 0 -28.4444 -5.68889 -39.8222 -17.0667 c -22.7556 -22.7556 -17.0667 -56.8889 5.68889 -79.6444 l 364.089 -329.956 c 11.3778 -11.3778 17.0667 -22.7556 17.0667 -34.1333 c 0 -11.3778 -5.68889 -22.7556 -17.0667 -34.1333 L 273.067 187.733 c -22.7556 -22.7556 -28.4444 -56.8889 -5.68889 -79.6444 c 22.7556 -22.7556 56.8889 -28.4444 79.6444 -5.68889 l 364.089 312.889 c 34.1333 28.4444 56.8889 73.9556 56.8889 119.467 s -17.0667 85.3333 -51.2 119.467 l -364.089 329.956 c -11.3778 5.68889 -28.4444 11.3778 -39.8222 11.3778 Z" p-id="1968" />
    </svg>

</div>
<div id="footageL">
    <p id="markL">CannedLychee@2020</p>
</div>
<div id="footageR">
    <p id="markR">powered by vue3.js</p>
</div>
</template>

<script lang="ts">
export default {
    name: 'App',
    setup() {
        const enter = () => {
            window.location.href = 'https://github.com/CannedLychee'
        }
        return {
            enter
        }
    }
};
</script>

<style lang="scss">
@import url('./assets/fonts/fonts.scss');
@import url('./css/animation.scss');

html {
    height: 100%;
    padding: 0px;
    margin: 0px;
    background-image: linear-gradient(1500deg, #f3f4f5 0%, #c0c2ce 100%);
}

body {
    height: 100%;
    padding: 0px;
    margin: 0px;
    display: flex;
    align-items: center;
    justify-content: center;

}

#page {
    height: 70px;
    color: #fe667b;
    display: flex;
    display: -webkit-flex;
    flex-wrap: nowrap;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    user-select: none;
    cursor: pointer;

    #welcome {
        position: relative;
        left: 20px;
        width: 100%;
        font-size: 60px;
        line-height: 40px;
        text-align: end;
        font-family: OperatorMono-Book;
        // font-style: italic;
    }

    #arrow {
        position: relative;
        left: -20px;
        top: 3px;
        opacity: 0;
        width: 50px;
        height: 50px;
        fill: currentColor;
        color: #fe667b;
        transition-duration: 100ms;
    }

}

#page:hover #arrow {
    opacity: 1;
}

#footageL {
    position: absolute;
    line-height: 0px;
    bottom: 10px;
    left: 10px;
    color: #777777;
    user-select: none;

    #markL {
        font-family: OperatorMono-XLight;
        font-size: 10px;
    }
}

#footageR {
    position: absolute;
    line-height: 0px;
    bottom: 10px;
    right: 10px;
    color: #eeeeee;
    user-select: none;

    #markR {
        font-family: OperatorMono-XLight;
        line-height: 0px;
        font-size: 10px;
    }
}
</style>
