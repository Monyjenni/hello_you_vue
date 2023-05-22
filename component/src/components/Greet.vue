<template>
<div>
<h2>Hello {{ name }} a.k.a {{ heroName }} ~~</h2>
</div>

</template>

<script>
//do import skeleton just write vbase-css
//register this to local
export default {
    //name of comp
    //name is dynamic controll by this name props
    name: 'GreetMony',
    props: ['name','heroName'],
    computed :{
        fullname () {
            return `${this.firstName} ${this.lastName}`
        }
    }


}
</script>