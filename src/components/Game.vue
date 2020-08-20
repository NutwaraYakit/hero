<template>
  <div>
    <p>HP Player {{randomDamage(1,3)}}
        {{player[randomDamage(1,3) - 1].name}}
    </p> 
    + รูป
    <hr>
    name = {{ aPlayer.name }}
    hp = {{ aPlayer.image }}
    <hr/>
    <p>HP Monster 150</p> 
    +รูป
    <button @click="start()">Start</button>
    <button @click="attack()">Attack</button>
  </div>
</template>

<script>
export default{
    data : function(){
        return{
            player: [
                {name: 'Anakin' , hp:90},
                {name: 'Iron man' , hp: 150},
                {name: 'Doraemon' , hp: 200},
            ],
            monster:[
                {name: 'Thanos' , hp:300},
                {name: 'Darth vader' , hp:20},
                {name: 'Comti' , hp: 20},
            ],
        }
    },
    methods:{
        randomDamage: function(min, max) {             
            return Math.max(Math.floor(Math.random() * max) + 1, min);    
        },
        start: function() {
            //1. random Player 1-5 --> ชื่อ hp รูป
            this.aPlayer=this.aPlayer[this.randomDamage(0,4)]
            //2. random Monster 1-5
        },

    
        }
    }


</script>

<style>

</style>