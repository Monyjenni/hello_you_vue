<template>
    <div>
        Hello {{ firstName }} {{ lastName }}
    </div>
</template>

<script>
    export default {
        name :"PersonGreeting",
        components : ['firstName','lastName']
        
    }
</script>

<style lang="sass" scoped>

</style>