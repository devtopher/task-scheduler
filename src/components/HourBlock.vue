<template>
    <div class="block">
        <div class="hour">{{ hour }}</div>
        <div class="slot">{{ task }}</div>
    </div>
</template>

<script>
export default {
    name: 'HourBlock',
    props: {
        hour: String,
        task: String,
    }
}
</script>

<style>
.block {
    width: 100%;
    border-left: 2px solid black;
    border-right: 2px solid black;
    border-top: 2px solid black;
    display: flex;
    justify-content: space-between;
}
.slot{
    margin-right: 1em;
}
</style>