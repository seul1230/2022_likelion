# [ MiniProject III ] 월간 데이콘 신용카드 사용자 연체 예측 AI 경진대회

### 🦁 Project 
멋쟁이사자처럼 AI School 7th **MiniProject 3** <br/>

**🙆‍♀️🙆 Team 7ㅏ즈아** <br/>
으쌰으쌰2팀 - 이승후, 상우진, 남하윤, 김준모

**🗓️ When**<br/>
2022.11.02 - 2022.11.06

<br/>

<p align='center'>
<img src='https://github.com/seul1230/seul1230.github.io/blob/main/assets/img/img_221103/competition.png?raw=true'>
</p>


이번 미니 프로젝트로 **7ㅏ즈아** 팀은 2021년 5월에 마감한 [**월간 데이콘 신용카드 사용자 연체 예측 AI 경진대회**](https://dacon.io/competitions/official/235713/overview/description)를 주제로 모델을 만들고 높은 성능을 낼 수 있는 방법에 대해 모색하기로 하였다. 

### 🗂️ Dataset

<p align='center'>
<img src='https://github.com/seul1230/seul1230.github.io/blob/main/assets/img/img_221103/data.png?raw=true'>
</p>

* **index**
* **gender**: 성별
* **car**: 차량 소유 여부
* **reality**: 부동산 소유 여부
* **child_num**: 자녀 수
* **income_total**: 연간 소득
* **income_type**: 소득 분류 <br/>
  ```
    ['Commercial associate', 'Working', 'State servant', 'Pensioner', 'Student']
  ```

* **edu_type**: 교육 수준 <br/>
  ```
    ['Higher education' ,'Secondary / secondary special', 'Incomplete higher', 
     'Lower secondary', 'Academic degree']
  ```

* **family_type**: 결혼 여부 
  ```
    ['Married', 'Civil marriage', 'Separated', 'Single / not married', 'Widow']
  ```

* **house_type**: 생활 방식
  ```
    ['Municipal apartment', 'House / apartment', 'With parents',
     'Co-op apartment', 'Rented apartment', 'Office apartment']
  ```

* **DAYS_BIRTH**: 출생일 <br/>
    데이터 수집 당시 (0)부터 역으로 셈. <br/>
    즉, -1은 데이터 수집일 하루 전에 태어났음을 의미

* **DAYS_EMPLOYED**: 업무 시작일 <br/>
    데이터 수집 당시 (0)부터 역으로 셈. <br/>
    즉, -1은 데이터 수집일 하루 전부터 일을 시작함을 의미. <br/>
    양수 값은 고용되지 않은 상태를 의미함.

* **FLAG_MOBIL**: 핸드폰 소유 여부
* **work_phone**: 업무용 전화 소유 여부
* **phone**: 전화 소유 여부
* **email**: 이메일 소유 여부
* **occyp_type**: 직업 유형
* **family_size**: 가족 규모
* **begin_month**: 신용카드 발급 월 <br/>
    데이터 수집 당시 (0)부터 역으로 셈, 즉, -1은 데이터 수집일 한 달 전에 신용카드를 발급함을 의미

* **credit**: 사용자의 신용카드 대금 연체를 기준으로 한 신용도 <br/>
    => 낮을수록 높은 신용의 신용카드 사용자를 의미함
    
### ➡️ 시도 History와 최종 성능 비교
**History**

|Baseline|Final Score|
|:---:|:---:|
|0.872|0.7836|


```
# basline => 0.88
# 점수 : ( Public / Private )

########## RandomFroest ##########
# 1
# baseline_submission_0.983 -> 0.86583 / 0.8516
# 직업유형(occyp_type) label encoding

# 2
# baseline_submission_0.951 -> 0.86071 / 0.8465
# DAYS_EMPLOYED 양수 처리

# 3
# baseline_submission_0.923 -> 0.85454
# DAYS_BIRTH / DAYS_EMPLOYED / begin_month 통계자료 -> bins 개수 조정


############ XGBoost ############
# 4
# baseline_submission_0.856 -> 0.8738 / 0.8654
# XGBoost
# 오히려 성능이 더 떨어짐

########## CatBoost ##########
# 5
# baseline_submission_0.824  -> 0.8013 / 0.7931
# 결측치 제거
# 의미 없는 컬럼 제거 : index, FLAG_MOBIL
# FLAG_MOBIL : 전부 1로, 동일한 값을 가짐

# 6
# baseline_submission_0.819 -> 0.7978 / 0.7978
# Age 컬럼 추가

# 7
# baseline_submission_0.821
# family_size 7 이상 통일

# 8
# 성능 저하 -> # 9에서 DAYS_BIRTH 살리기
# DAYS_BIRTH, work_phone
# work_phone : credit과의 상관계수 0

# 9
# baseline_submission_0.808 -> 0.7904 / 0.7836
# work_phone 컬럼만 제외, DAYS_BIRTH 살리고
# income_mean 계산
```


