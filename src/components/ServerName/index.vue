<template>
    <div class="container">
        <div class="name">
            {{nameServer}}
        </div>
        <div class="icon">
            <ExpandIcon :size="28" />
        </div>
    </div>
</template>


<script>
    import ExpandIcon from 'vue-material-design-icons/ChevronDown';


    export default{
        props:{
            nameServer: String
        },
        components: {
            ExpandIcon
        }
    }
</script>


<style scoped>
    .container{
        display: flex;
        grid-area: SN;
        background-color: var(--tertiary);
        padding: 0 11px 0 16px;
        box-shadow: rgba(0, 0, 0, 0.9);
        z-index: 2;
        
        justify-content: space-between;
        align-items: center;
    }
    
    .name{
        font-size: 16px;
        color: white;
        font-weight: bold;
    }

    .icon{
        color: var(--white);
        cursor: pointer;
    }
</style>