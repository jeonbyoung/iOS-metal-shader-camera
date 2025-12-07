# 🎨 iOS Metal Shader Camera: Real-time Rendering Engine

![Swift](https://img.shields.io/badge/Swift-5.0%2B-orange?style=flat&logo=swift)
![Metal](https://img.shields.io/badge/Metal-Shading_Language-red?style=flat)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow?style=flat)

> **"From C++ Logic to Metal Graphics"** > C++ 개발 경험을 바탕으로, iOS Metal(MSL)을 활용해 **실시간 렌더링 파이프라인**을 밑바닥부터 구축하는 **8주간의 프로젝트**입니다.

---

## 📌 Motivation
이 프로젝트의 목표는 상용 게임 엔진(Unity/Unreal)에 의존하지 않고, **Low-level API(Metal)** 를 직접 제어하여 고성능 카메라 필터 앱을 구현하는 것입니다.
특히 **AVFoundation**으로 Raw 데이터를 획득하고, **MSL(C++ 14 기반)** 로 쉐이더를 작성하며 GPU 가속의 원리를 깊이 있게 이해하고자 합니다.

## 🛠 Tech Stack Goals
- **Language:** Swift (App Logic), C++ / MSL (Shader Programming)
- **Frameworks:** Metal, MetalKit, AVFoundation, CoreVideo
- **Architecture:** MVVM Pattern (Planned)

---

## 📂 Repository Structure (Planned)

이 레포지토리는 기능별 모듈 단위로 폴더가 구분될 예정입니다.

```bash
📦 iOS-Metal-Shader-Camera
 ├── 📂 Shaders            # [W6-W7] .metal 쉐이더 파일 (Vertex/Fragment)
 ├── 📂 Managers           # [W2-W3] AVFoundation 카메라 세션 관리
 ├── 📂 Renderer           # [W5] Metal 파이프라인 설정 (Device, Queue)
 ├── 📂 Views              # [W1] UI 및 MTKView 설정
 └── 📜 README.md
````

-----

## 🚀 Learning Roadmap & Key Features

이 프로젝트에서 구현할 핵심 기능들입니다. 학습이 진행됨에 따라 코드가 채워질 예정입니다.

### 1\. Custom Render Pipeline

`MTKView`와 `MTLRenderPipelineDescriptor`를 사용하여 렌더링 파이프라인을 직접 구축합니다.

  - **Goal:** GPU 하드웨어 가속을 통한 60fps 렌더링
  - **Status:** `[Waiting for Week 5]`
  - **Code:** *(Coming Soon)*

### 2\. Real-time Texture Mapping

카메라의 `CVPixelBuffer` 데이터를 `MTLTexture`로 변환하여 3D 평면에 매핑합니다.

  - **Goal:** YUV 색상 공간을 RGB로 쉐이더 내부에서 변환 처리
  - **Status:** `[Waiting for Week 6]`

### 3\. Custom Fragment Shaders (MSL)

C++ 문법을 사용하는 MSL로 픽셀 단위의 시각 효과(Distortion, Glitch)를 구현합니다.

  - **Goal:** `time` 유니폼 변수와 삼각함수를 활용한 물결 효과 구현
  - **Status:** `[Waiting for Week 7]`

-----

## 📝 Weekly Progress Log

| Week | Topic | Key Activities | Status |
| :--- | :--- | :--- | :--- |
| **W1** | Swift & UI | Xcode 환경설정, Swift 문법(Optional, ARC) 적응 | ⬜️ |
| **W2** | AVFoundation | Camera Session 연결, Preview Layer 출력 | ⬜️ |
| **W3** | Data Stream | `CMSampleBuffer` 데이터 추출 및 분석 | ⬜️ |
| **W4** | CPU Processing | CoreImage 필터 적용 및 CPU 병목 현상 체감 | ⬜️ |
| **W5** | **Metal Basic** | **Hello Triangle (Render Pipeline 구축)** | ⬜️ |
| **W6** | Texture Mapping | Camera Feed → Metal Texture 변환 및 렌더링 | ⬜️ |
| **W7** | **Custom Shader** | **MSL(C++) 기반 물결/글리치 효과 구현 (Key Goal)** | ⬜️ |
| **W8** | Optimization | Instruments 메모리 누수 체크, 포트폴리오 완성 | ⬜️ |

-----

## 🔗 Study References

  - **Documentation:** [Apple Metal Documentation](https://developer.apple.com/metal/)
  - **Guide:** [Ray Wenderlich Metal Tutorial](https://www.google.com/search?q=https://www.raywenderlich.com/metal)

<!-- end list -->

```
```
