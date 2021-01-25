<template>
    <div class="container">
        <ServerButton isHome />
        <div class="separator"></div>
         <ServerButton :mentions="3" />
         <ServerButton hasNotification />
         <ServerButton :mentions="33" hasNotification />
         <ServerButton v-for="servers in 18" :key="servers.id"/>
    </div>
</template>

<script>
    import ServerButton from './ServerButton'

    export default{
        components:{
            ServerButton
        }
    }
</script>

<style scoped lang="scss">
    .container{
        display: flex;
        flex-direction: column;
        align-items: center;
        background-color: var(--tertiary);
        padding: 11px 0;
        max-height: 100vh;
        grid-area: SL;
        overflow: scroll; /** ativa a barra de rolagem nesse container */
        &::-webkit-scrollbar{ /** config do scrollbar */
            display: none; /** desativa a visibilidade do scroollbar */
        }
    }

    .separator{
        width: 32px;
        border-bottom: solid 2px var(--quarternary);
        margin-bottom: 8px;
    }
</style>