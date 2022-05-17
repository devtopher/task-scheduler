<template>
    <div class="module">
        <label for="hour-select">Select Task Start Time:</label>
        <select v-model="selected" name="hours" id="hour-select">
            <option disabled value="">Please select one</option>
            <option value="eight">8AM</option>
            <option value="nine">9AM</option>
            <option value="ten">10AM</option>
            <option value="eleven">11AM</option>
            <option value="twelve">12PM</option>
            <option value="thirteen">1PM</option>
            <option value="fourteen">2PM</option>
            <option value="fifteen">3PM</option>
            <option value="sixteen">4PM</option>
            <option value="seventeen">5PM</option>
            <option value="eighteen">6PM</option>
        </select>
        <textarea v-model="message" placeholder="Task Name Here"></textarea>
        <MyButton @click="handleSubmit" buttonText="Submit New Task" />
    </div>
</template>

<script>
import MyButton from './MyButton.vue'
export default {
    name: 'TaskModule',
    components: {
        MyButton,
    },
    data() {
        return {
            selected: '',
            message: ''
        }
    },
    methods: {
        handleSubmit: function () {
            let form = {
                selectedHour: this.selected,
                selectedMessage: this.message
            }
            console.log(this.selected, this.message)
            this.$emit('module-close-event', form)
        }
    }





}
</script>

<style scoped>
.module {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    z-index: 10;
    background: rgba(70, 130, 180, 1);
    width: 100%;
    height: 100vh;
    position: absolute;
    color: black;

}

label,
select,
textarea,
button {
    font-size: 2rem;
    margin-bottom: 1em;
}

button {
    margin: 0;
}
</style>