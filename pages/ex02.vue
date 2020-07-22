<template>
  <div>
    <h1>HELLO {{ first }}age:{{std}} </h1>
    <input type="text" :value="dep" color--text="red">
     <v-text-field
     v-model="first"
     label="์NAME"
            outlined
            shaped
          ></v-text-field>
    
    <v-text-field
            solo
            label="Name"
            append-icon="mdi-map-marker"
            clearable
          ></v-text-field>

          <v-text-field
            v-model="last"
            label="Last Name"
            solo-inverted
          ></v-text-field>

          <v-text-field
            v-model="title"
            :rules="rules"
            counter="20"
            hint="This field uses counter prop"
            label="Regular"
            clearable
          ></v-text-field>

  </div>
</template>
<script>
export default {
  data:function(){
    return{
    name:"alongkorn",
    age:45,
    // dep:"information  technology",
    first:"chaiyaphum"
    }
  }
}
</script>