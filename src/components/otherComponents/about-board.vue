<script>
export default {
    props: {
        heading : {
            Type : String,
            default : '90'
        },
        text : {
            Type : String,
            default : 'Завершено крупных сделок'
        }
    },
    methods: {
        ActiveMouse(active){
            let _case = this.$refs.case;
            let text = [this.$refs.heading, this.$refs.text, this.$refs.button_case];
            if (active){
                _case.style.background = '#005FA3';
                for (var i=0; i<text.length; i++){
                    text[i].style.color = '#fff';
                }
            } else {
                _case.style.background = '#EBEBEB';
                for (var i=0; i<text.length; i++){
                    text[i].style.color = '#000';
                    if (text[i] == this.$refs.button_case){
                        text[i].style.color = '#005FA3';
                    }
                }
            }
        },
        AlertTest(){
            alert('Это тестовая версия сайта');
        }
    },
}
</script>

<template lang="pug">
.case(@mouseenter='ActiveMouse(true)', @mouseleave='ActiveMouse(false)', ref='case')
    h1.heading(ref='heading') {{this.heading}}
    p.text(ref='text') {{this.text}}
    .button_case(ref='button_case' @mousedown='AlertTest()') Все кейсы
</template>

<style lang="scss">
.case{
    background: #EBEBEB;
    width: 175px;
    height: 195px;
    margin-right: 30px;
    padding-left: 40px;
    padding-top: 30px;
    padding-bottom: 30px;
    padding-right: 40px;
    display: flex;
    flex-direction: column;

    .heading{
        font-family: 'Lato';
        font-style: normal;
        font-weight: bold;
        font-size: 55px;
        letter-spacing: 0.1em;
        text-transform: uppercase;
    }
    .text{
        font-family: 'Lato';
        font-style: normal;
        font-weight: 700;
        font-size: 14px;
        line-height: 18px;
    }
    .button_case{
        font-family: 'Lato';
        font-style: normal;
        font-weight: 700;
        font-size: 14px;
        color: #005FA3;
        text-decoration-line: underline;
        display: flex;
        margin-top: auto;
        margin-bottom: 0em;
        cursor: pointer;
    }
}

@media (max-width: 800px){
    .case{
        margin: 0 auto;
        margin-right: 0px;
        margin-bottom: 20px;
    }
}
</style>