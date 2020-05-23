## 분석 정리
### 시간대별/월별/일별 자전거 이용건수와 시간대별/월별/일별의 사고건수 관계 분석
  #### 1. 시간대별 :point_right: 자전거 이용과 사고간의 시간에 대한 관계가 있음
  <img src="https://user-images.githubusercontent.com/33210124/82726646-8f7bf000-9d20-11ea-841c-7c66aa5cfc4f.png" width="70%"></img>
  <img src="https://user-images.githubusercontent.com/33210124/82726650-930f7700-9d20-11ea-865f-66fb8012be8f.png" width="50%"></img>    
  - 상관관계 분석을 진행해본 결과 상관계수는 0. 9232495576436509로 나왔으며 92% 정도의 강한 양적 상관관계를 보이는 것을 확인했다.   
    
  #### 2. 요일별 :point_right: 자전거 이용과 사고간의 요일의 관계는 없음
  <img src="https://user-images.githubusercontent.com/33210124/82726653-960a6780-9d20-11ea-87c1-114f320f8ea3.png" width="70%"></img>
  <img src="https://user-images.githubusercontent.com/33210124/82726655-97d42b00-9d20-11ea-8608-213641401c2a.png" width="50%"></img>  
  - 상관관계 분석을 진행해본 결과 상관계수는 -0.27919846696872563로 나왔으며 이는 약한 음적 선형관계를 나타낸다고 볼 수 있다
  
  #### 3. 월별 :point_right: 자전거 이용과 사고간의 월별 관계가 있음  
  <img src="https://user-images.githubusercontent.com/33210124/82726660-9a368500-9d20-11ea-8f1f-ffae7a1947c7.png" width="70%"></img>  
  <img src="https://user-images.githubusercontent.com/33210124/82726661-9b67b200-9d20-11ea-8503-4e8381a15de9.png" width="50%"></img>    
  - 상관관계 분석을 진행한 결과 상관계수는 0.8118655537977505로 나왔으며 강한 양적 선형관계를 나타낸다고 볼 수 있다.  

### 지역구별로 통근/통학 시 교통수단으로 자전거를 이용하는 현황과 지역구별 자전거 사고건수의 관계 분석  
#### :point_right: 결과적으로 지역구별로 통근, 통학 시 교통수단으로 자전거를 이용하는 지역구가 사고도 더 많이 발생했다는 관계를 도출
 <img src="https://user-images.githubusercontent.com/33210124/82726851-c999c180-9d21-11ea-851f-78a0e76ed835.png" width="100%"></img>   
 > 막대그래프 : 지역구별 자전거 사고건수  
 > 초록색 선 그래프 : 통근+통학  
 > 빨간색 선 그래프 : 통근  
 > 파란색 선 그래프 : 통학    
 
<img src="https://user-images.githubusercontent.com/33210124/82726919-344afd00-9d22-11ea-91d8-c68fef4c161d.png" width="50%"></img>    
- 사고건수와 통학, 통근을 더한 합계의 상관관계 분석을 한 결과 상관계수는 0.8115642738184344로 나왔다. 강한 양적 선형관계를 나타낸다.  

### 지역구별 자전거 전용도로와 지역구별 자전거 사고건수의 관계  
####  :point_right: 자전거 전용도로가 많이 구축되어 있는 지역구에서 자전거 사고도 많이남, 관계 없음
 <img src="https://user-images.githubusercontent.com/33210124/82726983-88ee7800-9d22-11ea-9792-8243eb57e8fa.png" width="100%"></img>   
> 막대그래프 : 자전거 전용도로(구간)   
> 빨간색 선 그래프 : 자전거 전용도로(길이)  
> 파란색 선 그래프 : 지역구별 자전거 사고건수     

<img src="https://user-images.githubusercontent.com/33210124/82727003-a885a080-9d22-11ea-88ce-2ce083d1fd7f.png" width="50%"></img> 
- 자전거 전용도로 구간과 사고건수의 상관관계 분석을 한 결과 상관계수는 0.6208705283375493로 나왔다. 뚜렷한 양적 선형관계를 나타낸다.  
<img src="https://user-images.githubusercontent.com/33210124/82727005-a9b6cd80-9d22-11ea-9d00-e809fb32f801.png" width="50%"></img>    
- 자전거 전용도로 길이와 사고건수의 상관관계 분석을 한 결과 상관계수는 0.5945696702173764로 나왔다. 뚜렷한 양적 선형관계를 나타낸다.
  
  ### 자전거 사고 심각도에 영향을 미치는 변수 분석(로지스틱 회귀분석)   
  #### :point_right: 공통적으로 도로형태가 교차로이거나 법규위반을 하거나 시간대가 오후7시~오전6시일 경우에 사고가 발생 심각도가 높아짐 (시간대별 자전거 사고와 도로형태별 자전거 사고 분석한 것에 뒷받침)
  - 가해운전자 데이터  
    <img src="https://user-images.githubusercontent.com/33210124/82727150-aec84c80-9d23-11ea-992d-c2fbf7e9e8ba.png" width="50%"></img>      
      
   > 유의수준 95%에서 종속변수인 심각도에 영향을 주는 변수는 성별, 나이, 도로형태이다. 즉 성별이 남자이거나 나이가 많거나 도로형태가 교차로일 경우 사고 심각도가 높아진다.  
가해 운전자 데이터의 양수인 편회귀계수(coef.)는 법규위반, 날씨, 시간이다. 즉 법규위반을 하거나 날씨가 맑지 않거나 오후7시~오전6시일 때 사고 심각도가 높아진다.

   <img src="https://user-images.githubusercontent.com/33210124/82727157-b38d0080-9d23-11ea-8544-70b484524c30.png" width="30%"></img>   

  > 오즈비의 경우 성별이 남자이거나 도로형태가 교차로일 경우에 사고 심각도가 높아진다.

 - 피해운전자 데이터  
    <img src="https://user-images.githubusercontent.com/33210124/82727224-2e561b80-9d24-11ea-95f9-a57ccb1587c7.png" width="50%"></img>      
      
   > 유의수준 95%에서 종속변수인 심각도에 영향을 주는 변수는 성별, 나이, 도로형태이다. 성별이 남자이거나 나이가 많거나 도로형태가 교차로일 경우 사고 심각도가 높아진다.  
피해 운전자 데이터의 양수인 편회귀계수(coef.)는 법규위반, 시간이다. 즉 법규위반을 하거나 오후7시~오전6시일 때 사고 심각도가 높아진다.


   <img src="https://user-images.githubusercontent.com/33210124/82727228-301fdf00-9d24-11ea-8b3f-4606bf009971.png" width="30%"></img>   

   > 오즈비의 경우 성별이 남자이거나 도로형태가 교차로일 경우 사고심각도가 높아진다.
