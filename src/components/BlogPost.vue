<template>
    <div>
        <h1>{{ title }}</h1>
        <p><slot/></p>
        <div class="flex justify-center">
            <button-counter :icon="icon"></button-counter>
            <button
                class="rounded border-2 m-2 p-2 text-green border-green"
                @click="$emit('enlarge-text', postFontSize+=0.1)">
            Enlarge Text
            </button>
        </div>
    </div>
</template>

<script>
import ButtonCounter from '@/components/ButtonCounter';

export default {
    props: {
        title: '',
        content: '',
        icon: ''
    },

    data () {
        return {
            postFontSize: 1
        }
    }, 
    
    components: {
        ButtonCounter
    }
}
</script>
