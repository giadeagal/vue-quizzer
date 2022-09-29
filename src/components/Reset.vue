<template>
    <button 
        type="button" 
        class="reset-btn"
        @click.prevent="resetQuiz"
        v-if="quizDone"
        >
        Reset
        </button>
</template>

<script>
export default {
    name: 'Reset',
    props: ['quizDone'],
    emits: ['quiz-reset'],
    methods: {
        resetQuiz() {
            this.$emit('quiz-reset');
        }
    }
}
</script>

<style>
button {
    cursor: pointer;
}
</style>