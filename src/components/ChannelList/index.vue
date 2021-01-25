<template>
    <div class="container">
        <div class="title_channel">
            <div class="title">
                CANAIS DE TEXTO
            </div>
            <div class="icon">
                <PlusIcon :size="16"/>
            </div>
        </div>
        <ChannelText channel_name="vue" selected/>
        <ChannelText channel_name="apex"/>
        <ChannelText channel_name="Fortnite"/>
    </div>
</template>


<script>
    import PlusIcon from 'vue-material-design-icons/Plus';
    import ChannelText from './channel_text';


    export default{
        components:{
            PlusIcon,
            ChannelText
        }
    }
</script>

<style scoped>
    .container{
        grid-area: CL;
        background-color: var(--secondary);
        display: flex;
        flex-direction: column;
    }

    .title_channel{
        display: flex;
        justify-content: space-between;
        color: var(--senary);
        padding: 20px 10px 0 10px;
    }

    .title{
        font-size: 13px;
    }

    .icon{
         cursor: pointer;
    }
</style>