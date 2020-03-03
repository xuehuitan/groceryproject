<template>
    <div>
        <button v-on:click= "add()"><p> Add to <b>Cart</b> + </p></button>
        <button v-on:click= "minus()"><p> Remove from <b>Cart</b> - </p></button>
        <br>
        <br>
        <pr><b>Cart: </b>{{counter}}</pr>
    </div>
</template>

<script>
export default {
    data(){
        return{
            counter: 0
        }
    },
    methods: {
        add: function(){
            if (this.counter < 10) {
                this.counter++;
            } else {
                alert("You cannot add more than 10 items!");
            }
        },
        minus: function(){
            if (this.counter > 0) {
                this.counter--;
            }
        }
    }
}
</script>

<style scoped>
button {
    font-family: 'Avenir', Helvetica, Arial, 
    sans-serif;
    text-align: center;
    width: 200px;
}
p{
    font-size: 12px;
    color: rgb(122, 63, 100);
}
pr{
    font-size:15px;
    color:ivory;
    background:rgb(122, 63, 100);
    padding: 10px;
}
</style>