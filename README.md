# 외교부 레포트 자동화 프로그램

> **외교부 월별 세출 집행 현황 데이터를 수집·가공하여 보고서를 생성하고 메일로 전송하는 자동화 프로그램입니다.**

<br>

## 기술 환경

- UiPath Studio
- Robotic Enterprise Framework (REFramework)
- Excel, Web Automation
- HTML Email, DataTable, Dictionary 등 활용

<br>

## 자동화 흐름 요약

1. 템플릿을 복사하여 각 월에 대응하는 Excel 시트를 생성 (2024년 07월 ~ 2025년 03월)
2. 외교부 홈페이지에서 월별 세출 집행 현황 데이터를 수집
3. 검색어와 0원이 아닌 항목을 필터로 추출하여 메일 본문용 테이블로 구성
4. 0원이 아닌 항목만 집계하여 각 월 시트에 저장
5. 집계 기준에 대한 총합 금액 계산
6. 전체 기간에 대한 총합 계산
7. 월별 데이터를 기준으로 집행액 추이 선 그래프 생성
8. 월별 데이터 정리 및 메일 본문 구성
9. 메일 본문 작성 후 첨부 파일과 함께 전송

<br>

## Workflow 구성

- **Initialization** <br>
  00\_Output Folder 초기화.xaml <br>
  01\_초기 DT 생성.xaml <br>
  02\_결과 파일 저장.xaml <br>
  03\_결과 파일 초기 설정.xaml <br>

- **Process Transaction** <br>
  04\_세출 집행 현황 DT 추출.xaml <br>
  05\_세출 집행 현황 DT 가공.xaml <br>
  06\_세출 집행 현황 DT 저장.xaml <br>

- **End Process** <br>
  07\_집행액 총 집계.xaml <br>
  08\_총합 DT 저장.xaml <br>
  09\_Excel 보고서 스타일.xaml <br>
  10\_메일 발송.xaml <br>
