<template lang="pug">
- const demoSingleVideo = {'title':'【超洗腦！】茄子蛋：愛情你比我想的閣較偉大 | 1小時無縫循環 |《當男人戀愛時》主題曲','thumbnailSrc': 'https://i.ytimg.com/vi/h6hFbYyHtyM/mqdefault.jpg','duration':'1:00:59','views': '104 萬次','date': '一個月','author': {'name':'GLoop 無縫循環','thumbnailSrc':'https://yt3.ggpht.com/qcFnM-Xosyikfr6muOrdckipsIWWXd-p570XEXuZwndf4zDZAadtrpvJGrBCYd5IeAT9sfNx=s88-c-k-c0x00ffffff-no-rj'}};

mixin oneVideo(videoData)
  .video
        .thumbnail
          img(src=videoData.thumbnailSrc alt='')
          span.duration #{videoData.duration}
        .details
          .author
            img(src=videoData.author.thumbnailSrc alt='')
          .text
            h3 #{videoData.title}
            span
              a(href='#') GLoop 無縫循環
              | &nbsp;• 觀看次數：#{videoData.view} • #{videoData.date}前
.mainBody
  .videos
    .videosGrid
      - let itemsNumber = 20;
      while itemsNumber > 0
        +oneVideo(demoSingleVideo)
        - itemsNumber--;
</template>
