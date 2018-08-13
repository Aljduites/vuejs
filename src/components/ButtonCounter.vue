<template>
    <div>
        <button
            class="border-2 rounded m-2 p-2 text-blue border-blue"
            @click="increment">
            {{ icon }} {{ count > 0 ? '+' : '' }}{{ count }}
        </button>
    </div>    
</template>

<script>
export default {
    props: {
        icon: {
            type: String,
            default: '👍'
        }
    },

    data () {
        return {
            count: 0
        }
    },

    methods: {
        increment () {
            this.count++;
        }
    }
}
</script>
<style>
.components {
    line-height: 1cm;
}
</style>
