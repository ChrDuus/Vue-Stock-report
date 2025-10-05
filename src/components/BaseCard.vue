<template>
    <div class="BaseCard">
        <ul>
  <li v-for="(num, i) in revenue" :key="i">{{ num }}</li>
</ul>
        <slot></slot>
    </div>

</template>

<script>
import { stockService } from '@/services/stockService';
export default{
    name: 'BaseCard',
    components:{

    },
    data() {
    return {
      revenue: [],      
      loading: true,    
      error: null,      
    };
},
async created() {
    try {
      const result = await stockService.getRevenue('$AAPL'); 
      this.revenue = result; 
      console.log("SERVICE RESULT:", result);
    } catch (err) {
      console.error(err);
      this.error = "Error loading Data";
    } finally {
      this.loading = false;
    }
  },
}

</script>

<style>
.BaseCard{
    border-radius: 16px;
    background-color: #011F35;
    padding: 24px 32px;

}

</style>