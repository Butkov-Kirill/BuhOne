<script>
import BoardCase from './otherComponents/about-board.vue';

export default {
    components: {
        BoardCase
    }
}
</script>

<template lang="pug">
.about
    .sides
        .left
            p.namePage О нас
            h1.heading Компания
                span <br>ИвановПром
            p.text Lorem Ipsum - это текст-"рыба", часто используемый в печати и вэб-дизайне.
                | Lorem Ipsum является стандартной "рыбой" для текстов на латинице с начала XVI века.
                | В то время некий безымянный печатник создал большую коллекцию размеров и форм шрифтов,
                | используя Lorem Ipsum для распечатки образцов. Lorem Ipsum не только успешно пережил
                | без заметных изменений пять веков, но и перешагнул в электронный дизайн.
        .right
            .board-line
                BoardCase
                BoardCase
            .board-line
                BoardCase
                BoardCase
</template>

<style lang="scss">
.about{
    padding-top: 140px;
    padding-bottom: 140px;
    .sides{
        padding-left: 10%;
        padding-right: 10%;
        display: flex;
        .left{
            width: 50%;
            .namePage{
                font-family: 'Lato';
                font-style: normal;
                font-weight: 900;
                font-size: 24px;
                color: #BDBDBD;
            }
            .heading{
                font-family: 'Merriweather';
                font-style: normal;
                font-weight: 900;
                font-size: 48px;
                line-height: 69px;
                color: #333;
                span{
                    color: #005FA3;
                }
                padding-bottom: 50px;
            }
            .text{
                font-family: 'Lato';
                font-style: normal;
                font-weight: 300;
                font-size: 18px;
                line-height: 25px;
                width: 80%;
            }
        }
        .right{
            width: 50%;
            display: flex;
            flex-direction: column;
            .board-line{
                margin: 0 auto;
                display: flex;
                &:first-child{
                    margin-bottom: 30px;
                }
            }
        }
    }
}

@media (max-width: 800px){
    .about{
        padding-top: 50px;
        padding-bottom: 50px;
        .sides{
            flex-direction: column;
            .left{
                width: 100%;
                .namePage{
                    font-size: 20px;
                }
                .heading{
                    font-size: 40px;
                    line-height: 55px;
                    padding-bottom: 15px;
                }
            }
            .right{
                width: 100%;
                .board-line{
                    flex-direction: column;
                    &:first-child{
                        margin-top: 25px;
                        margin-bottom: 0;
                    }
                }
            }
        }
    }
}
</style>