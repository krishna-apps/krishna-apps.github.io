<template>
  <div id="nav">
    <!-- <router-link to="/">Home</router-link>  -->
  </div>
  <router-view/>
</template>
<script>
export default {
  data() {
    return {
      showModal: false,
    };
  },
}
</script>

<style lang="scss">
#app, .home {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

/* reset */

* {
    max-width: 1600px;
    transition: 0.2s all cubic-bezier(0.65, 0.05, 0.36, 1);
    color: #2c3e50;
    cursor: unset;
    box-sizing: border-box;
}

body,
html,
#app {
    margin: 0;
    padding: 0;
    font-family: Avenir, Helvetica, Arial, sans-serif;
    max-width: 100%;
    background: #000;
}

a {
    cursor: pointer;
}


/* flex - services strip */

.svcContainer {
    max-width: 100%;
}

.svcContainer * {
    margin: auto;
}

.flx {
    display: flex;
    max-width: 950px;
    padding: 40px 0px;
    text-align: left;
    justify-content: center;
    align-items: center;
    margin: auto;
    overflow: hidden;
    flex-wrap: wrap;
}

.flx img {
    width: 420px;
    height: 300px;
    object-fit: contain;
    max-width: 100%;
}

.flxflip {
    flex-flow: row-reverse;
}

.slides {
    position: absolute;
    top: 0;
    width: 100%;
    overflow: hidden;
    height: 100vh;
}

.slides_spacing {
    height: 100vh;
}

.slide {
    position: absolute;
    top: 0;
    display: flex;
    align-content: center;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 100vh;
    padding-top: 50px;
    background-size: cover;
    background-position: center;
    flex-direction: column;
}

.slide h1 {
    padding: 10px;
    font-weight: 700;
    color: #151515;
    font-size: 3em;
    text-transform: capitalize;
    letter-spacing: 0.02em;
    font-family: "Poppins", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    font-weight: bold;
    text-align: center;
}

.slide p {
    color: #151515;
    padding: 10px;
    max-width: 520px;
    font-weight: bold;
    text-align: center;
    opacity: .8;
}

.spacer {
    flex-grow: 1;
}

.btn {
    padding: 18px 30px;
    background: #756aee;
    margin: auto;
    margin-top: 20px;
    color: white;
    border-radius: 5px;
    font-weight: bold;
    font-size: 1.5em;
    cursor: pointer;
    text-transform: capitalize;
    /* animation: grow-in-out 1s linear infinite alternate-reverse; */
    border: none;
}

@keyframes grow-in-out {
    to {
        transform: scale(1, 1);
    }
    from {
        transform: scale(.8, .8);
    }
}

.btn:hover {
    background: #000;
    animation-play-state: paused;
}

.modal {
    display: flex;
    align-content: center;
    align-items: center;
    justify-content: center;
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background: #000a;
    z-index: 100;
}

.modal-dialogue {
    background-color: #fff;
    border-radius: 5px;
    padding: 20px;
    min-width: 100px;
    min-height: 100px;
    text-align: center;
}

.modal-dialogue * {
    border-radius: 5px;
    outline: none;
}

fieldset {
    text-align: start;
}

.modal-dialogue p {
    position: relative;
    padding: 2%;
}

label {
    position: absolute;
    padding: 8px;
    opacity: .5;
}

.active {
    opacity: 1;
    color: blue;
    background: white;
    padding: 0 5px;
    font-size: 10px;
    left: 13px;
    top: 1px;
}

input,
textarea {
    padding: 5px;
    width: 96%;
}

input[type="submit"] {
    cursor: pointer;
    font-weight: bold;
}

input[type="submit"]:hover {
    background-color: green;
    color: white;
}


/* header */

nav {
    display: flex;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 50;
    background: transparent;
    align-items: center;
    align-content: center;
    justify-content: center;
}

nav.tr {
    background: white;
    box-shadow: #5555 0 0 0 2px;
    height: 60px;
}

.nav {
    display: flex;
    align-items: center;
    width: 100%;
    padding: 15px;
    height: 50px;
}

.nav-item {
    display: inline-block;
    position: relative;
    padding: 10px 0;
    margin: 20px;
    font-weight: bold;
    white-space: nowrap;
    cursor: pointer;
}

.nav-item * {
    text-decoration: none;
}

.nav-item:hover,
.popup li:hover,
.active {
    border-bottom: 2px solid #756aee;
    transform: translateY(-5%);
    filter: drop-shadow(0px 0px 15px #fff);
}

.nav img {
    height: 195%;
    margin: 0;
    cursor: pointer;
}

.nav img:hover {
    filter: drop-shadow(-4px 8px 10px #756aee);
    transition: all 0.1s;
}

.menu {
    padding: 5px;
    margin-right: 15px;
    transform: scale(0.7, 0.7);
    cursor: pointer;
}

#bar1,
#bar2,
#bar3 {
    width: 30px;
    height: 3px;
    background-color: #333;
    margin: 6px 0;
}

.open {
    transform: rotate(180deg) scale(0.7, 0.7);
}

.open #bar1 {
    transform: rotate(45deg) translate(10px, -7px);
    width: 20px;
}

.open #bar3 {
    transform: rotate(-45deg) translate(10px, 7px);
    width: 20px;
}

.popup {
    position: absolute;
    list-style: none;
    margin-top: 12px;
    margin-left: -10px;
    line-height: 38px;
    border-radius: 5px;
    box-shadow: 0px 0px 15px #0005;
    background: #fff;
    text-align: center;
    /* display: none; */
}

.nav-item:hover .popup {
    padding: 15px;
    display: inherit;
}

.footer {
    display: flex;
    padding-top: 30px;
    padding-bottom: 20px;
    flex-wrap: wrap;
    width: 100%;
    z-index: 1000;
    background: #1b1929aa;
}

footer * {
    color: white;
}

footer h1 {
    color: gray;
}

.tbl {
    margin-left: 0;
}

.tbl td {
    padding: 10px 20px;
}

td:first-child {
    color: #756aee;
    font-weight: bold;
    text-transform: capitalize;
}

td:not(:first-child):hover {
    cursor: pointer;
}

.ft {
    min-width: 250px;
    width: 25%;
    flex-grow: 1;
    margin: 0 25px;
    text-align: justify;
    min-height: 100%;
    letter-spacing: 0.025em;
}

.ft img {
    margin-top: 20px;
}

.form-el {
    position: relative;
}

.form-el input,
.form-el textarea {
    display: block;
    width: 92%;
    padding: 12px;
    margin: 10px 5px;
    font-size: 14px;
    font-weight: 500;
    letter-spacing: 0.025em;
    background-color: #aaa7;
    color: #efefef;
    border-radius: 2px;
    border: 2px solid #aaa2;
    outline: none;
}

.form-el input:focus,
.form-el textarea:focus {
    border: 2px solid #baf;
}

.form-el label {
    position: absolute;
    left: 10px;
    top: 7px;
    font-size: 14px;
}

label.active {
    left: 10px;
    top: -7px;
    font-size: 12px;
    border-radius: 8px;
    padding: 2px 8px;
    filter: none;
    background: #baf;
}

textarea {
    height: 150px;
    max-height: 250px;
    resize: vertical;
}

input.btn {
    background: #756aee;
    width: 97%;
    margin: auto;
}

input.btn:hover {
    cursor: pointer;
    background: #151515bb;
}

.form-validation {
    position: absolute;
    top: 2px;
    right: 35px;
    font-size: 12px;
    font-weight: bold;
    color: #ff543f;
    transition: all 0.3s;
    /* text-shadow: #f5543f 0 0 10px; */
}

.offering div {
    padding: 10px;
    display: flex;
    flex-wrap: nowrap;
    align-content: center;
}

.offering>div>div {
    width: 0px;
    height: 0px;
    transform: scaleY(0.1);
}

.offering>div:hover>span {
    transform: scale(2, 2) translateY(-5%);
    color: #756aee;
}

.offering>div:hover>div {
    width: 40px;
    height: 0.01em;
    background: #756aee;
}

.offering>div:hover {
    padding: 10px 20px;
    font-weight: bold;
    color: #756aee;
    cursor: pointer;
}

.copyright {
    text-align: center;
    color: white;
}

.fade-enter-active,
.fade-leave-active {
    transition: all .5s ease;
}

.fade-enter-from,
.fade-leave-to {
    opacity: 0;
}

.slide-up-enter-active,
.slide-up-leave-active,
.slide-enter-active,
.slide-leave-active {
    transition: all .75s ease-in-out;
}

.slide-leave-to {
    transform: translateX(-100%);
}

.slide-left-leave-to,
.slide-left-enter-from,
.slide-enter-from {
    transform: translateX(100%);
    opacity: 0;
}

.slide-up-leave-to,
.slide-up-enter-from {
    transform: translateY(80px) scale(.5, .5);
    opacity: 0;
}

.slide-left-enter-active,
.slide-left-leave-active,
.slide-right-enter-active,
.slide-right-leave-active {
    transition: all 1.25s ease-in-out;
}

.slide-right-leave-to,
.slide-right-enter-from {
    transform: translateX(-100%);
}

.bounce-enter-to {
    animation: bounce .5s linear;
}

.bounce-leave-from {
    animation: bounce .5s linear reverse;
}

@keyframes bounce {
    0% {
        transform: scale(0, 0);
    }
    70% {
        transform: scale(1.1, 1.1);
    }
    100% {
        transform: scale(1, 1);
    }
}
</style>
