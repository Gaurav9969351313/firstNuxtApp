<template>
    <h1>This is a _Id component {{ $route.params.id }}</h1>
</template>

<script>
export default {
    validate(data){
        console.log(data);
        //return true;
        return /^\d+$/.test(data.params.id); //dynamic segment validation of url parameters
    },
    layout:'users'
}
</script>

