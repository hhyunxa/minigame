# TODOS

## v2 리깅을 demo.html로 합치기

**What:** `finger-sports-day-v2.html`의 리깅 개선(`classifyRig`, `runPoseRel`, `boneFields`, `CharMesh.updateSwing`, `limbFatness`, 리깅 검사 도구)을 `finger-sports-day-demo.html`로 옮겨 두 파일을 하나로 만든다.

**Why:** 두 파일이 갈라져 있다. demo에는 수영·줄다리기·지휘·1:1이 있고, v2에는 두꺼운 그림의 찌그러짐을 25% → 5% 수준으로 줄인 리깅이 있다(`docs/RIGGING-PIPELINE.md` 5장).

**Pros:** 어떤 그림이든 덜 찌그러지고, 본 개발 출발점이 하나로 정리된다.

**Cons:** 수영·줄다리기·지휘의 자세 함수가 v2의 상대 회전 방식과 맞는지 확인되지 않았다. 종목마다 회귀 확인이 필요하다(사람: ~2일 / CC: ~1-2시간).

**Context:** 2026-10-14 eng review R1에서 회의 데모는 demo.html 그대로 가기로 했고, 이 병합은 회의 뒤로 미뤘다. 시작점: v2의 `runPose` → `runPoseStick`/`runPoseRel` 분기와 `boneFields(ex, mode)`. demo의 `swimPose`, 줄다리기·지휘 자세 함수가 `model`의 어떤 필드를 쓰는지부터 확인한다.

**Depends on / blocked by:** 팀 회의에서 "리깅 품질 목표"(회의 안건 5번) 결정.
