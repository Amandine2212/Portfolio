<script setup>
    const props = defineProps(['projet'])
    <script type="text/javascript" src="../CSS/scriptCDC.js"></script>
</script>

<template>
    <div class="SmallCard">
        <div class ="caroussel">
        <button class="btn" id="prev">&#10096;</button>
        <button class="btn" id="next">&#10097;</button>
        <ul>
            <li class="slide active">
                <img src="../images projets/CDCPage0.png" alt="Page0"> 
            </li>
            <li class="slide">
                <img src="../images projets/CDCPage1.png" alt="Page1"> 
            </li>
            <li class="slide">
                <img src="../images projets/CDCPage2.png" alt="Page2"> 
            </li>
            <li class="slide">
                <img src="../images projets/CDCPage3.png" alt="Page3">
            </li>
            <li class="slide">
                <img src="../images projets/CDCPage4.png" alt="Page4">
            </li>
            <li class="slide">
                <img src="../images projets/CDCPage5.png" alt="Page5"> 
            </li>
            <li class="slide">
                <img src="../images projets/CDCPage6.png" alt="Page6">
            </li>
            <li class="slide">
                <img src="../images projets/CDCPage7.png" alt="Page7">
            </li>
            <li class="slide">
                <img src="../images projets/CDCPage8.png"alt="Page8">
            </li>
            <li class="slide">
                <img src="../images projets/CDCPage9.png"alt="Page9">
            </li>
            <li class="slide">
                <img src="../images projets/CDCPage10.png"alt="Page10">
            </li>
            <li class="slide">
                <img src="../images projets/CDCPage11.png"alt="Page11">
            </li>
        </ul>
    </div>
        </div>
    </div>
</template>  


<style>
.text{
   display: flex;
   flex-direction: column;
   justify-content: center;
   padding: 25px;
   margin-top: 230px;
   text-align: justify;
}
.text p{
   font-size: medium;
   border-spacing: 5px 0;
   text-align: justify;
   color: #2a2523;
}

.ListeCDC{
   display: inline-block;
   font-size: medium;
   line-height: 1.4em;
   list-style:circle;
   margin: 15px;
}

.caroussel{
   height: 100%;
   width:80%;
   margin-top: 100px;
   position: relative;
}

.caroussel button{
   position: absolute;
   background:none;
   border: none;
   outline: none;
   font-size:2rem;
   z-index: 2;
   cursor: pointer;
   color:rgb(84,62,42);
   transform: translateY(-50%);
   top:50%;
}

#prev{
   left:5px;
}
#next{
   right:5px;
}

.caroussel li{
   list-style: none;
}

.slide{
   position: absolute;
   height: 100%;
   width: 100%;
   opacity: 0;
   transition: 0,4s ease-in-out;
}
.slide.active{
   opacity: 1;
}

.slide img{
   display: block;
   height: 80%;
   width: 100%;
   object-fit: cover;
}
</style> 
