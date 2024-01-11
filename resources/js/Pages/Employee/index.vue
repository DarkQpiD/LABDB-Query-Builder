<template>
    <div>
        <h1 class="font-bold">Employee</h1>
        <p class="border-solid border-4 border-teal-600 bg-teal-400 p-8 inline-block">Department</p>
        <div class="flex flex-wrap">
            <div v-for="(department, index) in dept" :key="index" class="border-orange-400 border-4 p-8 mb-4">
                <h2 class="mb-2">{{ department.dept_name }}</h2>
            </div>
        </div>
    </div>
    <h2 class="border-solid border-4 border-teal-600 bg-teal-400 p-8 inline-block">Male A</h2>
    <div class="flex flex-wrap">
            <div v-for="(male_emp, index) in male" :key="index" class="border-orange-400 border-4 p-8 mb-4">
                <h2 class="mb-2">Name : {{ male_emp.first_name }}</h2>
                <h2 class="mb-2">Gender : {{ male_emp.gender }}</h2>
            </div>
    </div>
    <h2 class="border-solid border-4 border-teal-600 bg-teal-400 p-8 inline-block">Female 50 yo</h2>
    <div class="flex flex-wrap">
            <div v-for="(female_emp, index) in female" :key="index" class="border-orange-400 border-4 p-8 mb-4">
                <h2 class="mb-2">Name : {{ female_emp.first_name }}</h2>
                <h2 class="mb-2">Gender : {{ female_emp.gender }}</h2>
                <h2 class="mb-2">Birthdate : {{ female_emp.birth_date }}</h2>
            </div>
    </div>
</template>
 
<script setup>
defineProps(["dept", "male", "female"]);

</script>


<style scoped>
h1{
    text-align: center;
    text-decoration: underline;
    font-size: x-large;
}
</style>