<script>
export default {
    methods: {
        TestAlert(){
            alert('Это тестовая версия сайта');
        }
    }
}
</script>

<template lang="pug">
.contacts
    .sides
        .left
            h1.name-page Связь с нами
            p.text У вас остались вопросы? Напишите нам - мы ответим в ближайшее время!
            .more-contacts
                .contact
                    img(src='../assets/images/icons/phone-white.svg')
                    p.contact-info +7 (111) 222-33-44
                .contact
                    img(src='../assets/images/icons/email-white.svg')
                    p.contact-info order@bu-one.ru
        .right
            .form
                .inputs
                    .input
                        label Имя
                        input(type='text', id='input_name', placeholder='Иван')
                    .input
                        label Фамилия
                        input(type='text', id='input_surname', placeholder='Иванов')
                .textarea
                    label Сообщение
                    textarea(type='text' id='textarea' placeholder='Ваше сообщение')
                .button
                    button(@mousedown='TestAlert()') Отправить сообщение

</template>

<style lang="scss">
.contacts{
    padding-left: 10%;
    padding-right: 10%;
    padding-top: 122px;
    background: url('../assets/images/background-last-screen.png');
    background-size: cover;
    padding-bottom: 140px;
    .sides{
        display: flex;
        .left{
            width: 100%;
            .name-page{
                color: #fff;
                font-family: 'Merriweather';
                font-style: normal;
                font-weight: 900;
                font-size: 48px;
                margin-bottom: 60px;
            }
            .text{
                color: #fff;
                font-family: 'Lato';
                font-style: normal;
                font-weight: 300;
                font-size: 18px;
                margin-bottom: 80px;
            }
            .more-contacts{
                display: flex;
                .contact{
                    display: flex;
                    margin-right: 40px;
                    color: #fff;
                    .contact-info{
                        padding-left: 15px;
                        font-family: 'Lato';
                        font-style: normal;
                        font-weight: 300;
                        font-size: 21px;
                    }
                }
            }
        }
        .right{
            width: 40%;
            margin-left: auto;
            margin-right: 0em;
            display: flex;
            flex-direction: column;
            .form{
                display: flex;
                flex-direction: column;
                height: 100%;
                label{
                    font-family: 'Lato';
                    font-style: normal;
                    font-weight: 400;
                    font-size: 16px;
                    color: #fff;
                }
                .inputs{
                    display: flex;
                    margin-bottom: 35px;
                    .input{
                        margin-right:30px;
                        input{
                            color: #fff;
                            background: none;
                            border: none;
                            border-bottom: 2px solid #fff;
                            font-family: 'Lato';
                            font-style: normal;
                            font-weight: 100;
                            font-size: 21px;
                            padding: 15px 0 15px 0;
                            &:focus{
                                outline: none;
                            }
                        }
                    }
                }
                .textarea{
                    display: flex;
                    flex-direction: column;
                    height: 100%;
                    textarea{
                        margin-top:15px;
                        font-family: 'Lato';
                        font-style: normal;
                        font-weight: 100;
                        font-size: 21px;
                        color: #fff;
                        background: none;
                        border:none;
                        border-bottom: 2px solid #fff;
                        resize: none;
                        height: 130px;
                        &:focus{
                            outline: none;
                        }
                    }
                    margin-bottom: 50px;
                }
                .button{
                    margin-top: auto;
                    margin-bottom: 0em;
                    margin-left: auto;
                    margin-right: 0em;
                    button{
                        padding: 18px 30px 18px 30px;
                        color: #fff;
                        border: none;
                        background: #005FA3;
                        font-family: 'Lato';
                        font-style: normal;
                        font-weight: 400;
                        font-size: 18px;
                        &:hover{
                            background: #00487c;
                            transition: 0.2s;
                        }
                    }
                }
            }
        }
    }
}

@media (max-width: 800px){
    .contacts{
        //padding-left: 10%;
        //@at-rootpadding-right: 10%;
        padding-top: 50px;
        //background: url('../assets/images/background-last-screen.png');
        //background-size: cover;
        padding-bottom: 50px;
        .sides{
            //display: flex;
            flex-direction: column;
            .left{
                width: 100%;
                margin-bottom: 50px;
                .name-page{
                    font-size: 30px;
                    margin-bottom: 25px;
                }
                .text{
                    font-size: 14px;
                    margin-bottom: 50px;
                }
                .more-contacts{
                    display: flex;
                    flex-direction: column;
                    .contact{
                        margin-right: 0;
                        margin-bottom: 20px;
                        img{
                            width: 30px;
                            height: 30px;
                        }
                        .contact-info{
                            padding-left: 15px;
                            margin: auto 0;
                            font-size: 14px;
                        }
                    }
                }
            }
            .right{
                width: 100%;
                margin-left: 0;
                margin-right: 0;
                .form{
                    height: 100%;
                    label{
                        display: flex;
                        flex-direction: column;
                        font-size: 15px;
                    }
                    .inputs{
                        display: flex;
                        flex-direction: column;
                        margin-bottom: 0;
                        .input{
                            margin-right:0;
                            margin-bottom: 40px;
                            input{
                                width: 100%;
                                font-size: 18px;
                                padding: 5px 0 15px 0;
                            }
                        }
                    }
                    .textarea{
                        textarea{
                            margin-top: 5px;
                            font-size: 18px;
                            height: 130px;
                            width: 100%;
                        }
                        margin-bottom: 50px;
                    }
                    .button{
                        button{
                            font-size: 16px;
                        }
                    }
                }
            }
        }
    }
}
</style>