<template>
    <div>
        <label for="hour-select">Choose an hour:</label><select name="hours" id="hour-select">
            <option value="8">8AM</option>
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