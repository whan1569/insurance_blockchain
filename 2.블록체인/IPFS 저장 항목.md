## ✅ **IPFS 저장 자료 정리표 (정형화 및 네이밍 컨벤션)**

| 분류    | 항목              | 해시 키 네이밍 예시                                                                             | 복수 여부 | 설명             |
| ----- | --------------- | --------------------------------------------------------------------------------------- | ----- | -------------- |
| 📸 사진 | 차량 파손 사진        | `photo_damage_01`, `photo_damage_02`                                                    | ✅     | 파손 부위별로 복수 저장  |
|       | 사고 현장 전경        | `photo_scene_01`, `photo_scene_02`                                                      | ✅     | 주변 전체를 보여주는 장면 |
|       | 번호판 식별 사진       | `photo_plate_01`, `photo_plate_02`                                                      | ✅     | 가해/피해 차량 식별용   |
| 🎥 영상 | 블랙박스 전방 영상      | `video_dashcam_front`                                                                   | ❌     | 차량 블랙박스 전방 영상  |
|       | 블랙박스 후방 영상      | `video_dashcam_rear`                                                                    | ❌     | 차량 블랙박스 후방 영상  |
|       | 목격자/탑승자 촬영 영상   | `video_witness_01`, `video_witness_02`                                                  | ✅     | 제3자 직접 촬영 영상   |
|       | CCTV 영상         | `video_cctv_01`, `video_cctv_02`                                                        | ✅     | 외부 고정 카메라 영상   |
| 📄 문서 | 사고 사실확인원 (경찰)   | `doc_police_report`                                                                     | ❌     | 경찰의 공식 사고 확인서  |
|       | 보험 접수 확인서       | `doc_insurance_report`                                                                  | ❌     | 보험사 발행 접수 증빙   |
|       | 진단서             | `doc_medical_01`, `doc_medical_02`                                                      | ✅     | 병원 진단서 복수 가능   |
|       | 보험 청구서          | `doc_claim_01`, `doc_claim_02`                                                          | ✅     | 청구 항목별 구분 가능   |
|       | 당사자 진술서         | `doc_statement_claimant`, `doc_statement_respondent_01`, `doc_statement_third_party_01` | ✅     | 역할 기반 구분       |
|       | 합의서             | `doc_agreement_01`, `doc_agreement_02`                                                  | ✅     | 민사 합의서 등       |
|       | 교통사고 조사보고서 (경찰) | `doc_police_analysis`                                                                   | ❌     | 경찰의 분석 요약 문서   |
|       | 보험 조사보고서 (손해사정) | `doc_insurance_analysis`                                                                | ❌     | 손해사정인의 최종 평가서  |

---

## 🧩 규칙 요약

* `photo_`, `video_`, `doc_` 으로 **자료 유형**을 명확히 구분
* **복수 가능 항목**은 `_01`, `_02` 등 **순번 붙이기**
* **당사자 자료**는 역할 기반 키 사용 (`claimant`, `respondent`, `third_party_<순번>`)
* **단일 문서**는 고정 키 사용 (중복 방지, 예: `doc_police_report`)

