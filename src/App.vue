<template>
  <div class="wrapper">
    <header>Shopping car</header>
    <div class="container">

      <div class="item"
            v-for="(item,index) in shopCar"
            :key="index"
      >
        <div class="logo">
          <img src="item.businessLogo">
          <span>{{ item.businessName }}</span>
        </div>
        <div class="details">
          <img src="item.commodityImg">
          <div class="details-list">
            <span>{{ item.commodityName }}</span>
            <div class="list-more">
              <span>Color: {{item.commodityColor}}</span>
              <span>Size: {{item.commoditySize}}</span>
            </div>
            <div class="list-price">
              ${{item.commodityPrice}}
            </div>
          </div>
        </div>
        <div class="num">
          <span>Number: </span>
          <div>
            <button>-</button>
            <input type="" name="" value="1">
            <button>+</button>
          </div>
        </div>
      </div>


    </div>
    <footer class="footer">
      <div class="footer-left">
        Price:
        <span>$1080.2 Free shipping </span>
      </div>
      <div class="footer-right">Payment</div>
    </footer>
  </div>
</template>

<script type="text/javascript">
  export default{
    data () {
      return {
        shopCar:[
          {
            id:"001",
            businessLogo:"https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR7mURUpDDSiSt2zKcCYaVQCAew63wR-JnnaQ&usqp=CAU",
            businessName:"NIKE",
            commodityImg:"https://m.media-amazon.com/images/I/61eoRxGMmfL._AC_UY879_.jpg",
            commodityName:"Nike Sweat Pant Men's Nsw Club Jogger Men's Nsw Club Jogger mens",
            commodityColor:"Gray",
            commoditySize:"L",
            commodityPrice:"95.31"
          },
          {
            id:"002",
            businessLogo:"data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBxAQERUSEhIVFRIWGBUXFRgWFRgVFRkYFRoXFxUWFhUbISggGBolHRUVITEhJSkrLi4uGB8zODMtNygtLisBCgoKDg0OGxAQGy8mICY1LS8tLzAtLy0wLS0tLy0tLS0vLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLf/AABEIAOEA4QMBIgACEQEDEQH/xAAcAAEAAgMBAQEAAAAAAAAAAAAABQcBBAYDAgj/xABFEAABAwIDAwkFBAcGBwAAAAABAAIDBBESITEFBkEHEyJRYXGBkaEyUnKCsUJiosEzU1SSssLRFCNDk9LhFRY0RGPi8P/EABoBAQADAQEBAAAAAAAAAAAAAAACAwQFAQb/xAA0EQACAQMCAwUHBAEFAAAAAAAAAQIDBBEhMQUSQRMiUWGRcYGhscHR8AYUMkIzFUNScuH/2gAMAwEAAhEDEQA/ALpREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAERc9vZvRHRMsLPmcOizgPvP6m/VRlJRWWWUaM601TgstkrtPakFM3HNI1g4XOZ7ANSe5cntDlJgbcQxPkPAuIjafK7vRVxX10tQ8ySvLnHieA6mjgOwLwawkgAEkmwAFySdABxK507yTfd0R9XbcAowWaz5n5aL7v26HYVPKRWO9hkTB8LnHzJt6LzoN4NsVb8ET3OPHCxgDe1zi2zQt3dvk/kktJUnA3UMB6Z+I/ZHZr3KxaGhigYGRMaxg0DRYf7ntVlKlWnrOTSMt1eWFv3LelGT8WspeuW/wA1IrYWyaqOz6qqklf7jTaMeNgXeg7FOoi2xjyrCPnqtWVSXNLHuSS9FoEWbLBt1qRWETEOseayAgMIiIMhERAEREAREQBERAEREAREQBERAERQm9O8MdFFiOcrriNnEnrPU0cT4cV5KSissnTpzqTUILLex472bzR0UZAs6cjoN6vvO+79fO1PVlU+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",
            businessName:"LINING",
            commodityImg:"https://m.media-amazon.com/images/I/51ps2OTqAHL._AC_UL600_FMwebp_QL65_.jpg",
            commodityName:"I-NING Lightning 2000 Badminton Racket",
            commodityColor:"Black",
            commoditySize:"One Size",
            commodityPrice:"119.99"
          },
          {
            id:"003",
            businessLogo:"https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR7mURUpDDSiSt2zKcCYaVQCAew63wR-JnnaQ&usqp=CAU",
            businessName:"NIKE",
            commodityImg:"https://m.media-amazon.com/images/I/61eoRxGMmfL._AC_UY879_.jpg",
            commodityName:"Nike Sweat Pant Men's Nsw Club Jogger Men's Nsw Club Jogger mens",
            commodityColor:"Gray",
            commoditySize:"L",
            commodityPrice:"95.31"
          },
          {
            id:"004",
            businessLogo:"https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR7mURUpDDSiSt2zKcCYaVQCAew63wR-JnnaQ&usqp=CAU",
            businessName:"NIKE",
            commodityImg:"https://m.media-amazon.com/images/I/61eoRxGMmfL._AC_UY879_.jpg",
            commodityName:"Nike Sweat Pant Men's Nsw Club Jogger Men's Nsw Club Jogger mens",
            commodityColor:"Gray",
            commoditySize:"L",
            commodityPrice:"95.31"
          }
        ]
      }
    }
  }

</script>

<style type="text/css">
  body {
    margin: 0;
    padding: 0;
    background:#f5f5f5;
  }

  .wrapper {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }

  header {
    height: 50px;
    width: 100%;
    position: fixed;
    left: 0;
    top: 0;
    background: #fff;
    z-index: 999;
    border-bottom: 1px solid #ccc;
    text-align: center;
    line-height: 50px;
  }

  .container {
    background: #fff;
    padding:50px;
    flex: 1;
  }

  .item {
    padding: 10px;
  }
  .container.item + .item{
    border-top:1px solid #ccc;
  }

  .logo {
    height: 40px;
    display:flex;
    align-items: center;

  }
  .logo img {
    width: 20px;
    height: 20px;
  }
  .logo span{
    color: #888;
    font-size:12px;
    margin-left: 20px;
  }
  .details {
    background: #f5f5f5;
    padding: 15px;
    display: flex;
    font-size: 12px;

  }
  .details img{
    width: 90px;
    height: 90px;
  }
  .details-list{
    margin-left:15px;
    color: #888;
  }
  .list-more span{
    display: block;
    color:#ccc;

  }
  .list-price{
    font-size:14px;
    color: black;
  }
  .num{
    color: #888;
    padding: 10px;
    display: flex;
    justify-content: space-between;
  }
  .num button{
    width: 25px;
    height: 25px;
    background:#e0e0e0;
    color: #58595b;
    border:none;
    outline: none;
  }
  .num input{
    width: 37px;
    height: 25px;
    border: none;
    text-align: center;
    background: #fff;
  }
  .footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 50px;
    width: 100%;
    position: fixed;
    bottom: 0;
    left: 0;
    z-index: 999;
    background-color: #fff;
    border-top: 1px solid #ccc;
  }

  .footer-left {
    text-align: right;
    line-height: 50px;
    font-size: 16px;
    padding-right: 6px;
  }

  .footer-left span {
    color: red;
  }

  .footer-right {
    background: red;
    color: #fff;
    width: 150px;
    height: 50px;
    line-height: 50px;
    text-align: center;
  }
</style>
