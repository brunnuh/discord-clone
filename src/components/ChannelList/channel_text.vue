<template>
    <div class="container_channel" :class='{active:selected}'>
       <div class="first" >
            <div class="icon_pound">
                <PoundIcon />
            </div>
            <div class="title">
                {{channel_name}}
            </div>
       </div>
        <div class="icon_account" >
            <AccountPlusIcon  :size="17"/>
            <SettingsIcon :size="17"/>
        </div>
    </div>
</template>

<script>
    import PoundIcon from 'vue-material-design-icons/Pound';
    import AccountPlusIcon from 'vue-material-design-icons/AccountPlus';
    import SettingsIcon from 'vue-material-design-icons/CogOutline';

    export default{
        props: {
            channel_name: String,
            selected: Boolean
        },
        components: {
            PoundIcon,
            AccountPlusIcon,
            SettingsIcon
        }
    }
</script>


<style scoped lang="scss">
    .container_channel{
        display: flex;
        flex-direction: row;
        padding: 10px 0px 0px 10px;
        justify-content: space-between;
        color: var(--senary);
        border-radius: 5px;
        background-color: transparent;
        &:hover,
        &:active{
            background-color: var(--quinary);
            color: var(--white);
        }
    }

    .first{
        display: flex;
        flex-direction: row;
    }

    .icon_pound{
        margin-right: 10px;
    }

    .title{
        font-weight: bold;
    }

    .icon_account{
        display: block;
        padding-right: 10px;
        cursor: pointer;
    }
    .active{
        background-color: var(--quinary);
        color: var(--white);
    }
</style>