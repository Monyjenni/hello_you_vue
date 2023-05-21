<template>
<h2>Hello {{ name }}</h2>
</template>

<script>
//do import skeleton just write vbase-css
//register this to local
export default {
    //name of comp
    //name is dynamic controll by this name props
    name: 'GreetMony',
    props: ['name']


}
</script>