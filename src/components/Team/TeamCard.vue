<template>
  <li class="transition">
    <div class="wrapper">
        <img target='_blank' class="image" height='100%' width="100%" v-lazy="memberImageUrl">
      <span class="transition">
      <h3 style="font-family:Comfortaa,cursive,'DejaVu Sans'">{{member.name}} <em>{{member.designation}}</em></h3>
        <a :href="member.facebook_link" target="_blank">
          <i class="fa fa-facebook"></i>
          </a>
     </span> </div>
  </li>
</template>

<script>
    export default {
        name: "TeamCard",
        props:{
            member:{required:true}
        },
        computed:{
            memberImageUrl(){
                return {
                    src:'http://res.cloudinary.com/ashishpatel0720/image/upload/v1520713373/team/'+this.member.name.split(" ")[0]+'.jpg',
                };
            }
        }
    };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped>
  img {
    max-width: 100%;
    height: auto;
  }
  body {
    font-family: 'Source Sans Pro', sans-serif;
    text-align: center;
    padding-top: 60px;
  }
  h2 {
    font-size: 50px;
    margin-bottom: 0px;
    font-weight: 100;
  }
  p {
    font-size: 18px;
  }
  .transition {
    transition: .3s cubic-bezier(.3, 0, 0, 1.3)
  }
  .three .transition {
    transition: .7s cubic-bezier(.3, 0, 0, 1.3)
  }
  .five .transition {
    transition: .5s cubic-bezier(.3, 0, 0, 1.3)
  }
  /* --------- TWO --------- */

  .two {
    list-style: none;
    padding: 0;
    margin: 100px 0;
  }
  .two > li {
    background: #FFFFFF;
    border: 1px solid rgba(150,150,150,0.29);
    -moz-box-shadow: 0px 0px 18px 0px rgba(103,85,85,0.39);
    box-shadow: 0px 0px 18px 0px rgba(103,85,85,0.39);
    width: 250px;
    height: 430px;
    display: inline-block;
    margin: 0 20px;
    text-align: center;
  }
  .two > li img {
    /*margin-top: 60px;*/
    margin-top: 0px;
  }
  /*.two > li:hover img {*/
  /*margin-top: 30px;*/
  /*}*/
  .two > li:hover {
    -moz-box-shadow: 0px 0px 5px 0px rgba(103,85,85,0.25);
    box-shadow: 0px 0px 5px 0px rgba(103,85,85,0.25);
  }
  .two > li:hover span {
    border-radius: 0;
    -webkit-border-radius: 0;
    -moz-border-radius: 0;
    /*bottom: -400px;*/
    bottom: -320px;
  }
  .two > li:hover h3 {
    color: rgba(255,255,255,1);
    margin-top: 25px;
  }
  .two > li .wrapper {
    overflow: hidden;
    position: absolute;
    width: 250px;
    height: 430px;
  }
  .two > li span {
    border-radius: 50%;
    -webkit-border-radius: 50%;
    -moz-border-radius: 50%;
    height: 500px;
    width: 500px;
    background: #BE2F41;
    display: block;
    position: absolute;
    bottom: -280px;
    left: -125px;
  }
  .two > li span i {
    color: #fff;
    text-transform: uppercase;
    border-radius: 50px;
    -moz-border-radius: 50px;
    -webkit-border-radius: 50px;
    border: 2px solid #fff;
    padding: 10px 30px;
    font-style: normal;
    margin-top: 10px;
    display: inline-block;
  }
  .two > li span:hover {
    background: #532538;
  }
  .two > li h3 {
    margin-top: 40px;
    color: rgba(255,255,255,1);
  }
  .two > li h3 em {
    display: block;
    font-style: normal;
    text-transform: uppercase;
    font-weight: 300;
    font-size: 12px;
    margin-top: 5px;
  }
  .two .social {
    list-style: none;
    text-align: center;
    margin: 10px 0 0 0;
    padding: 10px;
  }
  .two .social li {
    opacity: 0;
    padding: 5px;
    display: inline-block;
  }
  .two > li:hover .social li {
    opacity: 0.9;
  }
  .two .social li a {
    cursor: pointer;
    display: block;
    opacity: 1;
  }
  .two .social li a:hover {
    opacity: 0.5;
    margin-top: 80px;
  }
  .two > li:hover .social li a {
    -webkit-animation: social-show 0.5s 1;
    -moz-animation: social-show 0.5s 1;
    -o-animation: social-show 0.5s 1;
    animation: social-show 0.5s 1;
    -webkit-animation-delay: 0s;
    -moz-animation-delay: 0s;
    -o-animation-delay: 0s;
    animation-delay: 0s;
  }
  .two .social li img {
    width: 24px;
  }
  @-webkit-keyframes social-show {
    from {
      margin-top: 140px;
    }
    to {
      margin-top: 80px;
    }
  }
  @-moz-keyframes social-show {
    from {
      margin-top: 140px;
    }
    to {
      margin-top: 80px;
    }
  }
  @-o-keyframes social-show {
    from {
      margin-top: 140px;
    }
    to {
      margin-top: 80px;
    }
  }
  @keyframes social-show {
    from {
      margin-top: 140px;
    }
    to {
      margin-top: 80px;
    }
  }
</style>
