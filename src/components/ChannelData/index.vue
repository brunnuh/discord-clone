<template>
  <div class="container_channel-data">
      <div class="messages">
         
          <FieldMessage name="Rodrigo Conceicao" v-for="msgs in 50" :key="msgs.id"  data="12/02/2012"> 
            Teste de mensagem
          </FieldMessage>
          <FieldMessage name="Rodrigo Conceicao" data="12/02/2012" isBot hasMention> 
            Teste de mensagem
          </FieldMessage>

      </div>
      <div class="input-wrapper">
         
          <input type="text" placeholder="Conversar em #chat-livre" />
            <div class="icon">
              <At :size="24"/>
            </div>
      </div>
  </div>
</template>

<script>
import FieldMessage from './FieldMessage';
import At from 'vue-material-design-icons/At';

export default {
    components:{
        FieldMessage,
        At
    }
}
</script>

<style lang="scss" scoped>
    .container_channel-data{
        grid-area: CD;
        background-color: var(--primary);
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        flex: 1;
    }

    .messages{
        display: flex;
        flex-direction: column;
        height:calc(100vh - 46px - 68px); /** altura da tela - 46px do topo e  = 68px do input-wrapper */
        max-height:calc(100vh - 46px - 68px);
        overflow-y: scroll; /** criar barra de rolagem no eixo y */

        &::-webkit-scrollbar{ /** scrool */
            width: 8px;
        }

        &::-webkit-scrollbar-thumb{
            background-color: var(--tertiary);
            border-radius: 4px;
        }

        &::-webkit-scrollbar-track{
            background-color: var(--secondary);
        }
    }

    .input-wrapper{
        width: 100%;
        padding: 0 16px;
        height: 68px;
   

        input{
            width: 100%;
            height: 44px;
            padding: 0 10px 0 57px;
            border-radius: 5px;
            color: var(--white);
            background-color: var(--chat-input);
            position: relative;

            &::placeholder{
                color: var(--grey);
            }

        }
    
        .icon{
            color: var(--grey);
            position: relative;
            top: -50%;
            left: 14px;
            transition: 0.2s;
            width: 24px;
        }
    }
</style>