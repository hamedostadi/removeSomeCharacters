<template>
  <v-container>
    <v-layout row>
      <v-flex xs4>
        <v-text-field
            v-model="text"
            label="شبا"
            :hint="'شبای شما:'+ text"
          ></v-text-field>
      </v-flex> 
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'pmBox',
  data () {
      return {
        text: '',
    }
    },
    watch: {
      text:function(val) {

       this.text ='IR'+ val
       .replace(/^[\u0622\u0627\u0628\u067E\u062A-\u062C\u0686\u062D-\u0632\u0698\u0633-\u063A\u0641\u0642\u06A9\u06AF\u0644-\u0648\u06CC]+$/, '')
       .replace(/[a-zA-Z -]/g, '')
       .replace(/[\u0660-\u0669]/g, function (c) {
        return c.charCodeAt(0) - 0x0660;
        })
        .replace(/[\u06f0-\u06f9]/g, function (c) {
          return c.charCodeAt(0) - 0x06f0;
        });
      }
    },
}
</script>

<style scoped>

</style>
