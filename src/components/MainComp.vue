<template>
    <div>
        <JumboComp/>
        <AboutCompany/>
        <ServicesComp/>
        <ManagementComp/>
        <TeamComp :teamMembers="teamMembers"/>
        <EditorialComp :newsData="newsData"/>
        <NewsletterComp/>
        
    </div>
</template>
<script>
import JumboComp from "./sub-components/JumboComp.vue"
import AboutCompany from "./sub-components/AboutCompany.vue"
import ServicesComp from "./sub-components/ServicesComp.vue"
import ManagementComp from "./sub-components/ManagementComp.vue"
import TeamComp from "./sub-components/TeamComp.vue"
import EditorialComp from "./sub-components/EditorialComp.vue"
import NewsletterComp from "./sub-components/NewsletterComp.vue"

export default {
    name: 'MainComp',
    components:{
        JumboComp,
        AboutCompany,
        ServicesComp,
        ManagementComp,
        TeamComp,
        EditorialComp,
        NewsletterComp,
    },
    props:{
        teamMembers: Array,
        newsData: Array,
    }
}
</script>