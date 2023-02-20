<template>
  <nav>
    <div class="logo"><span>/</span>Rareblocks</div>
      <div  :class="isDisplayed ? 'false':'true'" class="menu">
        <li class="live-preview">Live Preview</li>
        <li>Features</li>
        <li>Documentation</li>
        <li>Help</li>
      </div>
      <div class="cart">
        <div class="number">2</div>
      </div>
      <div class="menu-bar" @click="toggleDisplayed"></div>
  </nav>

  <div class="content">
    <div class="right-content">
        <h1>Build SaaS Landing Page without Writing a Single Code</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. In nunc nisl eu consectetur. Mi massa elementum odio eu viverra amet.</p>
        <div class="buttons">
          <button class="btn1">Get UI Kit Now</button>
          <button class="btn2">Check live preview</button>
        </div>
    </div>
    <div class="left-content">
      <img src="../src/assets/hero.png" alt="">
    </div>
  </div>
</template>

<script>
  export default{
    data() {
      return{
        isDisplayed: true,
      }
    },
    methods: {
        toggleDisplayed(){
          this.isDisplayed = !this.isDisplayed
          console.log(this.isDisplayed);
        }
    },
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:ital,wght@0,400;0,700;1,500&family=Work+Sans:wght@500&display=swap');
  *{
    margin: 0;
    padding: 0px;
    font-family: 'plus jakarta sans';
    cursor: default;
    color: #fff;
  }
  body{
    background: #18181B;
  }
  #app{
    display: flex;
    align-items: center;
    justify-content: flex-start;
    flex-direction: column;
  }
  nav{
    background: #18181B;
    width: 100%;
    height: 82px;
    border-bottom: 1px solid #27272A; 
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  nav .logo{
    margin: 0px 0px 0px 28px;
    color: #fff;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    font-size: 16px;
  }
  nav .logo span {
    color: #F43F5E;
  }
  nav .menu{
    /* display: flex; */
    width: 441px;
    align-items: center;
    justify-content: space-between;
  }
  nav .menu li{
    font-size: 16px;
    color: #A1A1AA;
    cursor: pointer;
    list-style: none;
  }
  nav .menu li:hover{
    color: #fff;
  }
  nav .menu .live-preview{
    color: #fff;
  }
  nav .cart{
    width: 29px;
    height: 31px;
    margin: 0px 39px 0px;
    background: blue;
    display: flex;
    align-items: flex-start;
    justify-content: flex-end;
    background: url(../src/assets/Icon.svg) no-repeat center;
    cursor: pointer;
  }
  nav .cart .number{
    width: 21px;
    height: 21px;
    border-radius: 50px;
    background: #5754FF;
    z-index: 1;
    color: #fff;
    font-family: 'work sans';
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    top: -10px;
    right: -5px;
    font-size: 13px;
  }
  .menu-bar{
    display: none;
  }

  .content{
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    height: 100%;
    margin: 57px 0px 0px ;
  }
  .content .right-content{
    width: 440px;
    margin: 0px 0px 0px 152px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }
  .content .right-content h1{
    width: 100%;
    font-weight: 700;
    font-size: 42px;
  }
  .content .right-content p{
    color: #A1A1AA;
    margin: 29px 0px 0px;
  }
  .content .right-content .buttons{
    display: flex;
    justify-content: space-between;
    margin: 47px 0px 0px;
  }
  .content .right-content .btn1{
    width: 157px;
    height: 54px;
    background: #FFFFFF;
    border-radius: 5px;
    border: none;
    color: #18181B;
    font-weight: 700;
    font-size: 14px;
    cursor: pointer;
  }
  .content .right-content .btn2{
    width: 157px;
    height: 54px;
    background: #27272a8e;
    border-radius: 5px;
    border: none;
    color: #fff;
    font-weight: 700;
    font-size: 14px;
    margin: 0px 0px 0px 39px;
    cursor: pointer;
  }
  .content .right-content .btn2:hover{
    background: #27272A;
    transition: .2s;
  }
  .content .left-content{
    height: 100%;
    width: 100%;
    display: flex;
    justify-content: flex-end;
    overflow: hidden;
  }
  .content .left-content img{
    width: 1008.61px;
    height: 683.92px;
  }


  .false,.true{
    display: flex;
  }
  @media (max-width: 1000px) {
    nav .logo{
      font-size: 16px;
      margin: 0px 0px 0px 35px;
    }
  }
  @media (max-width: 1500px) {
    .content .left-content img{
      width: 850px;
      height: 576.37px;
    }
  }
  @media (max-width: 1350px) {
    .content .left-content img {
      width: 750px;
      height: 508.56px;
    }
  }
  @media (max-width: 1260px) {
    .content{
      display: flex;
      flex-direction: column-reverse;
      align-items: center;
      justify-content: flex-start;
    }
    .content .right-content{
      margin: 0px;
    }
    .content .left-content img{
      width: 1008.61px;
      height: 683.92px;
    }
    .content .right-content{
      margin: 50px 0px 
    }
  }
  @media (max-width: 985px) {
    nav{
      position: fixed;
    }
    nav .logo{
      font-size: 18px;
    }
    nav .menu{
      position: fixed;
      top: 58px;
      width: 100%;
      flex-direction: column;
      align-items: center;
      justify-content: flex-start;
      margin: 25px 0px 0px ;
      background: #18181B;
    }
    nav .menu li{
      margin: 20px 0px 10px;
      width: 100%;
      border-bottom: 1px solid #27272a4f;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    nav .cart{
      display: none;
    }
    nav .menu-bar{
      display: block;
      width: 36px;
      height: 13.5px;
      background: url('../src/assets/menu-bar.svg');
      margin: 0px 39px 0px;
    }
    .false{
      display: none;
    }
    .true{
      display: flex;
    }
    .content .left-content img{
      width: 900px;
      height: 610.27px;
    }
  }
  @media (max-width: 820px) {
   .content .left-content img{
      width: 800px;
      height: 542.47px;
    }
  }
  @media (max-width: 740px) {
    .content .left-content img{
      width: 680px;
      height: 461.1px;
    }
  }
  @media (max-width: 625px) {
    .content .left-content img{
      width: 595px;
      height: 403.46px;
    }
  }

  @media (max-width: 550px) {
    nav .logo{
      font-size: 16px;
    }
    .false{
      display: none;
    }
    .true{
      display: flex;
    }
    .content .left-content img{
      width: 500px;
      height: 339.04px;
    }
    .content .right-content{
      align-items: center;
      text-align: center;
      /* justify-content: center; */
    }
    .content .right-content h1{
      font-size: 32px;
    }
  }
  @media (max-width: 450px) {
    .content .left-content img{
      width: 420px;
      height: 284.8px;
    }
    .content .right-content{
      width: 90%;
    }
    .content .right-content h1{
      font-size: 22px;
    }
    .content .right-content .btn1{
      width: 120px;
      height: 41.27px;
      font-size: 12px;
    }
    .content .right-content .btn2{
      width: 120px;
      height: 41.27px;
      font-size: 11px;
    }
  }
</style>
