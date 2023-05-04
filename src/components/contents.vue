<script>
export default{
    name: "contents",
    data(){
        return{

        }
    }
}
</script>

<template>
    <div id="contents">
        <span>CURRENT SERIES</span>
        <div>

        </div>
    </div>
</template>

<style lang="scss">
@use '../style/main.scss' as *;
#contents{
    span{
        color: white;
        padding: 0.5rem 1rem;
        background-color: $blue-DC;
    }
}
</style>