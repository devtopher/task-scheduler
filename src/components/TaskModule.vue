<template>
    <div>
        <label for="hour-select">Choose an hour:</label><select name="hours" id="hour-select">
            <option value="8">8AM</option>
            <option value="9">9AM</option>
            <option value="10">10AM</option>
            <option value="11">11AM</option>
            <option value="12">12PM</option>
            <option value="13">1PM</option>
            <option value="14">2PM</option>
            <option value="15">3PM</option>
            <option value="16">4PM</option>
            <option value="17">5PM</option>
            <option value="18">6PM</option>
            </select>
        <textarea></textarea>
        <Button buttonText="Submit New Task"  />
    </div>
</template>

<script>
import Button from './Button.vue'
    export default{
        name: 'TaskModule',
        components: {
            Button,
        }


    }
</script>

<style scoped>
div{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    z-index: 10;
    background: rgba(70, 130, 180, .85);
    width: 80%;
    height: 200px;
    position: absolute;

}
</style>