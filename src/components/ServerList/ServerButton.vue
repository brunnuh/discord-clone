<template>
    <div class="serverbutton" :class="{'serverbutton-isHome' : isHome,'serverbutton-hasNotification' : hasNotification}">
        <img v-if="isHome"  src="../../assets/discord.svg" alt="logo-discord">
        <div v-if="mentions >= 1" class="mentions">
            {{mentions}}
        </div>
    </div>
</template>

<script>
    export default{
        props: {
            hasNotification: Boolean,
            mentions: Number,
            isHome: Boolean,
            selected: Boolean,
        }
    }
</script>

<style scoped lang="scss">
    .serverbutton{ /** estilo do butao */
        display: flex;
        flex-shrink: 0;
        align-items: center;
        justify-content: center;
        width: 48px;
        height: 48px;
        margin-bottom: 8px;
        background-color: var(--primary);
        cursor: pointer;
        position: relative;
        border-radius: 50%;
        transition: 0.2s;
        

        &.active,
        &:hover{
            border-radius: 16px;
            background-color: var(--discord);
        }
    }

    .serverbutton-hasNotification{ /** estilo da bolinha de notificacao */
        &::before{
            content: "";
            width: 9px;
            height: 9px;
            background-color: #fff;
            position: absolute;
            left: -17px;
            top: calc(50% - 4.5px);
            border-radius: 50%;
            display: block;
        }
    }

    .serverbutton-isHome{
        background-color: var(--rocketseat);
        &.active,
        &:hover{
            border-radius: 16px;
            background-color: var(--rocketseat);
        }
    }

    img{
        width: 24px;
        height: 24px;
        color: #fff;
    }

    .mentions{
        background-color: var(--notification);
        width: auto;
        height: 24px;
        padding: 0 4px;
        position: absolute;
        bottom: -4px;
        right: -4px;
        border: solid 4px var(--quarternary);
        border-radius: 12px;
        text-align: right;
        font-size: 13px;
        font-weight: bold;
        color: white;
    }
</style>