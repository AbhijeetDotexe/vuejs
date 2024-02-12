<template>
    <div class="container">

        <h1>{{ test }}</h1>
        <input class="inp" v-model="text" placeholder="Enter your text">
        <p>Message is: {{ text }}</p>
        <button @click="getData">Click Me</button>
        <br/>
        <div class="counter">

            <button @click="increaseValue">Add</button>
            <p class="count">{{ count }}</p>
            <button @click="decreaseValue">Subtract</button>
        </div>
        <!-- {{ inputText }} -->
        <p v-html="inputText"></p>
    </div>
</template>

<script>
    export default{
        name: 'ChildComponent',
        data(){
            return{
                count: 0,
                test: "This is just for testing !",
                text:"",
                inputText:"<h1>I hope this is working !</h1>"
            }
        },
        methods:{
            getData: function(){
                alert(this.text);
            },
            increaseValue: function(){
                this.count = this.count+=1;
            },
            decreaseValue: function(){
                this.count = this.count-=1;
            }
        }
    }

</script>
<style scoped>
.inp{

    height: 40px;
    border: 4px solid slategray;
    border-radius: 4px;

}
.counter{
    display: inline-flex;
    margin-top: 5px;
    border: 4px solid white;
}
.count{
    margin: 12px;
}
</style>