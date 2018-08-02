<template>
  <div class="row">
    <div class="col-md-8">
      map
    </div>
    <div class="col-md-4 menu">
      <div class="logo">
        <img src='./../../assets/logo1.png' class="img-fluid img-responsive"/>
      </div>
      <div class="nv">
        <ul class="list-unstyled">
          <li>
            <input type="text" class="form-control form-control-lg" placeholder="search location">
          </li>
          <li>
            <div class="input-group">
              <div class="input-group-prepend">
                <div class="input-group-text">
                  Select a Specific Time
                </div>
                <datepicker class="date" input-class="form-control-lg" placeholder="EX:9/8/2018"></datepicker>
              </div>
            </div>
          </li>
        </ul>
        <div class="charts">


        </div>
      </div>
    </div>
  </div>
</template>

<script>
  /* ============
   * Home Index Page
   * ============
   *
   * The home index page.
   */
  // eslint disabled
  /* eslint-disable no-alert, no-console */

  import VLayout from '@/layouts/Default';
  import VCard from '@/components/Card';
  import Datepicker from 'vuejs-datepicker';
  

  export default {
    /**
     * The name of the page.
     */
    name: 'home-index',

    /**
     * The components that the page can use.
     */
    components: {
      VLayout,
      VCard,
      Datepicker,
    },
    data(){
      return{
        date:'',
      }
    },
    mounted(){
      let dt = new Date()
      this.date=dt.toDateString
    }
  };
</script>
<style>
.menu{
  position: fixed;
  background:#f6f6e9;
  right: 0;
}
.menu .logo img{
width: 20em;
height: 20em;
}
</style>

