<template>
  <div class="container_channelinfo">
      <div class="chat_name">
          <PoundIcon />
          <p>Vue</p>
      </div>
      <div class="space"></div>
      <span class="text">
          Canal aberto para conversas
      </span>
  </div>
</template>

<script>
    import PoundIcon from 'vue-material-design-icons/Pound';
    export default {
        components:{
            PoundIcon
        }
    }
</script>

<style scoped lang="scss">
    .container_channelinfo{
        grid-area: CI;
        display: flex;
        flex-direction: row;
        background-color: var(--quinary);
        align-items: center;
        padding-left: 20px;
        z-index: 2;


        .chat_name{
            display: flex;
            flex-direction: row;
            
            p{
                margin: 4px 10px ;
                color: var(--white);
                font-size: 15px;
                font-weight: 700;
            }
            
            span{
                color: var(--symbol);
            }
        }

        .space{
            height: 20px;
            width: 0.5px;
            background-color: var(--grey);
        }

        .text{
            margin-left: 10px;
            color: var(--grey);
            font-weight: 700;
        }
    }
</style>