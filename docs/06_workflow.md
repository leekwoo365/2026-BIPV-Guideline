# 06. 작업 흐름 (Rhino/GH · MCP)

## 파라메트릭 설계 흐름
1. 매스/입면 표면 정의 (Rhino)
2. 입면 그리드 분할 (divide surface 로직)
3. 모듈 인스턴싱 + 방위/경사 속성 부여
4. 일사/반사 분석 (Ladybug/Honeybee)
5. 결과 기반 모듈 취사선택(발전·반사 기준)
6. 물량/리포트 산출

## MCP 연동
- **grasshopper-mcp**: GH_MCP 컴포넌트 캔버스 배치 후 재시작 필요(연결 함정 주의).
- **Swiftlet MCP(0.3.2)**: GH 정의를 도구로 노출, read-back 강점.

## 자동화 산출물
- 빛반사 PPT 자동화: python-pptx로 이미지/텍스트 교체·crop·슬라이드 복제 패턴.

## 파일 네이밍 규칙(권장)
- `simulation/YYMMDD_대상_분석유형.gh`
- `reports/YYMMDD_제목_vN.docx`

## 재현성
- GH 정의의 핵심 파라미터 값을 보고서/노트에 기록해 결과 재현 가능하게 유지.
