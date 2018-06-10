<template>
  <div class="home-page">
    <section class="intro">
      <h1>Get lastesr tech news!</h1>
    </section>
    <section class="featured-posts">
      <nuxt-link to="/posts/1" class="post-preview">
        <article>
          <div class="post-thumbnail"></div>
          <div class="post-content">
            <h1>post title 1</h1>
            <p>preview text 1</p>
          </div>
        </article>
      </nuxt-link>

      <nuxt-link to="/posts/2" class="post-preview">
        <article>
          <div class="post-thumbnail"></div>
          <div class="post-content">
            <h1>post title 2</h1>
            <p>preview text 2</p>
          </div>
        </article>
      </nuxt-link>
    </section>
  </div>
</template>

<script>


export default {
 
}
</script>

<style scoped>
  .intro {
    height: 300px;
    position: relative;
    padding: 30px;
    /* 
    box-sizing: border-box
    padding & board 的寬高不影響外層所設的寬高，而會影響content的寬高
    box-sizing: content-box
    padding & board 的寬高會影響到外層所設的寬高，（content width + padding + board）
    */
    box-sizing: border-box;
    background-position: center;
    background-size: cover;
  }

  .intro h1 {
    position: absolute;
    top: 10%;
    left: 5%;
    width: 90%;
    font-size: 1.5rem;
    color: black;
    background-color: rgb(211, 211, 211);
    padding: 10px;
    border-radius: 10px;
    box-shadow: 3px 3px 3px black;
    box-sizing: border-box;
    border: 1px solid black;
  }

  /* 裝置寬大於768的時候才載入的css */
  @media (min-width: 768px) {
    .intro h1 {
      font-size: 2rem;
    }
  }

  .featured-posts {
    display: flex;
    padding: 20px;
    box-sizing: border-box;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
  }

  .post-preview {
    border: 1px solid #ccc;
    box-shadow: 0 2px 2px #ccc;
    background-color: white;
    width: 90%;
  }

  a {
    /* 移除link底線 */
    text-decoration: none;
    color: black;
  }

  @media (min-width: 850px) {
    .post-preview {
      width: 400px;
      margin: 10px;
    }
  }

  .post-thumbnail {
    background-image: url(https://i.kinja-img.com/gawker-media/image/upload/s--vv79lYUc--/c_scale,f_auto,fl_progressive,q_80,w_800/v9rciwgxfbozbezevrpp.jpg);
    width: 100%;
    height: 200px;
    background-position: center;
    /* 將大圖以不重複填滿至容器中 */
    background-size: cover; 
  }

  .post-content {
    padding: 10px;
    text-align: center;
  }
  a:hover .post-content,
  a:active .post-content {
    background-color: #ccc;
  }
</style>
