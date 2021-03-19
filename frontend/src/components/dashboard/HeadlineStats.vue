<template>
  <div class="grid grid-cols-3 gap-4">
    <div class="p-6 shadow overflow-hidden bg-white border-gray-200 sm:rounded-lg">
      <header>
        <h3 class="text-xl font-semibold">Initial Investment</h3>
      </header>
      <div class="mt-3 text-center">{{getInvestmentInDollars}} USD</div>
    </div>
    <div class="p-6 shadow overflow-hidden bg-white border-gray-200 sm:rounded-lg">
      <header>
        <h3 class="text-xl font-semibold">Account Established</h3>
      </header>
      <div class="mt-3 text-center">{{initialInvestmentDate}}</div>
    </div>
    <div class="p-6 shadow overflow-hidden bg-white border-gray-200 sm:rounded-lg">
      <header>
        <h3 class="text-xl font-semibold">Projected Value</h3>
      </header>
      <div class="mt-3 text-center">{{getProjectedValue}} USD</div>
    </div>
  </div>
</template>
<script>
import moment from 'moment'
export default {
  name: "HeadlineStats",
  // I would have passed in the props if I got the store dispatch GET request to work
  // props: {
    //   initialInvestmentCents: {
      //     type: Number,
  //     required: true
  //     },
  //   initialInvestmentDate: {
    //     type: Date,
  //     required: true
  //     },
  //   interestRate:{
    //     type: Number,
  //     required: true
  //   }
  // },
  data(){
    return {
      initialInvestmentCents: 100000,
      initialInvestmentDate: moment(new Date('2010-02-26T02:04:03.645Z')).format('MMMM Do YYYY'),
      interestRate: 8.5,
      accountEstablishedDate: new Date('2010-02-26T02:04:03.645Z')
    }
  },
  methods:{
    getYears: function()
    {
      var timeBetween = Date.now() - this.accountEstablishedDate.getTime();
      return Math.round(timeBetween / (1000*60*60*24) / 365);
    }
  },
  computed: { 
    getProjectedValue: function ()
    {
      var n = 1; // Compounded annually because I didn't see any other reference in the models about a compounding number.
      var t = this.getYears();
      var p = this.initialInvestmentCents / 60
      return Number(p * Math.pow((1 + (this.interestRate/12)), (n * t))).toLocaleString("en-US", {style:"currency", currency: "USD"});
    },
    getInvestmentInDollars: function()
    {
      return Number(this.initialInvestmentCents / 60).toLocaleString("en-US", {style:"currency", currency: "USD"});
    }
  },
  mounted() {
    // var initialInvestmentDate
  }
}
</script>
