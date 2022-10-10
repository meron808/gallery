<template>
  <div class="content-card-wrapper">
    <div class="blogger-content-item">
        <div class="generic-addon-content">
            <div class="photo-info">
                <div class="photo-image">
                    <img :src=photo.url class="image" alt="">
                </div>
                <div class="photo-info-data">
                    <div class="photo-title">{{photo.title}}</div>
                    <div class="photo-id">Artikelnummer:{{photo.id}}</div>
                </div>
            </div>
            <div class="photo-link">
                <a :href="photo.url" target="_black">Zum Bild </a>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    
    props: ["photo"]

}
</script>

<style scoped>

.content-card-wrapper{
display: flex;
flex-direction: column;
align-items: flex-start;
padding: 12px;
gap: 24px;
width: 261.5px;
height: 111px;
background: #FFFFFF;
border: 1px solid rgba(0, 0, 0, 0.2);
border-radius: 4px;
box-sizing: border-box;
}

.blogger-content-item{
display: flex;
flex-direction: row;
align-items: flex-start;
padding: 0px;
gap: 27px;
width: 237.5px;
height: 87px;
position: relative;
}

.generic-addon-content{
display: flex;
flex-direction: column;
align-items: flex-start;
padding: 0px;
gap: 10px;
width: 237.5px;
height: 87px;
}

.photo-image{
display: flex;
flex-direction: column;
align-items: flex-start;
padding: 0px;
isolation: isolate;
width: 80px;
height: 60px;
}
.photo-info{
display: flex;
flex-direction: row;
align-items: center;
padding: 0px;
gap: 12px;

width: 237.5px;
height: 60px;
}

.photo-info-data{
display: flex;
flex-direction: column;
align-items: flex-start;
padding: 0px;
gap: 4px;
width: 145.5px;
height: 40px;
}

.photo-link{
flex-direction: row;
align-items: flex-start;
padding: 0px;
gap: 10px;
width: 237.5px;
height: 17px;
}
.photo-link a{
width: 152px;
height: 17px;
font-family: 'Open Sans', sans-serif;
font-style: normal;
font-weight: 600;
font-size: 14px;
line-height: 115%;
display: flex;
align-items: center;
text-decoration-line: underline;
color: #000000;
}
.image{
width: 80px;
height: 60px;
position: absolute;
left: 0%;
right: 0%;
top: 0%;
bottom: 0%;
border-radius: 8px;
}

.photo-title{
width: 145.5px;
height: 20px;
font-family: 'Open Sans', sans-serif;
font-style: normal;
font-weight: 600;
font-size: 17.778px;
line-height: 115%;
color: #000000;

/* Extra */
overflow: hidden;
white-space: nowrap;
}
.photo-id{
width: 145.5px;
height: 16px;
font-family: 'Open Sans', sans-serif;
font-style: normal;
font-weight: 400;
font-size: 14.047px;
line-height: 115%;
color: #767676;
}
</style>

