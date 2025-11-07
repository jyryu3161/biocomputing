# 🧩 **Pixi 기초 정리 **

---

## 🧠 1️⃣ Pixi란?

**Pixi**는
👉 “Python과 과학 계산용 프로그램을 **쉽고 빠르게 설치하고 관리할 수 있는 도구**”입니다.

* Python 프로그램을 위한 **패키지 관리자**이자 **환경 관리자**입니다.
* `conda`보다 빠르고, `pip`보다 쉬우며, **초보자도 명령어 몇 줄이면 환경 세팅 완료!**

---

## 💡 2️⃣ 왜 Pixi를 쓰나요?

| 기존 문제               | Pixi로 해결                    |
| ------------------- | --------------------------- |
| 패키지 설치가 어렵다         | `pixi add` 한 줄로 해결          |
| 프로젝트마다 버전이 다르다      | 각 프로젝트마다 독립된 환경 생성          |
| 다른 사람과 환경을 공유하기 어렵다 | `pixi.toml` 파일 하나로 공유       |
| 재현 불가능한 환경 문제       | `pixi.lock`으로 완벽히 동일한 환경 재현 |

---

## ⚙️ 3️⃣ Pixi 설치하기

리눅스나 macOS에서 아래 명령어 한 줄이면 설치됩니다:

```bash
curl -fsSL https://pixi.sh/install.sh | bash
```

설치 확인:

```bash
pixi --version
```

---

## 📁 4️⃣ 새 프로젝트 만들기

```bash
pixi init myproject
cd myproject
```

이렇게 하면 폴더 안에 `pixi.toml`이라는 파일이 만들어집니다.
이 파일은 **“이 프로젝트에서 쓸 프로그램 목록”**을 저장하는 설정 파일입니다.

---

## 📦 5️⃣ 패키지 설치하기

예를 들어 Python과 Numpy를 설치하려면:

```bash
pixi add python numpy
```

Pixi가 자동으로 환경을 만들고 필요한 패키지를 설치합니다.

---

## 🧮 6️⃣ 파이썬 실행해보기

설치가 끝나면 아래 명령으로 Python 실행 가능:

```bash
pixi run python
```

또는 파일을 실행하려면:

```bash
pixi run python hello.py
```

---

## ✏️ 7️⃣ 간단한 예제 (Hello Pixi!)

1️⃣ 프로젝트 만들기

```bash
pixi init hello_pixi
cd hello_pixi
```

2️⃣ Python 설치

```bash
pixi add python
```

3️⃣ 코드 작성

```bash
nano hello.py
```

내용:

```python
print("Hello, Pixi!")
```

4️⃣ 실행

```bash
pixi run python hello.py
```

출력:

```
Hello, Pixi!
```

---

## 🔢 8️⃣ Numpy 예제

```bash
pixi add numpy
```

`calc.py` 파일 작성:

```python
import numpy as np
numbers = np.array([1, 2, 3, 4, 5])
print("평균:", np.mean(numbers))
```

실행:

```bash
pixi run python calc.py
```

결과:

```
평균: 3.0
```

---

## 💻 9️⃣ Pixi 환경 진입 (가상환경 들어가기)

Pixi는 자동으로 가상환경을 관리합니다.
하지만 직접 환경에 들어가서 명령을 실행할 수도 있습니다:

```bash
pixi shell
```

→ 프롬프트 앞에 `(pixi)` 표시가 생기면 Pixi 환경 안입니다.
→ 나오려면 `exit` 입력.

---

## 📘 🔟 Pixi 환경 설정 파일 예시 (`pixi.toml`)

```toml
[project]
name = "hello_pixi"
version = "0.1.0"

[dependencies]
python = ">=3.10"
numpy = "*"

[tasks]
hello = "python hello.py"
```

명령 실행:

```bash
pixi run hello
```

---

## 🧭 11️⃣ Pixi 주요 명령 요약

| 명령어                       | 설명          |
| ------------------------- | ----------- |
| `pixi init myproject`     | 새 프로젝트 생성   |
| `pixi add numpy`          | 패키지 설치      |
| `pixi remove numpy`       | 패키지 삭제      |
| `pixi run python file.py` | 프로그램 실행     |
| `pixi shell`              | Pixi 환경 진입  |
| `pixi update`             | 모든 패키지 업데이트 |
| `pixi task add`           | 실행 태스크 등록   |

---

## 🧩 12️⃣ JupyterLab 설치 및 실행

이제 **Jupyter Lab (주피터 랩)** 을 Pixi 환경에 설치해보겠습니다.
Jupyter Lab은 웹 브라우저에서 Python 코드를 바로 실행하고 시각화할 수 있는 툴입니다.
(데이터 분석, 인공지능 실습에 매우 많이 사용됩니다!)

---

### ✅ 1단계. 설치

```bash
pixi add jupyterlab
```

### ✅ 2단계. 실행

```bash
pixi run jupyter-lab
```

➡ 실행하면 아래와 같은 메시지가 뜹니다:

```
To access the server, open this file in a browser:
    http://localhost:8888/lab?token=xxxxxxxxxx
```

👉 위 주소를 **Ctrl + 클릭** 하면 웹 브라우저가 열리며,
Jupyter Lab 인터페이스가 실행됩니다.

---

### ✅ 3단계. 새 노트북 만들기

1. 왼쪽 상단의 **“+”** 버튼 클릭
2. “Python 3” 노트북 선택
3. 아래처럼 코드 입력 후 `Shift + Enter` 로 실행:

```python
print("Hello, Jupyter Lab!")
```

결과:

```
Hello, Jupyter Lab!
```

---

### ✅ 4단계. 유용한 추가 패키지 설치 (선택)

```bash
pixi add matplotlib pandas
```

그리고 주피터에서 아래 코드 실행:

```python
import pandas as pd
import matplotlib.pyplot as plt

data = pd.DataFrame({"x": [1,2,3,4], "y": [2,3,5,7]})
plt.plot(data["x"], data["y"], marker='o')
plt.title("Simple Line Plot")
plt.show()
```

→ 간단한 그래프가 출력됩니다 🎨

---

## 📚 13️⃣ JupyterLab까지 포함한 전체 명령 정리

| 단계 | 명령어                                | 설명                        |
| -- | ---------------------------------- | ------------------------- |
| 1  | `pixi init myproject`              | 새 프로젝트 만들기                |
| 2  | `pixi add python numpy jupyterlab` | Python, Numpy, Jupyter 설치 |
| 3  | `pixi run python test.py`          | Python 코드 실행              |
| 4  | `pixi run jupyter-lab`             | JupyterLab 실행             |
| 5  | `pixi shell`                       | 환경 안으로 진입                 |
| 6  | `exit`                             | 환경 종료                     |

---

## 🎯 14️⃣ 정리 요약

✅ Pixi는 초보자도 **한 줄 명령으로 Python 환경을 구성**할 수 있게 도와줍니다.
✅ `pixi.toml` 파일 하나로 언제든 **같은 환경을 재현**할 수 있습니다.
✅ `pixi run jupyter-lab` 명령으로 **Jupyter 환경까지 바로 사용 가능**합니다.
✅ 설치, 실행, 공유—all-in-one. Pixi는 Python 학습의 가장 쉬운 출발점입니다 🚀

---

원하신다면 이 내용을

* 📘 **PDF 버전 (수업/교재용)**
* 💻 **실습용 예제 폴더 (`hello_pixi`, `jupyter_demo`) 포함 ZIP 파일**
  로 만들어드릴 수 있습니다.

어떤 형식으로 드릴까요?
예: `"PDF로 만들어줘"` / `"PDF + 예제 코드 함께"`
