# 🧨 Minesweeper AI Arena

> **"지뢰찾기의 한계에 도전하세요. 인간의 직관과 AI의 논리가 충돌하는 전장입니다."**
> **"Push the boundaries of Minesweeper. Where human intuition meets AI logic."**

---

<details open>
<summary><strong>🇰🇷 한국어 (Korean)</strong></summary>

## 🚀 주요 기능 (Key Features)

### 🏆 1. 분리된 리더보드 (Categorized Leaderboard)
공정한 경쟁을 위해 플레이 방식에 따라 랭킹을 3가지 카테고리로 엄격히 분류합니다.
- **PHYSICAL**: 어떤 도움도 없이 오직 인간의 판단과 반응속도로 기록한 순수 실력 랭킹.
- **HINT**: AI의 안전 확률 도움을 받아 전략적으로 플레이한 기록.
- **SOLVER**: 내장 솔버 혹은 직접 개발한 외부 봇을 이용한 알고리즘 성능 랭킹.
  - *동적 봇 탐지 시스템이 탑재되어, 기계적인 클릭 리듬이 감지되면 자동으로 SOLVER 랭킹으로 분류됩니다.*

### 🎥 2. 리플레이 재생 기능 (Game Replay System)
리더보드의 각 기록 옆에 있는 **재생(▶️) 버튼**을 클릭해 보세요!
- 상위권 랭커들이 어떤 순서로 지뢰를 찾아가는지, AI가 어떤 논리로 복잡한 구간을 돌파하는지 똑같은 속도로 복기할 수 있습니다.
![Start/Stop Solver Demo](./source/start-stop-solver.gif)

### 💡 3. 실시간 AI 힌트 (Live Hint & Probability)
마우스 오버만으로 현재 칸이 얼마나 안전한지 실시간으로 계산합니다.
- 단순한 확률을 넘어, **모순 검증(Contradiction Check)** 알고리즘을 통해 논리적으로 확정된 100% 안전한 칸을 찾아내어 당신의 생존율을 높여줍니다.
![Hint System Demo](./source/hint.gif)

### 🤖 4. 강력한 내장 솔버 (Built-in Autonomous Solver)
프로젝트에 탑재된 기본 AI 솔버의 성능을 확인해 보세요.
- 부분집합 분석(Subset Analysis)과 가설 검증(Lookahead) 기술을 사용하여 인간이 해결하기 어려운 고난도 배치를 초고속으로 풀어냅니다.

### 🔌 5. 외장 솔버 경쟁 (Open for External Bots)
자신만의 지뢰찾기 솔버를 개발 중이신가요?
- 본 서비스의 DOM 구조는 자동화 봇이 읽기 매우 쉽게 설계되어 있습니다. 여러분의 봇이 얼마나 빨리 Expert 난이도를 클리어하는지 랭킹에 등록하여 증명해 보세요!

---

## 🛠️ 기술 스택 (Tech Stack)

- **Frontend**: Vite + Vanilla JS (최적의 성능과 가벼운 로딩)
- **Backend**: Firebase Firestore (실시간 전역 랭킹 및 리플레이 로그 저장)
- **Security**: 클릭 간격의 표준 편차 및 `isTrusted` 속성을 분석하는 **Anti-Cheat 봇 탐지 알고리즘**.
- **Visuals**: `canvas-confetti`를 이용한 화려한 축하 효과 및 `flag-icons` 라이브러리를 통한 선명한 국기 표시.

## 🎮 조작 방법 (Controls)

- **Space**: 게임 재시작 (눌렀다 뗄 때 리셋되며, 꾹 누르면 스마일 아이콘이 반응합니다.)
- **좌클릭**: 칸 열기
- **우클릭**: 깃발 꽂기
- **숫자 클릭 (Chording)**: 주변 지뢰를 모두 찾은 상태에서 클릭 시 나머지 칸을 일괄 오픈합니다.

## 🚀 배포 및 설정 (Setup)

Vercel 배포 시 아래의 환경 변수(Environment Variables) 설정이 필요합니다:
- `VITE_FIREBASE_API_KEY`
- `VITE_FIREBASE_AUTH_DOMAIN`
- `VITE_FIREBASE_PROJECT_ID`
- `VITE_FIREBASE_STORAGE_BUCKET`
- `VITE_FIREBASE_MESSAGING_SENDER_ID`
- `VITE_FIREBASE_APP_ID`
- `VITE_FIREBASE_MEASUREMENT_ID`

</details>

---

<details>
<summary><strong>🇺🇸 영어 (English)</strong></summary>

## 🚀 Key Features

### 🏆 1. Category-based Leaderboard
Rankings are strictly classified into three categories to ensure fair competition:
- **PHYSICAL**: Pure skill rankings achieved solely by human judgment and reaction time.
- **HINT**: Strategic play records assisted by real-time safety probabilities.
- **SOLVER**: Performance rankings for algorithms, including the built-in solver and custom external bots.
  - *Equipped with a dynamic bot detection system that auto-classifies mechanical clicking rhythms into the SOLVER category.*

### 🎥 2. Game Replay System
Click the **Replay (▶️) button** next to any record on the leaderboard!
- Review how top rankers navigate the minefield and analyze the logic AI uses to clear complex sections at the original play speed.
![Start/Stop Solver Demo](./source/start-stop-solver.gif)

### 💡 3. Live AI Hint (Safety Probability)
Calculate the safety probability of each cell in real-time simply by hovering.
- Beyond simple odds, our **Contradiction Check** algorithm identifies 100% safe cells logically, significantly increasing your survival rate.
![Hint System Demo](./source/hint.gif)

### 🤖 4. Powerful Built-in Solver
Experience the power of our native AI solver.
- It utilizes **Subset Analysis** and **Lookahead (Contradiction Check)** techniques to solve high-difficulty patterns that are nearly impossible for humans to decipher at high speed.

### 🔌 5. Open for External Bots
Are you developing your own Minesweeper solver?
- The DOM structure of this app is designed to be easily readable by automation bots. Register your bot's record and prove how fast it can clear the Expert difficulty!

---

## 🛠️ Tech Stack

- **Frontend**: Vite + Vanilla JS (Optimized performance and lightning-fast load times)
- **Backend**: Firebase Firestore (Real-time global leaderboard and replay log storage)
- **Security**: **Anti-Cheat Bot Detection** analyzing standard deviation of click intervals and `isTrusted` attributes.
- **Visuals**: Vibrant victory effects via `canvas-confetti` and crisp SVG flag icons via `flag-icons`.

## 🎮 Controls

- **Space**: Restart Game (Triggered on release; the smiley reacts while held down.)
- **Left Click**: Reveal Cell
- **Right Click**: Toggle Flag
- **Number Click (Chording)**: Quickly reveal surrounding cells when the correct number of flags are placed.

## 🚀 Setup & Deployment

When deploying to Vercel, ensure the following Environment Variables are configured:
- `VITE_FIREBASE_API_KEY`
- `VITE_FIREBASE_AUTH_DOMAIN`
- `VITE_FIREBASE_PROJECT_ID`
- `VITE_FIREBASE_STORAGE_BUCKET`
- `VITE_FIREBASE_MESSAGING_SENDER_ID`
- `VITE_FIREBASE_APP_ID`
- `VITE_FIREBASE_MEASUREMENT_ID`

</details>
