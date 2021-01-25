<template>
  <div id="app">
    <ServerList />
    <ServerName nameServer="server vue"/>
    <ChannelList/>
    <UserInfo name="Bruno Santos" id="3213"/>
    <ChannelInfo />
    <ChannelData />
    <UserList />
  </div>
</template>

<script>
  import ServerList from './components/ServerList/index';
  import ServerName from './components/ServerName/index';
  import ChannelList from './components/ChannelList/index';
  import UserInfo from './components/UserInfo/index';
  import ChannelInfo from './components/ChannelInfo/index';
  import ChannelData from './components/ChannelData/index';
  import UserList from './components/UserList/index';

export default {
  name: 'App',
  components: {
    ServerList,
    ServerName,
    ChannelList,
    UserInfo,
    ChannelInfo,
    ChannelData,
    UserList
  }
}
</script>

<style scoped>
  #app{
    display: grid; /* tipo de display */
    height: 100vh; /** tamanho que essa pagina vai ocupar, no caso, toda a area */
    grid-template-columns: 71px 240px auto 240px; /** dividindo as colunas em 4 tamanhos, obs: a 3 parte pega o que sobrar */
    grid-template-rows: 46px auto 62px;/** dividindo em 3 linhas obs: a 2 pega o resto que sobrar */
    grid-template-areas: /** especificando as areas de cada componente */
      /*Colunas    1  2  3  4*/  
      /*1° Linha*/"SL SN CI CI"
      /*2° Linha*/"SL CL CD UL" 
      /*3° Linha*/"SL UI CD UL"
    ;
  }
</style>
