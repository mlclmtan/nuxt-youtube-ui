<template lang="pug">
- const buttons = [{'icon':'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAyCAYAAAAeP4ixAAAABmJLR0QA/wD/AP+gvaeTAAACGElEQVRoge3YvWsTcRzH8VfboKIiSBVEUZAO4ihKRRBRFwU3l4KjlP4H0qGji/9CBxcROunkoqgglSoO2kVHURGfEEEUfKg0Dvc7kzRpe0nucpd4bzgIyffh87nf7765O0oSsQ/3cTd87ktO4gOq4fiMM7kqapMhzOCPyMCtcFTDdzMhptBsww2R6GVcwbBI+LRGc9tz0rguB/FCbRudbRFzCh9DzGsc6Zm6hFzAd5HAp9i/RuxePA6xP3Cx7rfqKkfmVETbJ254DZsT5G3EbF3eLDbIycgeLKid2ckOakyG3CoeaRaeuZETeB+avMHRLmodwkutVyAzI0O4hKXQ4DZGU6g7GmrFwqdDr0yMrBytlzGSYv2RUHM59LgpAyMH8DwU/YrzaRZfwTl8kcHFPoFvoeAixtIqvAZjoVdsZKKbYvFojZf6OrZ0KbAdNuGq5hHdFjtxLxRYEl18eTGFX0HLPHYnTTyOdyHxLY5loa5NDuOVSNMnnF4vYQq/Q8ID7MpSXZvswB2Nu6TpLnor5jROikrvNCamolHjnEj7P56ojdae3ah1SKwv1rpA9KxAtJ0WMZ6LtM4YxzP8XC2gX1akgeEWgX1JaaRoDIyRNP8rOh0QqbwaKldkDZKe4VRH/MCsSGmkaJRGikZppGiURopGaaRolEaKRmmkaAyMkVYPQUV+p1VPg/ZWK/KwR0K6YT5vASX/DX8BtYScJ8Q7pSIAAAAASUVORK5CYII=','id':'home','text':'Home'},{'icon':'https://img.icons8.com/ios/50/000000/gas.png','id':'trending','text':'Trending'},{'icon':'https://img.icons8.com/ios/50/000000/youtube-play.png','id':'subscriptions','text':'Subscriptions'},{'icon':'https://img.icons8.com/ios/50/000000/video-gallery.png','id':'library','text':'Library'}];

mixin oneButton(buttonData,isActive)
  button.footer(class=isActive)
    img(id=buttonData.id src=buttonData.icon)
    span #{buttonData.text}
.footers
  each button,index in buttons
    if index==0
      +oneButton(button,'active')
    else
      +oneButton(button)
</template>
