<script>
import DEFAULT_IMAGE from '../../assets/images/girl.png';

export default {
    props: {
        text : {
            Type : String,
            default : 'Lorem Ipsum - это текст-"рыба", часто используемый в печати и вэб-дизайне. Lorem Ipsum является стандартной "рыбой" для текстов на латинице с начала XVI века. В то время некий безымянный печатник создал большую коллекцию размеров и форм шрифтов, используя Lorem Ipsum для распечатки образцов. Lorem Ipsum - это текст-"рыба", часто используемый в печати и вэб-дизайне.'
        },
        name_human : {
            Type : String,
            default : 'Екатерина Иванова'
        },
        post : {
            Type : String,
            default : 'Директор ООО “Раз-два”'
        },
        image_human : {
            Type : Image,
            default : DEFAULT_IMAGE
        }
    },
    mounted(){
        this.$nextTick(function(){
            this.$refs.image_human.src = this.image_human;
        });
    }
}
</script>

<template lang="pug">
.recall
    p.text {{this.text}}
    .info-human
        img(src='../../assets/images/girl.png', ref='image_human')
        .info
            .name {{this.name_human}}
            .post {{this.post}}
</template>

<style lang="scss">
.recall{
    margin-bottom: 40px;
    background: #EBEBEB;
    padding: 45px 95px 45px 95px;
    .text{
        font-family: 'Lato';
        font-style: normal;
        font-weight: 300;
        font-size: 18px;
        line-height: 25px;
        margin-bottom: 58px;
    }
    .info-human{
        display: flex;
        img{
            border-radius: 50%;
            margin-right: 45px;
        }
        .info{
            .name{
                font-family: 'Lato';
                font-style: normal;
                font-weight: 900;
                font-size: 18px;
                line-height: 25px;
                padding-bottom: 10px;
            }
            .post{
                font-family: 'Lato';
                font-style: normal;
                font-weight: 400;
                font-size: 14px;
                line-height: 19px;
            }
        }
    }
}

@media (max-width: 800px){
    .recall{
        margin-bottom: 50px;
        padding: 20px 20px 20px 20px;
        .text{
            font-size: 14px;
            margin-bottom: 40px;
        }
        .info-human{
            img{
                margin-right: 10px;
                width: 25%;
            }
            .info{
                .name{
                    padding-bottom: 5px;
                }
            }
        }
    }
}
</style>