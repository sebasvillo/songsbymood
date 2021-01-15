<template>
  <v-main background-color= "blue">
    <v-app-bar :clipped-left="clipped" fixed app elevate-on-scroll dense :color="app_color" shrink-on-scroll  fade-img-on-scroll scroll-target="#scrolling-techniques-3" max-height="100"
    >
          <template>
            <v-tabs align-with-title>
                <v-tab link to="/">
                  <v-img 
                    align="center"
                    src="https://i.imgur.com/4VRqgcI.png"
                    max-height="60"
                    max-width="150"
                    contain
                  ></v-img>
                </v-tab>
                <v-tab link to="/aboutUs">
                  <v-img 
                    align="center"
                    src="https://i.imgur.com/ohFYiFI.png"
                    max-height="45"
                    max-width="150"
                    contain
                  ></v-img>
                </v-tab>
            </v-tabs>
          </template>
      </v-app-bar>
    <v-card
      class="mx-auto"
      max-width="1300"
    >
      <v-img
        class="white--text align-end"
        height="200px"
        src="https://i.pinimg.com/originals/32/37/cc/3237ccb3ce40c41da3ba8d50c7925434.jpg"
      >
        <v-card-title 
        color = "blue">
        </v-card-title>
        <v-row v-if="app_color === 'yellow'" align="center" justify="center">
          <v-col cols=12 md=3 offset>
            <v-img align="center" src="https://pbs.twimg.com/media/C5J-eTrUoAEPMKQ.jpg"></v-img>
          </v-col>
          <v-col cols=12 md=3 align="center" offset>
            <v-img align="center" src="https://www.exberliner.com/downloads/21142/download/grafik.png?cb=d091188d3105d335a81cd84046d90333&w=640"></v-img>
          </v-col>
          <v-col cols=12 md=3 align="center" offset>
            <v-img align="center" src="https://static1.squarespace.com/static/59413d96e6f2e1c6837c7ecd/t/5c211b7e032be4789674aad8/1545673314588/Van+Gogh+Yellow.jpg?format=1500w"></v-img>
          </v-col>
          <v-col cols=12 md=2 align="center" offset>
            <v-img align="center" src="https://www.republica.com/cine-publico/wp-content/uploads/sites/21/2015/04/big_fish.jpg"></v-img>
          </v-col>
        </v-row>
          <v-row v-if="app_color === 'green'" align="center" justify="center">
            <v-col cols=12 md=3 offset>
              <v-img align="center" src="https://collectionapi.metmuseum.org/api/collection/v1/iiif/438008/preview"></v-img>
            </v-col>
            <v-col cols=12 md=3 align="center" offset>
              <v-img align="center" src="https://excusesandhalftruths.files.wordpress.com/2011/11/newimage17.png?w=600&h=337"></v-img>
            </v-col>
            <v-col cols=12 md=3 align="center" offset>
              <v-img align="center" src="https://cdn.vox-cdn.com/thumbor/jwZoNesfYb3tlNxBk5hkd60GvfQ=/0x0:1920x1040/1200x675/filters:focal(804x408:1110x714)/cdn.vox-cdn.com/uploads/chorus_image/image/62330190/neighbor_totoro_disneyscreencaps.com_4017.0.jpg"></v-img>
            </v-col>
            <v-col cols=12 md=3 align="center" offset>
              <v-img align="center" src="https://2.bp.blogspot.com/-Fd4bx1zojwM/UAVbZ4kiX3I/AAAAAAAAAIs/VTFci6Ep1Js/s1600/copy.jpg"></v-img>
            </v-col>
          </v-row>
          <v-row v-if="app_color === 'blue'" align="center" justify="center">
            <v-col cols=12 md=3 offset>
              <v-img align="center" src="https://media.overstockart.com/optimized/cache/data/product_images/VG485-1000x1000.jpg"></v-img>
            </v-col>
            <v-col cols=12 md=3 align="center" offset>
              <v-img align="center" src="https://cdn.hobbyconsolas.com/sites/navi.axelspringer.es/public/media/image/2017/01/moonlight.png"></v-img>
            </v-col>
            <v-col cols=12 md=3 align="center" offset>
              <v-img align="center" src="https://www.slashfilm.com/wp/wp-content/images/The-Royal-Tenenbaums.jpg"></v-img>
            </v-col>
            <v-col cols=12 md=3 align="center" offset>
              <v-img align="center" src="https://images2.minutemediacdn.com/image/upload/c_crop,h_842,w_1500,x_0,y_0/f_auto,q_auto,w_1100/v1554998529/shape/mentalfloss/rosemary_hed.jpg"></v-img>
            </v-col>
          </v-row>
          <v-row v-if="app_color === 'red'" align="center" justify="center">
            <v-col cols=12 md=3 offset>
              <v-img align="center" src="https://i.pinimg.com/originals/be/2c/1e/be2c1ea050e03ea6097ea859cf40f9d5.jpg"></v-img>
            </v-col>
            <v-col cols=12 md=3 align="center" offset>
              <v-img align="center" src="https://static01.nyt.com/images/2017/11/30/movies/darkest-anatomy1/darkest-anatomy1-videoSixteenByNine1050.png"></v-img>
            </v-col>
            <v-col cols=12 md=3 align="center" offset>
              <v-img align="center" src="https://goddessofhellfire.files.wordpress.com/2014/09/suspiria-technicolor.jpg"></v-img>
            </v-col>
            <v-col cols=12 md=3 align="center" offset>
              <v-img align="center" src="https://static1.abc.es/media/cultura/2020/09/05/pollock-k4ZD--620x349@abc.jpg"></v-img>
            </v-col>
          </v-row>
      </v-img>

      <v-card-subtitle class="pb-0">  
      </v-card-subtitle>

        <v-slider
          v-model="status"
          :tick-labels="ticksLabels"
          :max="3"
          step="1"
          ticks="always"
          value
          tick-size="1"
          @click="change_color"
          >
        </v-slider>
      </v-card-actions>
      <v-card-actions>
        <v-col align="center">
          <v-btn
            class="mx-2"
            fab
            dark
            color="red"
            @click="activate_section"
            @click.stop="request_random_song"
            @click.exact="activate_like"
          >
            <v-icon dark>
              mdi-play
            </v-icon>
          </v-btn>
        </v-col>
      </v-card-actions>
      <v-col align="center" v-if="section">
        <v-card-text class="text--primary">
          {{titulo}}
        </v-card-text>
        <v-card-text class="text--secondary">
          {{autor}}
        </v-card-text>
        <iframe width="560" height="315" :src="link" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen ></iframe>
        <v-row
            align="center"
            justify="center"
            v-if="like"
          >
            <v-btn
              tile
              color="green"
              @click="change_votacion('L')"
              @click.stop="hide_like"
            >
              <v-icon left>
                mdi-thumb-up
              </v-icon>
            </v-btn>
            <v-btn
              tile
              color="red"
              @click="change_votacion('D')"
              @click.stop="hide_like"
            >
              <v-icon left>
                mdi-thumb-down
              </v-icon>
            </v-btn>
          </v-row>
      </v-col>
    </v-card>
  </v-main>
</template>


<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'
import axios from 'axios'


export default {
  components: {
    Logo,
    VuetifyLogo,

  },
  data () {
      return {
        fruits: 'Alegría',
        ticksLabels: [
          'Alegría',
          'Calma',
          'Tristeza',
          'Ira',
        ],
        status:null,
        titulo: "",
        autor: "",
        link: "",
        haycancion: false,
        section: false,
        app_color: "white",
        votacion: "",
        like: true
      }
    },
    methods:{
      
      request_random_song(){
        let datos={
          estado: this.status
        }
        axios.post('http://localhost:5000/start', datos)
        .then(response => { 
          if(response.data){
            this.titulo=response.data.prueba[0]
            this.autor=response.data.prueba[1]
            this.link=response.data.prueba[2]
          }
        })
        .catch(response => {
            console.log(response)
        })  
      },
      activate_section: function(){
        let section=this.section
        if(!section){
          this.section=true
        }
      },
      activate_like: function(){
        let like=this.like
        if(!like){
          this.like=true
        }
      },
      hide_like: function(){
        let like=this.like
        if(like){
          this.like=false
        }
      },
      change_color(){
        let emocion=this.status
        if (emocion===0){
          this.app_color="yellow"
          }
        else if (emocion===1){
          this.app_color="green"
          }
        else if (emocion===2){
          this.app_color="blue"
          }
        else if (emocion===3){
          this.app_color="red"
          }
        },
        change_votacion(gusto){
        if (gusto==='L'){
          this.votacion="L"
          }
        else if (gusto==='D'){
          this.votacion="D"
          }
        let datos={
          tit: this.titulo,
          gus: this.votacion
        }
        axios.post('http://localhost:5000/votacion', datos)
        .then(response => { 
        })
        .catch(response => {
          console.log(response)
        }) 
        },
    }
}
</script>
