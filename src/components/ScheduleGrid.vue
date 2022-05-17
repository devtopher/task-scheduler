<template>
    <div class="container">
        <HourBlock id="8" :task="taskMapFromParent.eight" hour="8AM" />
        <HourBlock id="9" :task="taskMapFromParent.nine" hour="9AM" />
        <HourBlock id="10" :task="taskMapFromParent.ten" hour="10AM" />
        <HourBlock id="11" :task="taskMapFromParent.eleven" hour="11AM" />
        <HourBlock id="12" :task="taskMapFromParent.twelve" hour="12PM" />
        <HourBlock id="13" :task="taskMapFromParent.thirteen" hour="1PM" />
        <HourBlock id="14" :task="taskMapFromParent.fourteen" hour="2PM" />
        <HourBlock id="15" :task="taskMapFromParent.fifteen" hour="3PM" />
        <HourBlock id="16" :task="taskMapFromParent.sixteen" hour="4PM" />
        <HourBlock id="17" :task="taskMapFromParent.seventeen" hour="5PM" />
        <HourBlock id="18" style="border-bottom: 2px solid black;" hour="6PM" />
    </div>
</template>
<script>
import HourBlock from './HourBlock.vue'
export default {
    name: 'ScheduleGrid',
    components: {
        HourBlock,
    },
    props: {
        selectedHourFromParent: Number,
        selectedMessageFromParent: String,
        taskMapFromParent: Object,
    },
    methods: {
        readTaskMap: function () {
            console.log(this.taskMapFromParent)

        }
    }
}    
</script>
<style>
.container {
    display: flex;
    flex-direction: column;
    width: 60%;
}
</style>