<template>
    <div class="container_field-message" :class="{ 'has-mention' : hasMention }">
        <div class="avatar" :class="{ 'bot-avatar' : isBot }"></div>
        <div class="fields">
            <div class="name_data">
                <div class="name">{{name}}</div>
                <div v-if='isBot' class="isBot">BOT</div>
                <div class="data">{{data}}</div>
            </div>
            <div class="message"><slot/></div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        name: String,
        data: String,
        hasMention: Boolean,
        isBot: Boolean
    }
}
</script>

<style scoped lang="scss">
    .container_field-message{
        display: flex;
        flex-direction: row;
        align-items: center;
        padding: 8px 16px;
        background-color: transparent;
        margin-top: 13px;

        &.has-mention{
            border-left: solid 2px var(--mention-detail);
            background-color: var(--metion-message);
        }

        .avatar{
            width: 48px;
            height: 48px;
            border-radius: 50%;
            margin-right: 10px;
            background-color: var(--quarternary);
            opacity: 0.5;
            flex-shrink: 0; /** nao distorcer caso redimensionar */
            &.bot-avatar{
                background-color: var(--mention-detail);
            }
        }
        .fields{
            color: var(--white);
            .name_data{
                display: flex;
                flex-direction: row;
                .name{
                    font-weight: 700;
                }
                .data{
                    margin: 2px 0 0 6px;
                    font-size: 13px;
                    color: var(--grey)
                }
                .isBot{
                    display: flex;
                    background-color: var(--link);
                    font-size: 13px;
                    width: 35px;
                    margin-left: 6px;
                    border-radius: 3px;
                    align-items: center;
                    justify-content: center;
                }
            }
        }
        .message{
            margin-top: 5px;
        }
      
        &:hover{
            background-color: var(--quarternary);
        }
    }

</style>