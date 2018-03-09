---
title: 구글맵 API 테스트
updated: 2018-03-02 10:41
---


회사에서 디바이스 위치를 표시해주기 위해 지도 API를 사용하려고 합니다.
구글맵 아니면 다음, 네이버 이 셋 중에 쓸 것 같으니, 안써본 구글 맵을 테스트 해볼까 합니다.
구글 API 문서만 그대로 따라하면 멋진 지도를 보여줄 수 있습니다.

[Google Map JavaScript API 한글 버전](https://developers.google.com/maps/documentation/javascript/tutorial?hl=ko)

참고로 Google Maps JavaScript API는 하루 최대 25,000건의 지도 로드는 무료입니다. 그보다 많은 요청이 제공돼야하면 돈을 지불하시면 되는데, 시간과 요청수에 따라 가격이 책정됩니다.

먼저 Key 를 받아야 API를 쓸 수 있겠지요. API 문서 페이지에서 Key 받기 버튼을 쉽게 찾으실 수 있습니다.

가장 먼저 나오는 예제입니다.

{% highlight HTML %}
<!DOCTYPE html>
<html>
  <head>
    <title>Simple Map</title>
    <meta name="viewport" content="initial-scale=1.0">
    <meta charset="utf-8">
    <style>
      /* Always set the map height explicitly to define the size of the div
       * element that contains the map. */
      # map {
        height: 100%;
      }
      /* Optional: Makes the sample page fill the window. */
      html, body {
        height: 100%;
        margin: 0;
        padding: 0;
      }
    </style>
  </head>
  <body>
    <div id="map"></div>
    <script>
      function initMap() {
        const map; = new google.maps.Map(document.getElementById('map'), {
          center: {lat: 37.515040, lng: 127.108779},
          zoom: 8
        });
      }
    </script>
    <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap"
    async defer></script>
  </body>
</html>
{% endhighlight %}
<a href="{{ site.url }}/assets/html/googlemaptest.html" target="_blank">[실행화면보기]</a>
<br><br><br>

center와 zoom 는 필수 요소입니다. 빠지면 지도가 뜨지 않으니 주의하세요.
center는 지도가 나타낼 중앙 위치를 나타내는데 위도와 경도를 입력합니다.
위도와 경도는 구글 지도에서 쉽게 얻으실 수 있습니다.
![위도, 경도 얻기]({{ site.url }}/assets/images/0302-1.png)
<br><br><br>

이제 지도를 조금씩 바꿔볼겁니다. JavaScript만 수정해보겠습니다.

우선 마커가 이미 찍혀있는 지도를 그려보겠습니다. initMap 함수를 다음과 같이 고쳐줍니다.

{% highlight JavaScript %}
function initMap() {
    const jamsilStation = {lat: 37.513264, lng: 127.100130};
    const map = new google.maps.Map(document.getElementById('map'), {
        zoom: 18,
        center: jamsilStation
    });
    const marker = new google.maps.Marker({
        position: jamsilStation,
        map: map
    });
}
{% endhighlight %}<a href="{{ site.url }}/assets/html/googlemaptest.1.html" target="_blank">[실행화면보기]</a>

<br><br><br>

다음엔 여러가지 이벤트를 적용하여 보여주는 방법을 포스팅해보겠습니다~