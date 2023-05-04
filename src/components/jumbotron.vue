<script>
export default{
    name: "jumbotron",
}
</script>

<template>
    <div id="jumbotron">
    </div>
</template>

<style lang="scss">
@use '../style/main.scss' as *;
#jumbotron{
    background-image: url(../assets/img/jumbotron.jpg);
    background-position: center top;
    background-size: cover;
    background-repeat: no-repeat;
    min-height: 300px;
}
</style>