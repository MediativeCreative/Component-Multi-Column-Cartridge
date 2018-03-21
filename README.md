## Component Multi-Column Cartridge

**See the preview component [here](https://mediativecreative.github.io/Component-Multi-Column-Cartridge/)**

### Code to edit

This code is a starting base to make multi column design.
To make it easily responsive we use the `display: Flex` method so all the columns automatically adjust their height to be equal
This can be break down in 4 different styles:


**- Youtube video + Content**

To make a Youtube video component just copy and place this code:

**HTML**
```html
<section class="md_container">
  <div class="md_videoWrapper">
    <div class="md_videoCopy">Suspendisse accumsan, sem sit amet suscipit finibus</div>
    <div class="md_videoPlayer">
      <div class="md_vidContainer">
        <iframe width="100%" height="315" src="https://www.youtube.com/embed/MWczaVUiAhY?rel=0&modestbranding=1&autohide=1&showinfo=0&cc_load_policy=0" frameborder="0" allowfullscreen></iframe>
      </div>
    </div>
  </div>
</section>
```
**CSS**
```css
.md_container{
  width: 100%;
  position: relative;
}
.md_videoWrapper{
  display: -webkit-box;
  display: -moz-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-flex-flow: row;
  -moz-flex-flow: row;
  -ms-flex-flow: row;
  -o-flex-flow: row;
  margin-bottom: 10px;
  align-items: center;
  background-color: #f6f6f6;
}
.md_videoCopy{
  position: relative;
  background-color: #f6f6f6;
  color: #1267a4;
  font-size: 25px;
  flex: 2 1 0;
  -webkit-flex: 2 1 0;
  -moz-flex: 2 1 0;
  -ms-flex: 2 1 0;
  -o-flex: 2 1 0;  
  text-align: center;
  padding: 0 60px 0 60px;
  line-height: 30px;
  font-weight: bold;
}
.md_vidContainer{
  position: relative;
  width: 100%;
  height: 0;
  padding-bottom: 56.1%;
}
.md_vidContainer iframe{
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
}
.md_videoPlayer{
  position: relative;
  flex: 3 1 0;
  -webkit-flex: 3 1 0;
  -moz-flex: 3 1 0;
  -ms-flex: 3 1 0;
  -o-flex: 3 1 0;
}
@media screen and (max-width : 1000px){
  .md_videoWrapper {
    -webkit-flex-flow: column;
    -moz-flex-flow: column;
    -ms-flex-flow: column;
    -o-flex-flow: column;
    order: 1;
  } 
  .md_videoCopy{
    padding: 30px 60px 30px 60px !important;
    order: 2;
  }
}
```  
      
**- Multi columns (single or multi rows)**

To make a Multi column design just copy and place this code:

**HTML**
```html
<section class="md_container">
  <div class="md_contentBlockWrapper">
    <div class="md_contentBlock">
      <img class="md_contentImg" src="http://i.walmartimages.ca/img/mediative/Batiste/batiste-shampoo-hero-img.jpg" alt="DON'T FOGET THE COPY" title="DON'T FOGET THE COPY">
      <div class="md_contentTitle">Aliquam vel ullamcorper enim</div>
      <div class="md_contentCopy">Aenean mollis interdum aliquam. Fusce elementum est sit amet tellus luctus interdum. Nullam at egestas sapien. Proin posuere augue in magna fermentum, sed dignissim ligula dapibus. Phasellus laoreet, elit ut facilisis cursus, velit justo vestibulum ipsum, non euismod eros ante eu tellus.</div>
    </div>
    <div class="md_contentBlock">
      <img class="md_contentImg" src="http://i.walmartimages.ca/img/mediative/Batiste/batiste-shampoo-hero-img.jpg" alt="DON'T FOGET THE COPY" title="DON'T FOGET THE COPY">
      <div class="md_contentTitle">Aliquam vel ullamcorper enim</div>
      <div class="md_contentCopy">Aenean mollis interdum aliquam. Fusce elementum est sit amet tellus luctus interdum. Nullam at egestas sapien. Proin posuere augue in magna fermentum, sed dignissim ligula dapibus. Phasellus laoreet, elit ut facilisis cursus, velit justo vestibulum ipsum, non euismod eros ante eu tellus.</div>
    </div>
    <div class="md_contentBlock">
      <img class="md_contentImg" src="http://i.walmartimages.ca/img/mediative/Batiste/batiste-shampoo-hero-img.jpg" alt="DON'T FOGET THE COPY" title="DON'T FOGET THE COPY">
      <div class="md_contentTitle">Aliquam vel ullamcorper enim</div>
      <div class="md_contentCopy">Aenean mollis interdum aliquam. Fusce elementum est sit amet tellus luctus interdum. Nullam at egestas sapien. Proin posuere augue in magna fermentum, sed dignissim ligula dapibus. Phasellus laoreet, elit ut facilisis cursus, velit justo vestibulum ipsum, non euismod eros ante eu tellus.</div>
    </div>
  </div>
</section>
```
**CSS**
```css
.md_container{
  width: 100%;
  position: relative;
}
.md_contentBlockWrapper{
  position: relative;
  display: -webkit-box;
  display: -moz-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-flex-flow: wrap;
  -moz-flex-flow: wrap;
  -ms-flex-flow: wrap;
  -o-flex-flow: wrap;
  margin-top: 12px;
  justify-content: space-between;
}
.md_contentBlockWrapper :nth-child(3n){
  margin-right:0;
}
.md_contentBlock{
  width: calc((100% / 3) - 1%);
  position: relative;
  background-color: #f6f6f6;
  margin-bottom: 10px;
  margin-right: 1%;
}
.md_contentImg{
  width: 100%;
  height: auto;
}
@media screen and (max-width : 1000px){
  .md_contentBlockWrapper{
    -webkit-flex-flow: column;
    -moz-flex-flow: column;
    -ms-flex-flow: column;
    -o-flex-flow: column;
  }
  .md_contentBlockWrapper :nth-child(1n){
    margin-right:0;
  }
  .md_contentBlock{
    width: 100%;
    margin-right: 0;
  }
}
```
**- Image + Content**

To make a full width image and content design just copy and place this code:

**HTML**

```html
<section class="md_container">
  <div class="md_contentFullWidthWrapper">
    <div class="md_contentFullWidthImg"></div>
    <div class="md_contentFullWidthCopy">
      <div class="md_contentTitle">Aliquam vel ullamcorper enim</div>
      <div class="md_contentCopy">Aenean mollis interdum aliquam. Fusce elementum est sit amet tellus luctus interdum. Nullam at egestas sapien. Proin posuere augue in magna fermentum, sed dignissim ligula dapibus. Phasellus laoreet, elit ut facilisis cursus, velit justo vestibulum ipsum, non euismod eros ante eu tellus. Aenean mollis interdum aliquam. Fusce elementum est sit amet tellus luctus interdum. Nullam at egestas sapien. Proin posuere augue in magna fermentum, sed dignissim ligula dapibus. Phasellus laoreet, elit ut facilisis cursus, velit justo vestibulum ipsum, non euismod eros ante eu tellus. Aenean mollis interdum aliquam. Fusce elementum est sit amet tellus luctus interdum. Nullam at egestas sapien. Proin posuere augue in magna fermentum, sed dignissim ligula dapibus. Phasellus laoreet, elit ut facilisis cursus, velit justo vestibulum ipsum, non euismod eros ante eu tellus.</div>
    </div>
  </div>
</section>
```

**CSS**

```css
.md_container{
  width: 100%;
  position: relative;
}
.md_contentFullWidthWrapper{
  position: relative;
  display: -webkit-flex;
  display: -moz-flex;
  display: -ms-flexbox;
  display: -o-flex;
  display: flex;
  -webkit-flex-flow: row;
  -moz-flex-flow: row;
  -ms-flex-flow: row;
  -o-flex-flow: row;
  margin-top: 10px;
  margin-bottom: 10px;
  background-color: #f6f6f6;
}
.md_contentFullWidthImg{
  flex: 2 1 0;
  -webkit-flex: 2 1 0;
  -moz-flex: 2 1 0;
  -ms-flex: 2 1 0;
  -o-flex: 2 1 0;
  width: 100%;
  min-height: 200px;
  background-repeat: no-repeat;
  background-position: top center;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  -ms-background-size: cover;
  background-size: cover;  
  background-image: url("http://i.walmartimages.ca/img/mediative/Batiste/batiste-shampoo-hero-img.jpg");
}
.md_contentFullWidthCopy{
  flex: 2 1 0;
  -webkit-flex: 2 1 0;
  -moz-flex: 2 1 0;
  -ms-flex: 2 1 0;
  -o-flex: 2 1 0;
  padding: 10px 0;
}
.md_contentTitle{
  color: #1267a4;
  font-size: 20px;
  font-weight: 800;
  padding-top: 8px;
  padding-bottom: 8px;
  padding: 15px 30px 10px 30px;
}
.md_contentCopy{
  position: relative;
  font-size: 14px;
  line-height: 19px;
  color: #333;
  font-weight: 200;
  padding: 0px 30px 30px 30px;
}
@media screen and (max-width : 1000px){
  .md_contentFullWidthWrapper{
    -webkit-flex-flow: column;
    -moz-flex-flow: column;
    -ms-flex-flow: column;
    -o-flex-flow: column;
  }
  .md_contentFullWidthImg{
    height: 0;
    padding-bottom: 56%;
  }
}
```
