<template>
    <div>
        <JumboComp/>
        <AboutCompany/>
    </div>
</template>
<script>
import JumboComp from "./sub-components/JumboComp.vue"
import AboutCompany from "./sub-components/AboutCompany.vue"
export default {
    name: 'MainComp',
    components:{
        JumboComp,
        AboutCompany,
    }
}
</script>