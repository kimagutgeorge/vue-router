<template>
    <div v-for="job in jobs" :key="job.id" class="job">  
        <RouterLink :to="{ name:'JobDetails', params: {id:job.id} }">
            <h2>{{ job.title }}</h2>
        </RouterLink>
    </div>
</template>

<script>
export default {
    data() {
        return {
            jobs: [
                { title: 'Ninja UX Designer', id: 1, details: 'lorem'},
                { title: 'Ninja Web Dev', id: 2, details: 'lorem'},
                { title: 'Ninja Vue Dev', id: 3, details: 'lorem'}
            ]
        }
    }
}
</script>

<style>
    .job h2{
        background-color: #f4f4f4;
        padding:20px;
        border-radius: 10px;
        margin:10px auto;
        max-width: 600px;
        cursor:pointer;
        color:#444;
    }
    .job h2:hover{
        background-color: #ddd;
    }
    .job a{
        text-decoration: none;
    }
</style>