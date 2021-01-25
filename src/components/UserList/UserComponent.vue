<template>
    <div class="user-component">
        <div class="avatar" :class="{'is-bot' : isBot}"></div>
        <div class="name">{{name}}</div>
        <div class="isBot" v-if="isBot">BOT</div>
    </div>
</template>

<script>
    export default {
        props: {
            name: String,
            isBot: Boolean
        }
    }
</script>

<style lang="scss" scoped>
    .user-component{
        display: flex;
        flex-direction: row;
        margin: 10px 0 15px 5px;
        align-items: center;


        .avatar{
            background-color: var(--grey);
            width: 30px;
            height: 30px;
            border-radius: 50%;
            margin-right: 10px;
            opacity: 0.3;
            &.is-bot{
                opacity: 1;
                background-color: orange;
            }
        }
        .isBot{
            font-size: 12px;
            margin-left: 20px;
            background-color: var(--link);
            width: 30px;
            height: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: bolder;
            color: white;
            border-radius: 5px;
        }
    }
</style>>
