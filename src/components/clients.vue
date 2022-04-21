<script>
import OptionBar from './otherComponents/scroll-buttons-bar.vue';

export default {
    components: {
        OptionBar
    }
}
</script>

<template lang="pug">
.clients
    p.name-page Наши клиенты
    h1.heading С нами работают
    .images
        img(src='../assets/images/microsoft.png')
        img(src='../assets/images/microsoft.png')
        img(src='../assets/images/microsoft.png')
        img(src='../assets/images/microsoft.png')
    OptionBar(color_point = "#005FA3", color_button = '#005FA3', id_bar='2')
</template>

<style lang="scss">
.clients{
    background: #EBEBEB;
    padding-left: 10%;
    padding-right: 10%;
    padding-top: 100px;
    .name-page{
        font-family: 'Lato';
        font-style: normal;
        font-weight: 900;
        font-size: 24px;
        color: #BDBDBD;
        padding-bottom: 40px;
    }
    .heading{
        font-family: 'Merriweather';
        font-style: normal;
        font-weight: 900;
        font-size: 48px;
        color: #333;
        padding-bottom: 80px;
    }
    .images{
        display: flex;
        img{
            margin: 0 auto;
            &:first-child{
                margin-left: 0;
            }
            &:last-child{
                margin-right: 0;
            }
        }
        padding-bottom: 50px;
    }
}

@media (max-width: 800px){
    .clients{
        padding-top: 50px;
        .name-page{
            font-size: 20px;
            padding-bottom: 0;
        }
        .heading{
            font-size: 22px;
            padding-bottom: 25px;
        }
        .images{
            display: flex;
            flex-direction: column;
            img{
                width: 60%;
                &:first-child{
                    margin: 0 auto;
                }
                &:last-child{
                    margin: 0 auto;
                }
            }
            padding-bottom: 50px;
        }
    }
}
</style>