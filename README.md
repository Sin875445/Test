# Test[Uploading inde
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>คุณคือแมวสายพันธุ์ไหน?</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: url('https://cdn.pixabay.com/photo/2016/11/18/16/22/cat-1838099_960_720.jpg') no-repeat center center fixed;
            background-size: cover;
            text-align: center;
            color: #333;
        }
        .container {
            width: 80%;
            margin: auto;
            padding: 20px;
            background: rgba(255, 255, 255, 0.8);
            border-radius: 10px;
        }
        .quiz {
            display: none;
            background: rgba(255, 255, 255, 0.9);
            padding: 20px;
            border-radius: 10px;
        }
        .btn {
            background-color: #ff99cc;
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            margin-top: 20px;
            border-radius: 5px;
        }
        .btn:hover {
            background-color: #ff6699;
        }
        img {
            width: 200px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container" id="intro">
        <h1>คุณคือแมวสายพันธุ์ไหน?</h1>
        <img src="https://cdn.pixabay.com/photo/2017/01/31/22/06/cat-2029270_960_720.png" alt="การ์ตูนแมว">
        <p>เลือกคำตอบที่ตรงกับตัวคุณมากที่สุด แล้วดูผลลัพธ์ว่าคุณเป็นแมวสายพันธุ์ไหน!</p>
        <button class="btn" onclick="startQuiz()">เริ่มทำแบบทดสอบ</button>
    </div>
    
    <div class="container quiz" id="quiz">
        <h2>แบบทดสอบ</h2>
        <form id="quizForm">
            <p>1. คุณชอบทำอะไรเวลาว่าง?</p>
            <input type="radio" name="q1" value="A"> A) นอนหลับชิลๆ ตื่นมากินแล้วก็นอนต่อ<br>
            <input type="radio" name="q1" value="B"> B) สำรวจสิ่งต่างๆ หาอะไรใหม่ๆเสมอ ไม่ชอบอยู่เฉยๆ<br>
            <input type="radio" name="q1" value="C"> C) ใช้เวลากับเพื่อน หรืออยู่กับคนที่รัก<br>
            <input type="radio" name="q1" value="D"> D) ใช้เวลาอยู่เงียบๆ ไม่ชอบให้ใครมายุ่ง<br>
            
            <p>2. คุณคิดว่าคุณเป็นคนแบบไหน?</p>
            <input type="radio" name="q2" value="A"> A) ขี้เกียจหน่อยๆ แต่ก็รักสบาย<br>
            <input type="radio" name="q2" value="B"> B) สายลุยสุดๆ พลังงานล้นเหลือ<br>
            <input type="radio" name="q2" value="C"> C) เข้ากับคนง่าย เป็นมิตรกับทุกคน<br>
            <input type="radio" name="q2" value="D"> D) เป็นตัวของตัวเอง มีความสุขกับโลกส่วนตัว<br>

            <p>3. อาหารแบบไหนที่คุณชอบมากที่สุด?</p>
            <input type="radio" name="q2" value="A"> A) อะไรก็ได้ที่อร่อยและกินง่าย<br>
            <input type="radio" name="q2" value="B"> B) อาหารแปลกใหม่ ชอบลองของใหม่ๆ<br>
            <input type="radio" name="q2" value="C"> C) อาหารที่ทำให้รู้สึกอบอุ่น เช่น ซุปหรือขนมปัง<br>
            <input type="radio" name="q2" value="D"> D) อาหารเรียบง่าย แต่มีสไตล์<br>
            
            <p>4. ถ้าคุณต้องเลือกสถานที่อยู่ คุณจะเลือกแบบไหน?</p>
            <input type="radio" name="q2" value="A"> A) บ้านที่อบอุ่น มีที่ให้นอนสบาย<br>
            <input type="radio" name="q2" value="B"> B) เปลี่ยนสถานที่ใหม่ๆไปเรื่อย<br>
            <input type="radio" name="q2" value="C"> C) บ้านที่มีคนเยอะๆ อบอุ่นและเป็นกันเอง<br>
            <input type="radio" name="q2" value="D"> D) เป็นตัวของตัวเอง มีความสุขกับโลกส่วนตัว<br>

            <p>5. คุณรู้สึกอย่างไรกับการพบปะผู้คนใหม่ๆ?</p>
            <input type="radio" name="q2" value="A"> A) เฉยๆ ถ้าไม่รบกวนกันก็โอเค<br>
            <input type="radio" name="q2" value="B"> B) ตื่นเต้น! ชอบเจอคนใหม่ๆ และเรียนรู้สิ่งใหม่<br>
            <input type="radio" name="q2" value="C"> C) สนุก! ชอบทำความรู้จักและสร้างมิตรภาพ<br>
            <input type="radio" name="q2" value="D"> D) ไม่ค่อยชอบเท่าไหร่ ชอบอยู่กับตัวเองมากกว่า<br>

            <button class="btn" type="button" onclick="showResult()">ดูผลลัพธ์</button>
        </form>
    </div>
    
    <div class="container quiz" id="result" style="display: none;">
        <h2>ผลลัพธ์ของคุณ</h2>
        <p id="resultText"></p>
        <button class="btn" onclick="goBack()">ลองอีกครั้ง</button>
    </div>
    
    <script>
        function startQuiz() {
            document.getElementById('intro').style.display = 'none';
            document.getElementById('quiz').style.display = 'block';
        }
        
        function showResult() {
            let answers = { A: 0, B: 0, C: 0, D: 0 };
            document.querySelectorAll('input[type=radio]:checked').forEach(input => {
                answers[input.value]++;
            });
            
            let maxType = Object.keys(answers).reduce((a, b) => answers[a] > answers[b] ? a : b);
            let descriptions = {
                A: "คุณคือแมวเปอร์เซีย! มีคุณลักษณะ ที่รักสบาย ชอบความอบอุ่นและการพักผ่อน คุณเป็นคนใจเย็น ไม่ค่อยชอบความวุ่นวาย ",
                B: "คุณคือแมวเบงกอล! มีคุณลักษณะ  มีพลังงานเยอะ ชอบผจญภัยและไม่ชอบอยู่เฉยๆ คุณเป็นคนกระตือรือร้น",
                C: "คุณคือแมวบริติชชอร์ตแฮร์! มีคุณลักษณะ ที่เป็นมิตร อบอุ่น และชอบอยู่กับคนอื่น คุณเป็นคนอ่อนโยน รักครอบครัวและเพื่อนฝูง",
                D: "คุณคือแมวสก็อตติชโฟลด์! มีคุณลักษณะ ที่รักอิสระ สุขุม และมีโลกส่วนตัว คุณอาจจะดูนิ่งๆ แต่จริงๆ แล้วอบอุ่นและมีเสน่ห์ในแบบของตัวเอง"
            };
            
            document.getElementById('quiz').style.display = 'none';
            document.getElementById('resultText').innerText = descriptions[maxType];
            document.getElementById('result').style.display = 'block';
        }
        
        function goBack() {
            document.getElementById('result').style.display = 'none';
            document.getElementById('intro').style.display = 'block';
        }
    </script>
</body>
</html>
x.html.html…]()
