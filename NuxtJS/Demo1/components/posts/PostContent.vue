<template>
    <b-col md="3">
      <!--สร้างการ์ดcontent-->
    <b-card
      :title=title
      :img-src=image
      img-alt="Image"
      img-top
      tag="article"
      style="max-width: 20rem;"
      class="mb-2"
  >
    <b-card-text>
      {{content}}
    </b-card-text>
    <nuxt-link class="btn btn-success" :to="postLink">อ่านบทความ</nuxt-link>

    <b-button href="#" variant="primary">Go somewhere</b-button>
  </b-card>
</b-col>
</template>

<script>
export default {
  props:{
    id:{
      type:String,
      required:false
    },
    title:{
      type:String,
      required:false
    },
    content:{
        type:String,
        required:false
    },
    image:{
      type:String,
      required:false
    },
    isAdmin:{ //เช็คว่าผู้ใช้
      type:Boolean,
      required:true
    }
  },
  computed:{
    postLink(){  //เลือกเส้นทางผู้ใช้
      return this.isAdmin ? '/admin/posts/'+this.id : '/posts/'+this.id
    }
  }


}
</script>