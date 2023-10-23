<template>
    <h1 @click="myAlert">{{name}}</h1>
    <h1>{{family}}</h1>
    <h1>{{phone}}</h1>
</template>

<script>
export default {
    name: "Hello",
    props: { name: String, family: String, phone: Number },
    methods: {
        myAlert()
        {
            alert("Click Happened");
            this.$emit("nameClicked",this.name) 

            
        },
        myAlert2(text)
        {
            alert(text);
        }
    },
};
</script>