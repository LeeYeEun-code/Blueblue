<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>심리 상태 검사</title>
    <style>
        /* 본문에 사용할 폰트 (UhBee mysen Bold) */
        @font-face {
            font-family: 'UhBeeMysenBold';
            src: url('https://drive.google.com/uc?export=view&id=1F2bRgXgB07Yu8dHroCNV2MGniPSyFJZY') format('truetype'); /* UhBee mysen Bold 폰트 경로 */
        }

        /* 제목에 사용할 폰트 (EF 제주돌담체) */
        @font-face {
            font-family: 'EFJejudoldam';
            src: url('https://fastly.jsdelivr.net/gh/projectnoonnu/noonfonts_2210-EF@1.0/EF_jejudoldam.woff2') format('woff2'); /* EF 제주돌담체 폰트 경로 */
        }

        /* 기본 스타일 설정 */
        body {
            font-family: 'UhBeeMysenBold', sans-serif;
            background-image: url('https://i.postimg.cc/fbsGDc5L/IMG-2634.png');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            margin: 0;
            padding: 0;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            box-sizing: border-box;
        }

        h1 {
            font-family: 'EFJejudoldam', sans-serif;
            color: #00796b;
            font-size: 2rem;
            text-align: center;
            margin-bottom: 20px;
        }

        form {
            padding: 20px;
            border-radius: 10px;
            width: 100%;
            max-width: 400px;
            box-sizing: border-box;
            text-align: left; /* 폼 내용을 왼쪽 정렬 */
        }

        .question {
            margin-bottom: 15px;
            font-size: 1.2rem;
            display: block; /* 체크박스와 레이블을 일렬로 정렬하기 위해 block으로 설정 */
        }

        .question label {
            display: inline-block;
            margin-left: 10px;
        }

        .result {
            margin-top: 20px;
            font-weight: bold;
            color: red;
            font-size: 1.25rem;
        }

        /* 버튼 스타일 */
        button {
            background-color: #00796b;
            color: white;
            padding: 12px;
            border: none;
            border-radius: 5px;
            font-size: 1.1rem;
            cursor: pointer;
            width: 100%;
            font-family: inherit;
        }

        button:hover {
            background-color: #005f56;
        }

        input[type="checkbox"] {
            transform: scale(1.5); /* 체크박스 크기 확대 */
            vertical-align: middle;
        }

        label {
            font-size: 1rem;
        }
    </style>
</head>
<body>
    <h1>심리 상태 검사</h1>
    <form id="testForm">
        <div class="question">
            <input type="checkbox" id="q1" name="q1">
            <label for="q1">하루 중 대부분 우울, 신경질, 짜증, 공허함, 절망 등이 느껴진다.</label>
        </div>
        <div class="question">
            <input type="checkbox" id="q2" name="q2">
            <label for="q2">만사가 재미가 없고 흥미가 없다.</label>
        </div>
        <div class="question">
            <input type="checkbox" id="q3" name="q3">
            <label for="q3">식욕이 없거나 폭식한다.</label>
        </div>
        <div class="question">
            <input type="checkbox" id="q4" name="q4">
            <label for="q4">말이 느려지거나 목소리가 작아졌다.</label>
        </div>
        <div class="question">
            <input type="checkbox" id="q5" name="q5">
            <label for="q5">과거 실수나 상처가 자꾸 떠오른다.</label>
        </div>
        <div class="question">
            <input type="checkbox" id="q6" name="q6">
            <label for="q6">피곤하고 무기력하다.</label>
        </div>
        <div class="question">
            <input type="checkbox" id="q7" name="q7">
            <label for="q7">집중력이 떨어지고 결정을 내리기 어렵다.</label>
        </div>
        <div class="question">
            <input type="checkbox" id="q8" name="q8">
            <label for="q8">쉽게 짜증나고 다른 사람과의 관계가 힘들다.</label>
        </div>
        <div class="question">
            <input type="checkbox" id="q9" name="q9">
            <label for="q9">자주 머리가 아프거나 소화가 안 된다.</label>
        </div>
        <div class="question">
            <input type="checkbox" id="q10" name="q10">
            <label for="q10">죽고 싶다는 생각이 들거나 극단적인 선택을 고려한 적이 있다.</label>
        </div>
        <button type="button" onclick="showResult()">확인</button>
    </form>

    <div class="result" id="resultText"></div>

    <script>
        function showResult() {
            // 선택된 체크박스 확인
            const selectedQuestions = [];
            for (let i = 1; i <= 10; i++) {
                const checkbox = document.getElementById(`q${i}`);
                if (checkbox.checked) {
                    selectedQuestions.push(i);
                }
            }

            // 결과 설정
            let result = "당신";
            if (selectedQuestions.length >= 1) {
                result += "을 우울증이 노리고 있어요! 만화책을 처방해 드릴테니 꼭 읽고 가세요.";
            } else {
                result += "은 행복하군요! 앞으로도 행복하길 응원할게요:)";
            }

            // 결과 출력
            document.getElementById("resultText").innerText = result;
        }
    </script>
</body>
</html>
