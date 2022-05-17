<template>
    <button>{{buttonText}}</button>
</template>

<script>
export default{
    name: 'Button',
    props: {
        buttonText: String,
    }
}
</script>

<style scoped>
    button{
        margin-left: 2em;
        padding: 10px 20px;
        background: black;
        border: none;
        border-radius: 5px;
        color: white;
        cursor: pointer;
        transition: all .5s ease-in-out 1ms;
    }
    button:hover,
    button:focus{
        transform: scale(1.1);
    }
</style>