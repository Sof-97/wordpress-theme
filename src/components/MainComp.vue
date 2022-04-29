<template>
    <div>
        <JumboComp/>
    </div>
</template>
<script>
import JumboComp from "./sub-components/JumboComp.vue"

export default {
    name: 'MainComp',
    components:{
        JumboComp,
    }
}
</script>