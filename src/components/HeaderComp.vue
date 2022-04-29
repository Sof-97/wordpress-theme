<template>
    <div>
        <!-- Header Top  - orario apertura e contatti -->
        <div class="header_top">
            <div>
                <i class="fa-solid fa-clock"></i>
                <span>Open Hours: Mon - Sat - 9:00 - 18:00</span>
            </div>
            <div class="contacts">
                <p><i class="fa-solid fa-phone"></i>{{contacts.phone}}</p>
                <p><i class="fa-solid fa-envelope"></i>{{contacts.email}}</p>
                <i class="fa-brands fa-facebook-f"></i>
                <i class="fa-brands fa-twitter"></i>
                <i class="fa-brands fa-linkedin"></i>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HeaderComp',
    props:{
        contancts: Object,
    }

}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';
.header{
    &_top{
        display: flex;
        justify-content: space-around;
        color: #fff;
        background-color: $smalt-blue;
        padding: 5px 0;
        i{
            margin-right: 5px;
        }
        .contacts{

        }
    }
}
</style>