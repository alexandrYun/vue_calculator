<template>
    <div>
        <div><input type="text" v-model="x" /></div>
        <div><input type="text" v-model="y" /></div>
        <div><span v-text="result"></span></div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            x: 0,
            y: 0,
            lastResult: 10,
        }  
    },
    computed: {
        result: function() {
            let x = +this.x;
            // if(Number.isNaN(x)) return this.lastResult;
            let y = +this.y;
            // if(Number.isNaN(y)) return this.lastResult;
            // this.lastResult = x + y;
            let res = x + y;
            return `Результат сложения ${res}`
        }
    }
}
</script>
