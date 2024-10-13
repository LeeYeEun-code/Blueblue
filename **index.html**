<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>심리 상태 검사</title>
	 <!-- 두 개의 폰트 파일 불러오기 -->
    <style>
        /* 첫 번째 파일: 본문에 사용할 폰트 (UhBee mysen Bold) */
        @font-face {
            font-family: 'UhBeeMysenBold';
            src: url('https://drive.google.com/uc?export=view&id=1F2bRgXgB07Yu8dHroCNV2MGniPSyFJZY') format('truetype'); /* 변환된 Google Drive 링크 */
        }

        /* 두 번째 파일: 제주돌담체 (WOFF2 형식 사용) */
        @font-face {
            font-family: 'EF_jejudoldam';
            src: url('https://fastly.jsdelivr.net/gh/projectnoonnu/noonfonts_2210-EF@1.0/EF_jejudoldam.woff2') format('woff2');
            font-weight: normal;
            font-style: normal;
        }

        /* 기본 스타일 설정 */
        body {
            font-family: 'UhBeeMysenBold', sans-serif;
            background-image: url('https://i.postimg.cc/fbsGDc5L/IMG-2634.png');
            background-size: cover;
            background-repeat: no-repeat;
            background-position: center;
            margin: 0;
            padding: 20px;
            font-size: 16px; /* 핸드폰에 맞는 기본 폰트 크기 */
        }

        h1 {
            font-family: 'EF_jejudoldam', sans-serif;
            color: #00796b;
            font-size: 24px; /* 제목을 핸드폰에 맞게 조정 */
            text-align: center;
        }

        .question {
            margin-bottom: 15px;
            font-size: 18px; /* 질문 크기를 핸드폰에 맞게 조정 */
        }

        .result {
            margin-top: 20px;
            font-weight: bold;
            color: red;
            font-size: 20px;
        }

        /* 버튼 스타일 */
        button {
            background-color: #00796b;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            font-size: 18px;
            cursor: pointer;
        }

        button:hover {
            background-color: #005f56;
        }

        form {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        input[type="checkbox"] {
            transform: scale(1.5); /* 체크박스를 크게 해서 모바일에서 쉽게 체크 가능 */
        }

        label {
            margin-left: 10px;
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
        <button type="button" onclick="showResult()">확인</button>
    </form>

    <div class="result" id="resultText"></div>

    <script>
        function showResult() {
            const q1 = document.getElementById("q1").checked;
            const q2 = document.getElementById("q2").checked;

            let result = "당신의 심리 상태는 ";
            if (q1 || q2) {
                result += "우울증이 의심됩니다. 전문가와 상담을 권장합니다.";
            } else {
                result += "양호합니다.";
            }

            document.getElementById("resultText").innerText = result;
        }
    </script>
</body>
</html>
