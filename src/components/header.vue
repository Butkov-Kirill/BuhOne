<script>
export default {
    methods: {
        ButtonClick(className){
            this.$emit('scroll', className+'-block');
        }
    }
}
</script>

<template lang="pug">
.header
    .left
        img(src='../assets/images/logo.svg')
        h1 BuhOne
    .right
        .info
            .information
                img.icon(src='../assets/images/icons/phone.svg')
                p 8 (111) 222-33-44
            .information
                img.icon(src='../assets/images/icons/clock.svg')
                p Пн-Пт 10:00-18:00
            .information
                img.icon(src='../assets/images/icons/email.svg')
                p order@buhone.ru
            .information
                img.icon(src='../assets/images/icons/adress.svg')
                p Невский пр. 130
        .buttons
            button(@mousedown='ButtonClick("main")') Главная
            button(@mousedown='ButtonClick("services")') Услуги
            button(@mousedown='ButtonClick("about")') Кейсы
            button(@mousedown='ButtonClick("about")') О компании
            button(@mousedown='ButtonClick("contacts")') Контакты
</template>

<style lang="scss">
.header{
    padding-left: 10%;
    padding-right: 10%;
    padding-top: 30px;
    padding-bottom: 30px;
    display: flex;
    .left{
        width: 30%;
        display: flex;
        margin: auto 0;
        img{
            width: 40px;
            height: 40px;
        }
        h1{
            color: rgba(0, 95, 163, 1);
            font-family: 'Merriweather';
            font-style: normal;
            font-weight: 900;
            font-size: 36px;
            padding-left: 30px;
        }
    }
    .right{
        width: 70%;
        display: flex;
        flex-direction: column;
        .info{
            width: 100%;
            display: flex;
            justify-content: center;
            img{
                padding-right: 15px;
            }
            p{
                font-family: 'Lato';
                font-style: normal;
                font-weight: 400;
                font-size: 13px;
                line-height: 17px;
            }
            .information{
                display: flex;
                margin: 0 auto;
                &:first-child{
                    margin-left: 0;
                }
                &:last-child{
                    margin-right: 0;
                }
            }
            padding-bottom: 22px;
        }
        .buttons{
            width: 100%;
            display: flex;
            button{
                background: none;
                border: none;
                font-family: 'Lato';
                font-style: normal;
                font-weight: 700;
                font-size: 14px;
                line-height: 17px;
                letter-spacing: 0.1em;
                text-transform: uppercase;
                display: inline-block;
                margin: 0 auto;
                border-bottom: 2px solid rgba(0, 0, 0, 0);

                &:hover{
                    border-bottom: 2px solid #000;
                }

                &:first-child{
                    margin-left: 0;
                }
                &:last-child{
                    margin-right: 0;
                }
            }
        }
    }
}

@media (max-width: 800px) {
    .header{
        padding-top: 15px;
        padding-bottom: 15px;
        .left{
            width: 100%;
            h1{
                font-size: 25px;
                padding-left: 15px;
                margin: auto 0;
            }
        }
        .right{
            display: none;
        }
    }
}
</style>