# 🏭 RPA 기반 제조기업 사무자동화 시스템

> 경남 소재 제조기업(㈜신스윈)의 주문·재고 관리 프로세스를 자동화하기 위해 개발한 RPA (Robotic Process Automation) 소프트웨어 프로젝트입니다.  
> 반복적인 Excel 작업을 자동화하고 인적 오류를 최소화하여 생산성 향상에 기여했습니다.

---

##  프로젝트 개요

본 프로젝트는 경남 소재 제조기업 ㈜신스윈의 반복적이고 수작업 중심인 주문·재고 관리 업무를 자동화하기 위해 RPA(Robotic Process Automation) 소프트웨어를 개발한 사례입니다.  
주요 목표는 기존 공정을 크게 변경하지 않고, 반복적이고 오류 가능성이 높은 Excel 기반 업무를 자동화하여 업무 효율을 높이고, 인적 오류를 최소화하는 것입니다.  
프로젝트는 크게 두 가지 모듈로 구성됩니다. 첫 번째, 외부 시스템에서 주문 및 단가 데이터를 받아 지정 경로에 저장하는 **Data Provider** 모듈, 두 번째, 저장된 데이터를 읽어 생산량을 계산하고 최종 Excel 산출물을 생성하는 **Automatic Excel Calculator(AEC)** 모듈입니다.  
이를 통해 주문서 표준화, 재고 반영 자동화, Excel 기반 생산량 계산 프로세스 자동화 등 핵심 업무를 시스템화하며, 실제 산업 환경에서 RPA 자동화의 적용 가능성을 검증하였습니다.

### 배경
- 기존 주문·재고 관리 과정이 **수작업(Excel)** 으로 이루어져 있어  
  - 인적 오류 발생 가능성이 높음  
  - 인력 교체 시 유지보수 난이도 증가  
- 이를 해결하기 위해 **RPA 소프트웨어**를 활용한 자동화 시스템 개발

### 목표
- **주문서 표준화** 및 **재고 반영 자동화**
- Excel 기반의 생산량 계산 프로세스 자동화
- 유지보수 부담 감소 및 데이터 신뢰성 향상

---
### RPA 소프트웨어 도식화
<img width="354" height="266" alt="image" src="https://github.com/user-attachments/assets/a38e42e7-b60c-4402-9ecd-75e668933c68" />

○ 전체적인 공정과정의 수정없이 단순 반복된 업무나 필요한 부분을 자동화를 위해. 본 프로젝트를 통해 RPA 소프트웨어를 활용하여 수동으로 관리되었던 주문 발주 및 생산공정에서 재고를 반영한 생산량 계산을 위한 Excel화일의 자동화 프로세스를 구축하고자 함.


○ 이를 통해 인력의 변경에 따른 유지보수의 어려움, 수동 입력으로 인한 인적 오류의 가능성을 최소화 하며, 실제 산업 전반에서의 RPA 자동화 시스템의 적용 가능성을 확인할 수 있음.

### RPA 소프트웨어의 프로세스
<img width="353" height="346" alt="image" src="https://github.com/user-attachments/assets/79a19dd3-e218-47ea-886b-5be7eb5b44b2" />

○ RPA 소프트웨어는 개발모델에 따라 Data Provider, Automatic Excel Calculator로 구성되며, External File System, Window Scheduler와 연동됨.


○ Data Provider는 외부시스템으로부터 제시된 입력 파일을 Window의 File System 내의 특정 경로에 저장하여 Receving과 Price 파일 각각으로 저장하게 됨.
### Automatic Excel Calculator 도식화
<img width="523" height="363" alt="image" src="https://github.com/user-attachments/assets/17a1c6f3-0ae9-4d54-a18a-9fab8b73f62e" />

○ Data Provideer에서 생상한 입력 파일을 받아 엑셀 파일을 계산하여 중간산출물을 만든 후 이를 이용해 결과 파일을 생성해 특정 경로에 저장함.

##  기술 스택

| 구분 | 사용 기술 |
|------|-----------|
| 언어 | Python |
| 데이터 처리 | pandas, openpyxl |
| 자동화 | Windows Task Scheduler |
| 버전 관리 | Git / GitHub |

---

##  주요 기능

- **Data Provider**
  - 외부 시스템에서 입력 파일(주문·단가 파일)을 자동으로 지정 경로에 저장
- **Automatic Excel Calculator (AEC)**
  - 입력 데이터를 읽어 중간 계산 → 최종 산출물 생성
  - 회사 재고 데이터 + 주문 데이터를 통합하여 생산량 계산
- **출력 자동화**
  - 요구사항에 맞춘 Excel 양식으로 결과 파일 생성
  - 생산라인에 전달할 수 있는 형태로 자동 저장

---


