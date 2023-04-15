<template>
    <nav>
      <input type="checkbox" name="check" id="check" v-model="isOpen" />
      <label for="check" class="checkbtn">
        <i class="fas fa-bars"></i>
      </label>
      <img src="../assets/logo.svg" alt="Logo" class="logo" />
      <ul :class="{ 'active': isOpen }">
        <li><a href="#">About</a></li>
        <li><a href="#">Sponsors</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isOpen: false
      };
    }
  };
  </script>
  
  <style scoped>
  * {
    padding: 0;
    margin: 0;
    text-decoration: none;
    list-style: none;
  }
  
  nav {
    background-color: #02071a;
    width: 100%;
    height: 80px;
    display: flex;
    justify-content: space-around;
    align-items: center;
  }
  
  .logo {
    color: white;
    font-size: 35px;
    line-height: 80px;
    font-weight: bold;
    padding-left: 100px;
  }
  
  ul {
    float: right;
    margin-right: 20px;
  }
  
  ul li {
    display: inline-block;
    line-height: 80px;
    margin-left: 5px;
  }
  
  ul li a {
    color: white;
    font-size: 17px;
    text-transform: uppercase;
    padding: 7px 13px;
    border-radius: 3px;
  }
  
  .checkbtn {
    font-size: 30px;
    color: white;
    float: right;
    line-height: 80px;
    margin-right: 40px;
    cursor: pointer;
    display: none;
  }
  
  #check {
    display: none;
  }
  
  @media (max-width: 952px) {
    .logo {
      font-size: 30px;
      padding-left: 50px;
    }
  
    ul li a {
      font-size: 16px;
    }
  }
  
  @media (max-width: 715px) {
    .checkbtn {
      display: block;
    }
  
    img {
      width: 50vw;
    }
  
    ul {
      position: fixed;
      width: 100%;
      height: 100vh;
      background-color: #2c3e50;
      top: 80px;
      left: -100%;
      text-align: center;
      transition: all 0.5s;
    }
  
    .active {
      left: 0;
    }
  
    ul li {
      display: block;
      margin: 50px 0;
      line-height: 30px;
    }
  
    ul li a {
      font-size: 20px;
    }
  }
  </style>
  