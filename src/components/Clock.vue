<template>
    <div >
        {{ value.hours }} : {{ value.minutes }}
    </div>
</template>

<script>

export default {
    name: 'clock',
    props: {
        value:{
            type: Object
        }
    },

    created() {
        setInterval(() => {
            var dT = new Date();
            this.$emit('input', {hours: dT.getHours().toString(), minutes:dT.getMinutes().toString()});
            this.$emit('setSecondCurrentTime', {hours: dT.getHours().toString(), minutes: dT.getMinutes().toString()} );
        }, 1000);
    }
}

</script>


<style scoped>

</style>