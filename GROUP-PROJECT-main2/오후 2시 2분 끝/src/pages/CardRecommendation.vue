<template>
  <div class="row">
    <div class="col p-3">
      <h2>카드 추천</h2>
    </div>
  </div>
  <div class="row">
  <div class="d-flex justify-content-start">
    <div class="card" style="width: 400px">
      <img
        class="card-img-top"
        src="https://search.pstatic.net/common/?src=http%3A%2F%2Fblogfiles.naver.net%2FMjAyNDA0MzBfNDIg%2FMDAxNzE0NDUyMjE5MzE1.-UHJrviLUyXn4KBIFcJJqJLlWrTGwuOiqS_5R_oJYnAg.WjKcjRfq1Y0VGUeHbZeTNAXvhxyVWjLwzatSIeiL8p8g.PNG%2F09321_img.png&type=a340"
        alt="Card image"
        style="width: 100%"
      />
      <div class="card-body">
        <h4 class="card-title">K-패스카드</h4>
        <p class="card-text">
            <ul>
            <li>대중교통 10% 할인</li>
            <li>생활서비스 5% 할인</li>
            <li>KB Pay 이용 시 생활서비스 5% 추가할인</li>
            <br>
        </ul>
        </p>
    </div>   
    <div class="button-container">
        <a
          href="https://card.kbcard.com/CRD/DVIEW/HCAMCXPRICAC0076?cooperationcode=09321&mainCC=a"
          class="btn btn-primary "
          target="_blank"
          
          >링크 이동</a
        >
        <button @click="calculate1" class="btn btn-primary">계산</button>
      </div>
</div>
    <div class="card" style="width: 400px">
      <img
        class="card-img-bottom"
        src="https://img1.kbcard.com/ST/img/cxc/kbcard/upload/img/product/39123_img.png"
        alt="Card image"
        style="width: 100%"
      />
      <div class="card-body">
        <h4 class="card-title">My WE:SH 카드</h4>
        <p class="card-text">
        <ul>
            <li>KB Pay/음식/OTT 10~30% 할인</li>
            <li>배달/커피/영화/미용실 등 5~30% 선택 할인</li>
            <li>Happy Birth Month / 전월실적 채워드림</li>
        </ul>
        </p>
        
    </div>
    <div class="button-container">
        <a
          href="https://card.kbcard.com/CRD/DVIEW/HCAMCXPRICAC0076?mainCC=a&cooperationcode=09123&eventNum=&cateType=&cateIdx=&channelMedCate=&channelSmaCate=&pageNo=&%EC%B9%B4%EB%93%9C%EC%83%81%ED%92%88%EB%B6%84%EB%A5%98%EC%BD%94%EB%93%9C%EB%B2%88%ED%98%B8%EC%84%A0%ED%83%9D="
          class="btn btn-primary "
          target="_blank"
          
          >링크 이동</a
        >
        <button @click="calculate" class="btn btn-primary">계산</button>
      </div>
</div>

    <div class="card" style="width: 400px">
      <img
        class="card-img-top"
        src="https://newsprime.co.kr/data/photos/cdn/20190937/art_1568101611.jpg"
        alt="Card image"
        style="width: 100%"
      />
      <div class="card-body">
        <h4 class="card-title">윙크 카드</h4>
        <p class="card-text">
            학습비 자동납부 1.2/1.7만원 청구할인
        </p>
        
    </div>
    <div class="button-container-location" >
        <a
          href="https://card.kbcard.com/CRD/DVIEW/HCAMCXPRICAC0076?mainCC=a&cooperationcode=04334"
          class="btn btn-primary "
          target="_blank"
          
          >링크 이동</a
        >
      </div>
</div>
</div>
</div>
<div class="d-flex justify-content-start">
    <div class="card" style="max-width: 400px">
      <img
        class="card-img-top"
        src="https://img1.kbcard.com/ST/img/cxc/kbcard/upload/img/product/04453_img.png"
        alt="Card image"
        style="width: 100%"
      />
      <div class="card-body">
        <h4 class="card-title">골든라이프올림카드</h4>
        <p class="card-text">
         <ul>
        <li>병원or마트 5% 청구할인</li>
         <li>6대 영역 1~2% 포인트리 적립</li>
         <li>3대 영역 5~10% 청구할인</li>
        </ul>
        </p>
        
    </div>
    <div class="button-container">
        <a
          href="https://card.kbcard.com/CRD/DVIEW/HCAMCXPRICAC0076?mainCC=a&cooperationcode=04451"
          class="btn btn-primary "
          target="_blank"
          
          >링크 이동</a
        >
      </div>
</div>
    <div class="card" style="max-width: 400px">
      <img
        class="card-img-top"
        src="https://img1.kbcard.com/ST/img/cxc/kbcard/upload/img/product/04288_img.png"
        alt="Card image"
        style="width: 100%"
      />
      <div class="card-body">
        <h4 class="card-title">T-economy KB국민카드</h4>
        <p class="card-text">
            SKT 통신요금 자동납부 1만2천원/1만7천 청구할인
        </p>
        
        
    </div>
    <div class="button-container">
    <a
          href="https://card.kbcard.com/CRD/DVIEW/HCAMCXPRICAC0076?mainCC=a&cooperationcode=04288"
          class="btn btn-primary "
          target="_blank"
          
          >링크 이동</a
        >
      </div>
</div>
    <div class="card" style="max-width: 400px">
      <img
        class="card-img-top"
        src="https://img1.kbcard.com/ST/img/cxc/kbcard/upload/img/product/09116_img.png"
        alt="Card image"
        style="width: 100%"
      />
      <div class="card-body">
        <h4 class="card-title">American Express Rose Gold Card</h4>
        <p class="card-text">
            <ul>
            <li>온라인 쇼핑 10% 할인 (KB Pay)</li>
            <li>커피, 편의점 10% 할인 (KB Pay)</li>
            <li>오프라인 쇼핑, 온라인 항공/면세점 5% 할인 (KB Pay)</li>
        </ul>
        </p>
        
    </div>
    <div class="button-container">
        <a
          href="https://card.kbcard.com/CRD/DVIEW/HCAMCXPRICAC0076?mainCC=a&cooperationcode=09116"
          class="btn btn-primary "
          target="_blank"
          
          >링크 이동</a
        >
      </div>
  </div>
  </div>
</template>

<style>
.btn-primary{
    background-color: #967E76;
    color: black;
    font-weight: bold;
    border:none
}  
.button-container {
      position: absolute; /* 버튼 컨테이너는 절대적 위치 설정 */
      bottom: 20px; /* 아래쪽 여백 */
      left: 50%; /* 가운데 정렬을 위해 왼쪽 여백 설정 */
      transform: translateX(-50%); /* 가운데 정렬 */
    }
.card-body{
  padding: 50px;
}
.button-container-location{
  padding: 30px;
}

</style>

<script>
import axios from 'axios';

export default {
  methods: {
    async calculate() {
      try {
        const response = await axios.get('http://localhost:3000/expenditures');
        if (response.status === 200) {
          const expenditureData = Array.isArray(response.data) ? response.data : [];
          
          // 1. 모든 "amount" 값의 합 계산
          const totalAmount = expenditureData.reduce((acc, item) => acc + item.amount, 0);
          
          // 2. "미용" 카테고리의 합계를 고려한 값의 차 계산
          const beautyTotal = expenditureData
            .filter(item => item.category === '문화생활')
            .reduce((acc, item) => acc + item.amount, 0);
          const adjustedTotalAmount = totalAmount - (beautyTotal * 0.3);

          // 혜택 계산
          const benefit = totalAmount - adjustedTotalAmount;

          // 두 값 모두 알림창으로 표시
          alert(`적용 전: ${totalAmount.toLocaleString()}, 적용 후: ${adjustedTotalAmount.toLocaleString()}, 혜택: ${benefit.toLocaleString()}`);
        } else {
          alert('데이터 조회 실패');
        }
      } catch (error) {
        alert('에러발생 : ' + error);
      }
    },
    async calculate1() {
      try {
        const response = await axios.get('http://localhost:3000/expenditures');
        if (response.status === 200) {
          const expenditureData = Array.isArray(response.data) ? response.data : [];
          
          // 1. 모든 "amount" 값의 합 계산
          const totalAmount = expenditureData.reduce((acc, item) => acc + item.amount, 0);
          
          // 2. "미용" 카테고리의 합계를 고려한 값의 차 계산
          const beautyTotal = expenditureData
            .filter(item => item.category === '교통')
            .reduce((acc, item) => acc + item.amount, 0);
          const adjustedTotalAmount = totalAmount - (beautyTotal * 0.1);

          // 혜택 계산
          const benefit = totalAmount - adjustedTotalAmount;

          // 두 값 모두 알림창으로 표시
          alert(`적용 전: ${totalAmount.toLocaleString()}, 적용 후: ${adjustedTotalAmount.toLocaleString()}, 혜택: ${benefit.toLocaleString()}`);
        } else {
          alert('데이터 조회 실패');
        }
      } catch (error) {
        alert('에러발생 : ' + error);
      }
    }
  }
};

</script>


