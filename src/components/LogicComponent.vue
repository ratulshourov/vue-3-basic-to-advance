<template>
    <div>
        <h1 v-if="isActive">You are active user</h1>
        <h1 v-else>You are not active user</h1>
        <ul>
            <li v-for="aFramework in framework" :key="aFramework">{{ aFramework }}</li>
        </ul>
<h1>Developer List</h1>
        <ul>
            <li v-for="aFramework in developersInfo" :key="aFramework.fname">{{ aFramework.fname }}
            </li>
            
        </ul>
       
    </div>
</template>

<script>
export default {
    data() {
        return {
            isActive: false,

            framework:['laravel','codeigniter'],
            developersInfo:[
               {
                fname:'ratul',
               },
               {
                fname:'Minhaj',
               }
            ]
        };
    },
}
</script>

<style scoped>

</style>