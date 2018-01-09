<template>
  <div id='footer'>
      <ul>
          <li v-for="(item,index) in list" :key="index" :class="{'active':item.active}" v-link="item.path">
              <p class="iconfont" :class="item.icon,icon.active?item._icon:''"></p>
              <span>{{item.label}}</span>
          </li>
      </ul>
  </div>
</template>
<script>
export default {
  name:'footers',
  props:{
      active:{
          type:String
      }
  },
  data(){
      return{
          list:{
             home:{
                label:"首页",
                icon:'icon-home',
                _icon:'icon-homefill',
                path:'home',
                active:false
             },
            sort:{
                label:"分类",
                icon:'icon-sort',
                _icon:'icon-sortfill',
                path:'sort',
                active:false
            },
            cart:{
                label:'购物车',
                icon:'icon-cart',
                _icon:'icon-cartfill',
                path:'cart',
                active:false
            },
            user:{
                label:'我的',
                icon:'icon-user',
                _icon:'icon-userfill',
                path:'user',
                active:false
            }
          }
      }
  },
  created(){
      let key=this.active;
      this.list[key].active=true;
  }

}
</script>

<style lang='scss'>
    @import '../../../static/css/reset.css';
    #footer {
        position: fixed;
        display: flex;
        width: 100%;
        height: 40px;
        box-sizing: border-box;
        left: 0;
        bottom: 0;
        border-top:1px solid #ccc;
        ul li{
            flex:1;
            text-align: center;
            box-sizing: border-box;
            p{
                display: block;
                height: 100%;
                line-height: 64px;
                text-align: center;
                font-size: .26rem;
                color:#999;
            }
        }
          .nav-item a.active{
        color:#fc5879;
    }
    .icon-home{
        background: url("./assets/navicon1.png") no-repeat  center 2px;
        background-size: .43rem;
    }
    .icon-homefill{
        background: url("./assets/navicon1-1.png") no-repeat  center 2px;
        background-size: .43rem;
    }
    .icon-sort{
        background: url("./assets/navicon2.png") no-repeat  center 2px;
        background-size: .43rem;
    }
    .icon-sortfill{
        background: url("./assets/navicon2-1.png") no-repeat  center 2px;
        background-size: .43rem;
    }
    .icon-cart{
        background: url("./assets/navicon3.png") no-repeat  center 2px;
        background-size: .43rem;
    }
    .icon-cartfill{
        background: url("./assets/navicon3-1.png") no-repeat  center 2px;
        background-size: .43rem;
    }
    .icon-user{
        background: url("./assets/navicon4.png") no-repeat  center 2px;
        background-size: .43rem;
    }
    .icon-userfill{
        background: url("./assets/navicon4-1.png") no-repeat  center 2px;
        background-size: .43rem;
    }
    }
</style>
