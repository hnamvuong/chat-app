<template>
    <div class="conversation">
        <h1>{{ contact ? contact.name : 'Select a Contact' }}</h1>
        <MessagesFeed :contact="contact" :messages="messages"></MessagesFeed>
        <MessageComposer @send="sendMessage"></MessageComposer>
    </div>
</template>

<script>
    import MessagesFeed from "./MessagesFeed";
    import MessageComposer from "./MessageComposer";
    export default {
        props: {
            contact: {
                type: Object,
                default: null
            },
            messages: {
                type: Array,
                default: []
            }
        },
        methods: {
            sendMessage(text) {
                console.log(text);
            }
        },
        components: {MessageComposer, MessagesFeed},
    }
</script>

<style scoped>

</style>
