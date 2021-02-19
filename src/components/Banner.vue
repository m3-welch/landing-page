<template>
    <div class="banner-container">
        <div class="banner" @mouseenter='showUrl' @mouseleave="showName" :value="title">
            <span id="title" class="title" @click="click">{{ title }}</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Banner',
    data() {
        return {
            title: 'morgan welch',
        }
    },
    methods: {
        showUrl() {
            this.title = 'morganwel.ch'
        },
        showName() {document.getElementById("title").classList.add('animate__animated', 'animate__fadeInDown', 'animate__fast')
            this.title = 'morgan welch'
        },
        click() {
            window.location.href = process.env.VUE_APP_URL
        }
    }
}
</script>

<style scoped>

.title:hover{
    cursor: pointer;
}

.title {
    text-shadow: 0px 0px 25px rgba(0,0,0,0.75);
}

.banner {
    background: rgb(222,201,233);
    background: linear-gradient(90deg, rgba(222,201,233,1) 0%, rgba(216,192,231,1) 10%, rgba(210,183,229,1) 20%, rgba(193,158,224,1) 30%, rgba(177,133,219,1) 40%, rgba(160,108,213,1) 50%, rgba(145,99,203,1) 60%, rgba(129,90,192,1) 70%, rgba(114,81,181,1) 80%, rgba(98,71,170,1) 90%);
    color: #DAC3E8;
    height: 250px;
    width: 100%;
    margin: 0;
    text-align: center;
    line-height: 250px;
    font-family: 'Nunito', sans-serif;
    font-weight: bold;
    font-size: 75px;
    -webkit-box-shadow: 0px 20px 52px -17px rgba(0,0,0,0.75);
    -moz-box-shadow: 0px 20px 52px -17px rgba(0,0,0,0.75);
    box-shadow: 0px 20px 52px -17px rgba(0,0,0,0.75);
}

</style>