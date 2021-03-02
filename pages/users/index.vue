<template>
    <div><h2>Todo task</h2>
<Frominput/>
<Header/>
</div>
</template>
   
<script>
import Header from "@/components/Header"
import Frominput from "@/components/Frominput"
export default {
    layout:"coreLayout"   ,
    components:{
        Header,
        Frominput
        
    }
}
</script>