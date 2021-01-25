<template>
    <div class="user-list">
        <div class="users-online">
            <div class="title">
                DISPONIVEL - 1
            </div>
            <UserComponent name="Maikel Neris"/>
            <UserComponent name="Kleito Neris"/>
            <UserComponent name="News bot" isBot/>
        </div>
        <div class="users-offline">
            <div class="title">
                OFFLINE - 24
            </div>
            <UserComponent name="Pedro Sousa" isBot/>
            <UserComponent v-for='users in 50' :key="users.id" name="Joaquim Silva"/>
        </div>
    </div>
</template>

<script>
    import UserComponent from './UserComponent';

    export default {
        components:{
            UserComponent
        }
    }
</script>

<style lang="scss" scoped>
    .user-list{
        grid-area: UL;
        display: flex;
        flex-direction: column;
        background-color: var(--secondary);
        color: var(--white);
        padding: 20px 15px;
        overflow-y: scroll;

        &::-webkit-scrollbar{
            display: none;
        }
        .title{
            font-size: 14px;
            color: var(--grey)
        }
    }
</style>>
