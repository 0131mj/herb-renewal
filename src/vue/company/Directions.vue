<template>
    <div class="p-3">
        <div id="map" class="mb-3" style="width:500px;height:400px;"></div>
        <div>
            <dt>ADDRESS</dt><dd>부산광역시 금정구 중앙대로 2093, 803호</dd>
            <dt>TEL</dt><dd>051-902-1755</dd>
            <dt>FAX</dt><dd>051-517-1755</dd>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Directions',
        mounted() {
            /* eslint-disable */
            console.log('mounted start');
            var container = document.getElementById('map'); //지도를 담을 영역의 DOM 레퍼런스
            var options = { //지도를 생성할 때 필요한 기본 옵션
                center: new daum.maps.LatLng(35.271153, 129.092369), //지도의 중심좌표.
                level: 3 //지도의 레벨(확대, 축소 정도)
            };

            var map = new daum.maps.Map(container, options); //지도 생성 및 객체 리턴

            // 줌 컨트롤 추가
            var control = new daum.maps.ZoomControl();
            map.addControl(control, daum.maps.ControlPosition.TOPRIGHT);

            console.log('mounted end');
        }
    }
</script>