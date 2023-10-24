<template>
    <!-- <slot name="name" @click="myAlert">{{name}}</slot>
    <slot name="family">{{family}}</slot>
    <slot name="phone">{{phone}}</slot> -->
    <slot name="name"></slot>
    <slot name="family"></slot>
    <slot name="phone"></slot>
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