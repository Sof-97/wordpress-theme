<template>
    <div>
        <JumboComp/>
        <AboutCompany/>
        <ServicesComp/>
    </div>
</template>
<script>
import JumboComp from "./sub-components/JumboComp.vue"
import AboutCompany from "./sub-components/AboutCompany.vue"
import ServicesComp from "./sub-components/ServicesComp.vue"
export default {
    name: 'MainComp',
    components:{
        JumboComp,
        AboutCompany,
        ServicesComp,
    }
}
</script>