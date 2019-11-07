   <template>
  <div class="maindiv">
    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="6" class="bg1"></b-col>
        <b-col sm="6" class="bg2">
          <p class="para">Made by with Love By [Name]</p>
        </b-col>
      </b-row>
    </b-container>

    <!-- <p>footer blog below writting code</p> -->

    <b-container class="cart-bg">
      <b-row>
        <b-col sm="6" offset="4" class="potato-banner">
          <b-nav>
            <b-nav-item>
              <img src="../assets/mashedPotato.jpg" width="150" height="90" />
            </b-nav-item>
            <b-nav-item>
              <b-button variant="success" @click="likefnc+=1">Like</b-button>
            </b-nav-item>
            <b-nav-item disabled>
              <span class="text">likes: {{likefnc}}</span>
            </b-nav-item>
          </b-nav>
        </b-col>
      </b-row>

      <!-- <p>This is second dish blog</p> -->

      <b-row>
        <b-col sm="6" offset="4" class="potato-banner">
          <b-nav>
            <b-nav-item>
              <img src="../assets\bakedPotato.jpeg" width="150" height="90" />
            </b-nav-item>
            <b-nav-item>
              <b-button @click="dislikefun+=1" variant="danger">Dislike</b-button>
            </b-nav-item>
            <b-nav-item disabled>
              <span class="text">Dislikes:{{dislikefun}}</span>
            </b-nav-item>
          </b-nav>
        </b-col>
      </b-row>

      <!-- <P>This  below blog is reset blog </P> -->

      <b-row>
        <b-col sm="6" offset="5" class="potato-banner1">
          <b-nav>
            <b-nav-item>
              <b-button @click="reset" variant="warning">Reset</b-button>
            </b-nav-item>
            <b-nav-item disabled>
              <span class="text">TotalClickes : {{likefnc + dislikefun}}</span>
            </b-nav-item>
          </b-nav>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      likefnc: 0,
      dislikefun: 0
    };
  },
  methods: {
    // likefnc(){
    //    this.like +=1;
    // },
    // dislikefun(){
    //     this.dislike +=1;
    // },
    reset() {
      (this.likefnc = 0), (this.dislikefun = 0);
    }
  }
};
</script>

<style  scoped>
.maindiv {
  width: 90%;
  /* border: 1px solid red; */
  margin: 0 auto;
  /* display: flex; */
}

.bg2 {
  background-image: url("../assets/thumbs.png");
  height: 40vh;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}
.bg1 {
  background-image: url("../assets/potatoimg.png");
  height: 40vh;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.cart-bg {
  background-image: url("../assets/blackimg.png");
  height: auto;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}


.para {
  position: absolute;
  top: 100px; 
  left: 60px;
  font-size: 30px;
}
.smallimg1 {
  display: flex;
}
.smallimg2 {
  display: flex;
}
.potato-banner {
  padding: 20px;
}
.text {
  font-size: 30px;
  color: white;
}
</style>
