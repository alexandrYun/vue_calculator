<template>
    <div>
        <span v-text="hourtime"></span>
        <span v-text="hours"></span>
        <span v-text="minutes"></span>
        <span v-text="seconds"></span>
    </div>
</template>

<script>
export default {
    data() {
        return {
            hours: 0,
            minutes: 0,
            seconds: 0,
        }  
    },
    mounted() {
        this.$options.timer = window.setTimeout(this.updateDateTime, 1000);
    },
    methods: {
            updateDateTime() {
                const now = new Date();
                this.hours = now.getHours();
                this.minutes = now.getMinutes();
                this.seconds =  now.getSeconds();
                this.$options.timer = window.setTimeout(this.updateDateTime, 1000);
        }
    },
}
</script>