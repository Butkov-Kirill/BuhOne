<script>
const ACTIVE_POINT = '1', DEACTIVE_POINT='0.4';

export default {
    props: {
        color_point : {
            Type: String,
            default: '#fff'
        },
        color_button: {
            Type: String,
            default: '#fff'
        },
        id_bar : {
            Type: String,
            default: '1',
        }
    },
    data(){
        return{
            ID : 1,
            points : null
        }
    },
    mounted(){
        this.$nextTick(function(){
            let buttons = [];
            for (var i=1; i<3; i++){
                buttons[i] = document.getElementById('button-arrow'+i);
                buttons[i].id = this.id_bar+'bar_button-arrow'+i;
                buttons[i].style.background = this.color_button;
            }
            let points = [];
            for (var i=1; i<5; i++){
                points[i] = document.getElementById('point_'+i);
                points[i].id = this.id_bar+'bar_point_'+i;
                points[i].style.background = this.color_point;
            }
            this.points = points;
            this.SetPoint(parseInt(this.ID));
        }); 
    },
    methods: {
        ClickButton(side){
            let id = parseInt(this.ID);
            if (side == 'left'){
                if (id>1){
                    id--;
                } else {
                    id=4;
                }
            } else if (side == 'right'){
                if (id<4){
                    id++;
                } else {
                    id=1;
                }
            }
            this.ID = id;
            this.SetPoint(id);
        },
        SetPoint(id){
            for (var i = 1; i < 5; i++){
                document.getElementById(this.points[i].id).style.opacity = DEACTIVE_POINT;
            }
            document.getElementById(this.points[id].id).style.opacity = ACTIVE_POINT;
            this.$emit(this.id_bar+'chuse_point', id);
        }
    }
}
</script>

<template lang="pug">
.option-bar
    .points
        .point(id='point_1')
        .point(id='point_2')
        .point(id='point_3')
        .point(id='point_4')
    .buttons
        .button(@mousedown = 'ClickButton("left")')
            div.button-arrow(id='button-arrow1' style='opacity: 0.2')
            i(class='fas fa-chevron-left')
        .button(@mousedown = 'ClickButton("right")')
            div.button-arrow(id='button-arrow2' style='opacity: 0.4')
            i(class='fas fa-chevron-right')
</template>

<style lang="scss">
.option-bar{
    display: flex;
    margin-bottom: 100px;
    .points{
        display: flex;
        margin-top: auto;
        margin-bottom: 0em;

        .point{
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background: #000;
            margin-right: 40px;
        }
    }
    .buttons{
        margin-left: auto;
        margin-right: 0em;
        display: flex;

        .button{
            position: relative;
            width: 60px;
            height:60px;
            .button-arrow{
                width: 60px;
                height: 60px;
                border: none;
                position:absolute;
            }
            i{
                font-size: 30px;
                color: #fff;
                z-index:2;
                position:absolute;
                left: 50%;
                top: 50%;
                transform: translate(-50%, -50%);
            }

            &:hover{
                box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.582);
                z-index:1;
                transition: 0.3s;
            }
        }
    }
}

@media (max-width: 800px){
    .option-bar{
        margin-bottom: 70px;
        .points{
            .point{
                width: 6px;
                height: 6px;
                margin-right: 25px;
            }
        }
        .buttons{
            .button{
                width: 40px;
                height:40px;
                .button-arrow{
                    width: 40px;
                    height: 40px;
                }
                i{
                    font-size: 20px;
                }
            }
        }
    }
}
</style>