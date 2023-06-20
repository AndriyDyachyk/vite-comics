
<script>
export default {
    data(){
        return{
            navBarMenu:[
                {
                    
                }
            ]
        }
    }
}
</script>
<template lang="">
    <header>
        <div class="container">
            <div class="logo"><img src="/dc-logo.png" alt=""></div>
            <nav>
                <ul>
                    <li><a href="" v-for="(menu, index) in navBarMenu">{{}}</a></li>
                </ul>
            </nav>
        </div>
    </header>
</template>
<style lang="">
    
</style>