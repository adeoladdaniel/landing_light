<template>
<div>
 
 <Navbar v-bind:users="users"/>


<div class="hrr">  <hr/> </div>

<b-container class="bv-example-row">
  <b-row class="w-100" cols="2">
    <b-col md="6">
          <div class="text-move">
                <h4>Payment Information</h4>  
                <span>Choose your method of payment.</span>
                
            </div>

             <div class="mastercard">
                <div>
                    <span>CARD NUMBER</span><br/><br/>

                    <p> 4 3 2 4 &nbsp;&nbsp; 5 4 3 3 &nbsp;&nbsp; 9 3 8 2 &nbsp;&nbsp; 1 0 3 0</p>

                    <img class="palet" src="../assets/palet.png"  alt="pelt"/>

                    <span class="exp">EXPIRATION DATE<br/><br/>

                        03/24<br/><br/>

                        John Doe
                    </span>
                    <img  class="master" src="../assets/mastercard.png" alt="master"/>
                </div>

            </div>
    </b-col>
    <b-col md="6">
          <div class="card-info">
                <div class="img-sec">
                        <img src="../assets/paypal.png" alt="paypal" class="pay"/>
                        <img src="../assets/discover.png" alt="discover"/>
                        <img src="../assets/visa.png"  alt="visa"/>
                </div>
                <div class="card-details">
                      <b-row>
                         <b-col md="6">
                             
                            <div>  <span>Credit card number</span></div>
                            <input placeholder="4324   5433   9382   1030"/>
                         </b-col>
                         <b-col md="6">
                             <div> <span className="s-span">Expiration date</span></div>
                             <input placeholder="03/24" className="s-input"/><br/><br/><br/>
                         </b-col>
                     </b-row>

                      <b-row>
                             <b-col>
                                <div>  <span>Credit card number</span></div>
                                <input placeholder="4324   5433   9382   1030"/>
                             </b-col>
                             <b-col>
                                 <div> <span >Expiration date</span></div>
                                 <input placeholder="03/24" /><br/><br/><br/>
                             </b-col>
                     </b-row>

                     <b-row>
                         <b-col md="12">
                             <div>
                            <label class="rcontainer">
                            <input type="radio" checked="checked" name="radio"/>
                            <span class="checkmark"></span>
                            </label> <br/>
                             <span class="use">Use the card for the time purchase</span><br/>
                    </div>
                    <button class="ripple">Add Card</button>
                         </b-col>
                     </b-row>
                </div>
          </div>
    </b-col>
   
  </b-row>
</b-container>
 <div class="hrrr">  <hr/> </div>

 <b-container>
        <div class="subtotal">
            <span>Subtotal <b>₦2,497.00</b></span>
            <br/><br/>
            <span>Estimated TAX <b>₦119.64</b></span>
            <br/><br/>
            <span>Promotional Code <b>₦-60.00</b></span>

        </div>
 </b-container>
        <div class="hrrr">  <hr/> </div>
<b-container>
     <div class="complete">
                <button class="rippler">
                    Complete Payment
                </button>
                <span> TOTAL: ₦2,497.00 </span>
            </div>
</b-container>
</div>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'
import users from './user.json'




export default {
  name: 'Home',
  components: {
    Navbar,
    
  },

  data(){
     return{
        users
     }
  },
  mounted(){
     console.log(typeof(users));
  }
}
</script>

<style lang="scss">
.hrr{
    padding: 0rem 5rem 0rem 5rem;
}
.text-move{

    margin-top: 3rem;
    span{
        font-size: 14px;
        color: #d3d6dc;
    }
    // h4{
    //     // font-weight: bold;
    // }
}

.mastercard{

    width: 29rem;
    padding: 2rem 2rem;
    height: 19rem;
    border-radius: 5px;
    margin: 4rem 0rem;
    background: linear-gradient(to left, #6463c2, #9f55af, #c54891, #d8476d,#c2565f);
p{
    color: white;
}
span{
    color: white;
    font-size: 10px;
}

}
.palet{
    width: 21%;
    margin: 0rem -2rem;
}
.exp{
    position: absolute;
    bottom: 6rem;
    margin: 0rem -1rem;
}
.master{
    width: 21%;
    float: right;
    margin-top: 6rem;
}

.card-info{
    margin-top: 3rem;

}
.img-sec{
    align-items: flex-end;
    margin-right: -2rem;
    margin-top: 4.5rem;


    img{
        width: 2rem;
        float: right;
        margin-right: 1rem;
    }
}
.pay{
    width: 4rem !important;
    margin-left: 2rem !important;

}
.card-details{
        padding-top: 5rem;

    span{
        font-size: 14px;
        color: #626262;
    }
    input{
        margin-top: 0.5rem;
        width: 100%;
        height: 2.5rem;
        background: #eff0f2;
    border: none;
    border-radius: 5px;
    font-size: 13px;
    padding: 1.5rem;
    }
    input:focus{
        outline: none;
    }


    
}
.rcontainer input {
  position: absolute;
  opacity: 0;
  cursor: pointer;
}

/* Create a custom radio button */
.checkmark {
    position: absolute;
    top: 0.5rem;
    left: 1rem;
    height: 25px;
    width: 25px;
    background-color: #eee;
    border-radius: 50%;
    margin-top: 1rem;
}


/* On mouse-over, add a grey background color */
.rcontainer:hover input ~ .checkmark {
  background-color: #ccc;
}

/* When the radio button is checked, add a blue background */
.rcontainer input:checked ~ .checkmark {
  background-color: #2196F3;
}

/* Create the indicator (the dot/circle - hidden when not checked) */
.checkmark:after {
  content: "";
  position: absolute;
  display: none;
}


.rcontainer input:checked ~ .checkmark:after {
  display: block;
}


.rcontainer .checkmark:after {
 	top: 9px;
	left: 9px;
	width: 8px;
	height: 8px;
	border-radius: 50%;
	background: white;
}
.use{
    padding: 0.7rem 3rem;
}



.ripple {
    background-position: center;
    transition: background 0.8s;
    margin-top: 2rem;
    width: 100%;
    padding: 1rem;
    border: none;
    border-radius: 4px;
    color: white;
    background: #3f67e9;
  }
  .ripple:hover {
    background: #466be6 radial-gradient(circle, transparent 1%, #466be6 1%) center/15000%;
  }
  .ripple:active {
    background-color: #6eb9f7;
    background-size: 100%;
    transition: background 0s;
  }

  .hrrr{
    padding: 2rem 6rem 0rem 5rem;
}
.subtotal{
    // span{
    //     // font-weight: bolder;

    // }

    b{
        float: right;
    }
}
.rippler{
    border: none;
    padding: 1rem 4rem;
     border-radius: 4px;
    background: #3f67e9;
    color: white;
    background-position: center;
    transition: background 0.8s;
}
.rippler:hover {
background: #466be6 radial-gradient(circle, transparent 1%, #466be6 1%) center/15000%;
}
.rippler:active {
background-color: #6eb9f7;
background-size: 100%;
transition: background 0s;
}

.complete{


    margin-top: 3rem;
    margin-bottom: 5rem;
    span{

    
    font-size: 22px;
    float: right;
    font-weight: bolder;
    padding: 1rem 0rem;
}
}

@media screen and (max-width: 600px) {
    .exp{
       
        margin: -0.5rem -1rem;
    }
  }

  @media screen and (max-width: 600px) {
    .img-sec{
       
        margin-top: -4.5rem;
        margin-right: 0rem;
    }
  }
  @media screen and (max-width: 600px) {
    .rippler {
        padding: 1rem 2rem;
    }
    .mastercard{
        width: 22rem;
    }
    .row-cols-2 > * {
    flex: 100% !important;
    max-width: 100% !important;
}

  }



</style>