<template lang="pug">
.copyright
    p.text 2019 (с) Все права защищены. БухОне.ру
    p.text Разработано: BuhOne
</template>

<style lang="scss">
.copyright{
    padding: 30px 10% 30px 10%;
    display: flex;
    .text{
        font-family: 'Lato';
        font-style: normal;
        font-weight: 300;
        font-size: 14px;
        &:last-child{
            margin-left: auto;
            margin-right: 0em;
        }
    }
}

@media (max-width: 800px){
    .copyright{
        padding: 10px 10% 10px 10%;
        .text{
            font-size: 10px;
        }
    }
}
</style>