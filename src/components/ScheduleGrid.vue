<template>
    <div class="container">
        <HourBlock hour="8AM" />
        <HourBlock hour="9AM" />
        <HourBlock hour="10AM" />
        <HourBlock hour="11AM" />
        <HourBlock hour="12PM" />
        <HourBlock hour="1PM" />
        <HourBlock hour="2PM" task="naptime" />
        <HourBlock hour="3PM" />
        <HourBlock hour="4PM" />
        <HourBlock hour="5PM" />
        <HourBlock hour="6PM" />
        <HourBlock hour="7PM" task="Go to sleep" />
        <HourBlock style="border-bottom: 2px solid black;" hour="8PM" />
    </div>
</template>
<script>
import HourBlock from './HourBlock.vue'
export default {
    name: 'ScheduleGrid',
    components: {
        HourBlock,
    }
}    
</script>
<style>
    .container{
        display: flex;
        flex-direction: column;
        width: 60%;
    }
</style>