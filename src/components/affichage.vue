<template>
  <div class=“affichage”>
    <section>
      <div class="container col-md-12">

    <hr>
            <div class="row row-margin-bottom col-md-12">
            <div class="col-md-12 no-padding lib-item" data-category="view">
                <div class="lib-panel">
                    <div class="row box-shadow">
                        <div class="col-md-6">
                            <img class="lib-img-show" :src="someData.poster">
                        </div>
                        <div class="col-md-6">
                            <div class="lib-row lib-header">
                                {{someData.show_title}}
                                <div class="lib-header-seperator">

                                </div>
                            </div>

                            <div class="lib-row lib-desc">
                              <p>{{someData.release_year}}</p>
                                {{someData.summary}}
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-1"></div>

        </div>
</div>
    </section>

  </div>
</template>

<script>
export default {
  name: 'affichage',
  props : ['someData']

}
</script>

<!-- Add “scoped” attribute to limit CSS to this component only -->
<style scoped>
body {
    padding: 20px;
    font-family: 'Open Sans', sans-serif;
    background-color: black;
}

.lib-panel {
    margin-bottom: 20Px;
}
img{
  height :100%;
}
.lib-panel img {
  
    height :100%;
    background-color: transparent;
}

.lib-panel .row,
.lib-panel .col-md-6 {
    padding: 0;
    background-color: black;
}


.lib-panel .lib-row {
    padding: 0 20px 0 20px;
}

.lib-panel .lib-row.lib-header {
    background-color: black;
    font-size: 47px;
    padding: 10px 20px 0 20px;
    color: white;
}

.lib-panel .lib-row.lib-header .lib-header-seperator {
    height: 2px;
    width: 26px;
    background-color: #d9d9d9;
    margin: 7px 0 7px 0;
}

.lib-panel .lib-row.lib-desc {
    position: relative;
    height: 100%;
    display: block;
    font-size: 24px;
    color : white;
}
.lib-panel .lib-row.lib-desc a{
    position: absolute;
    width: 100%;
    bottom: 10px;
    left: 20px;
}

.row-margin-bottom {
    margin-bottom: 20px;
}

.box-shadow {
    -webkit-box-shadow: 0 0 10px 0 rgba(0,0,0,.10);
    box-shadow: 0 0 10px 0 rgba(0,0,0,.10);
}

.no-padding {
    padding: 0;
}

</style>
