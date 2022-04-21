<script>
export default {
    props: {
        innerText : String,
        pathToPhoto : String
    },
    mounted(){
        let text = this.$refs.text;
        let picture = this.$refs.image;
        text.innerText = this.innerText;
        picture.src = this.pathToPhoto;
    },
    methods: {
        MouseAction(isEnter){
            let Rect = this.$refs.blueRect;
            if (isEnter){
                Rect.style.opacity = '0.4';
            } else {
                Rect.style.opacity = '0';
            }
        },
        SignalTest(){
            alert("Это тестовая версия сайта");
        }
    }
}
</script>

<template lang="pug">
.card(@mouseenter='MouseAction(true)', @mouseleave='MouseAction(false)', @mousedown='SignalTest()')
    img.imageBackground(ref="image")
    .blueRect(ref="blueRect")
    p(ref="text") Text

</template>

<style lang="scss">
.card{
    width: 350px;
    height: 350px;
    margin-right: 30px;
    display: flex;
    .imageBackground{
        position: absolute;
        width: 350px;
        height: 350px;
    }
    .blueRect{
        position: absolute;
        width: 350px;
        height: 350px;
        background: rgb(0, 95, 163);
        opacity: 0;
    }
    p{
        color: #fff;
        font-family: 'Lato';
        font-style: normal;
        font-weight: 900;
        font-size: 24px;
        padding-left: 45px;
        padding-bottom: 45px;
        margin-top: auto;
        margin-bottom: 0em;
        z-index: 2;
    }
}

@media (max-width: 800px){
    .card{
        width: 80vw;
        height: 80vw;
        margin-right: 0px;
        margin-top: 15px;
        .imageBackground{
            width: 80vw;
            height: 80vw;
        }
        .blueRect{
            width: 80vw;
            height: 80vw;
        }
    }
}
</style>