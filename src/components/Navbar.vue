<template>
  <div>
  <b-navbar toggleable="lg" type="dark">


    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
       
      </b-navbar-nav>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto text">
      
      
      <b-nav-item href="#"><span>TRIPS</span></b-nav-item>

      <b-nav-item href="#"><span> RECENTLY VIEWED</span></b-nav-item>
      
      <b-nav-item href="#"><span> BOOKINGS</span></b-nav-item>
      
      <b-nav-item href="#">  
       <img src="../assets/user.png"  alt="user"/>

      </b-nav-item>

      


       
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</div>
</template>

<script>
export default {
  name: 'SideBar',
  props: {
    users: Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">

.text{

    
    padding:3rem 0rem;
    align-items: flex-end;
    

    // & > a:not(:last-child) {
        
    // }
    span{
        color: black;
        margin-right: 3rem;
        // font-weight: bolder;

    }
    // img{

    //     width: 3rem;
    //     object-fit: contain;
    // }
    
}

.navbar-dark .navbar-toggler {
    color: rgba(255, 255, 255, 0.5);
    border-color: rgba(255, 255, 255, 0.1);
    background-color: #3f67e9;
 
}

@media screen and (max-width: 600px) {
    .text{
  
      align-items: normal;
    }
    }


</style>
