<template>
    <input v-model="input" @keyup.enter="emitInput" type="text"/>
</template>
<script>
export default {
    name:"searchbar",
    data(){
        return{
            input:"",
        }
    },
    methods: {
        emitInput: (input) =>{
            this.input = input
            console.log(this.input);
            this.$emit("emitinput", this.input)
        }
    }
}
</script>
