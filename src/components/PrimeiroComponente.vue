<template>
    <h1>Olá {{frame}}!</h1>
</template>

<script>
export default{
    name: 'PrimeiroComponente',
    data() {
        return{
            frame: 'Angular'
        }
    }
}
</script>
