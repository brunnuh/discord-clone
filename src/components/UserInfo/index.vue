<template>
    <div class="container_user_info">
        <div class="icon_and_infos">
            <div class="logo_user"></div>
            <div class="user_name_tag">
                <div class="name">
                    {{name}}
                </div>
                <div class="tag">
                    #{{id}}
                </div>
            </div>
        </div>
        <div class="icons">
            <MicrophoneIcon :size="20" class="icon_1"/>
            <HeadphoneIcon :size="20" class="icon_2"/>
            <SettingsIcon :size="20" class="icon_3"/>
        </div>
    </div>
</template>

<script>
import SettingsIcon from 'vue-material-design-icons/CogOutline';
import HeadphoneIcon from 'vue-material-design-icons/Headphones';
import MicrophoneIcon from 'vue-material-design-icons/Microphone';


export default {
    props:{
        name: String,
        id: Number
    },
    components:{
        SettingsIcon,
        HeadphoneIcon,
        MicrophoneIcon
    }
}
</script>

<style scoped lang="scss">
    .container_user_info{
        grid-area: UI;
        background-color: var(--quarternary);
        display: flex;
        flex-direction: row;
        width: 100%;
        height: 100%;
        padding: 15px 10px;
        justify-content: space-between;

        .icon_and_infos{
            display: flex;
            flex-direction: row;
            .logo_user{
                background-color: var(--grey);
                width: 40px;
                height: 40px;
                border-radius: 50%;
                margin-right: 7px;
            }

            .user_name_tag{
                margin-top: 3px;
                font-weight: 600;
                font-size: 13px;
                .name{
                    color: var(--white);
                }
            
                .tag{
                    color: var(--symbol);
                    margin-top: 2px;
                }
            }
        }
    
        .icons{
            margin-top: 6px;
            color: var(--symbol);
            cursor: pointer;
            span{
                 &:active,
                 &:hover{
                    color: var(--white);
                }
            }
            
        }
        
    }
</style>