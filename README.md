
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bài tập ghép đôi – Hàm số lượng giác (Toán 11)</title>
<style>
body {
  font-family: "Segoe UI", Arial, sans-serif;
  background-color: #f9f9f9;
  color: #222;
  margin: 20px;
  line-height: 1.6;
}
h1 {
  text-align: center;
  color: #2a6cb3;
}
.container {
  max-width: 700px;
  margin: 0 auto;
  background: white;
  padding: 20px;
  border-radius: 15px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}
.question {
  margin-bottom: 18px;
}
select {
  padding: 5px;
  border-radius: 8px;
  border: 1px solid #ccc;
}
button {
  padding: 10px 20px;
  margin-top: 20px;
  border: none;
  background: #2a6cb3;
  color: white;
  border-radius: 8px;
  cursor: pointer;
}
button:hover {
  background: #1e5693;
}
.result {
  font-weight: bold;
  margin-top: 10px;
}
.correct { color: green; }
.incorrect { color: red; }
</style>
</head>
<body>
<div class="container">
  <h1>Bài tập ghép đôi – Hàm số lượng giác (Toán 11)</h1>
  <form id="quizForm">
    <div class="question">1️⃣ Hàm số y = sinx có tập giá trị là:
      <select>
        <option value="">-- Chọn đáp án --</option>
        <option value="A">[-1;1]</option>
        <option value="B">R</option>
        <option value="C">[0; +∞)</option>
      </select>
    </div>

    <div class="question">2️⃣ Hàm số y = cosx là hàm:
      <select>
        <option value="">-- Chọn đáp án --</option>
        <option value="A">Chẵn</option>
        <option value="B">Lẻ</option>
        <option value="C">Không chẵn, không lẻ</option>
      </select>
    </div>

    <div class="question">3️⃣ Hàm số y = tanx có chu kỳ là:
      <select>
        <option value="">-- Chọn đáp án --</option>
        <option value="A">π</option>
        <option value="B">2π</option>
        <option value="C">π/2</option>
      </select>
    </div>

    <div class="question">4️⃣ Hàm số y = cotx có chu kỳ là:
      <select>
        <option value="">-- Chọn đáp án --</option>
        <option value="A">π</option>
        <option value="B">2π</option>
        <option value="C">π/4</option>
      </select>
    </div>

    <div class="question">5️⃣ Đồ thị của y = sinx và y = cosx có dạng:
      <select>
        <option value="">-- Chọn đáp án --</option>
        <option value="A">Đường hình sin</option>
        <option value="B">Đường thẳng</option>
        <option value="C">Parabol</option>
      </select>
    </div>

    <div class="question">6️⃣ Giá trị lớn nhất của sinx là:
      <select>
        <option value="">-- Chọn đáp án --</option>
        <option value="A">1</option>
        <option value="B">0</option>
        <option value="C">-1</option>
      </select>
    </div>

    <div class="question">7️⃣ Công thức: sin²x + cos²x =
      <select>
        <option value="">-- Chọn đáp án --</option>
        <option value="A">1</option>
        <option value="B">0</option>
        <option value="C">2</option>
      </select>
    </div>

    <div class="question">8️⃣ Hàm số y = sinx đồng biến trên:
      <select>
        <option value="">-- Chọn đáp án --</option>
        <option value="A">(-π/2; π/2)</option>
        <option value="B">(π/2; 3π/2)</option>
        <option value="C">(0; π)</option>
      </select>
    </div>

    <div class="question">9️⃣ Hàm số y = cosx nghịch biến trên:
      <select>
        <option value="">-- Chọn đáp án --</option>
        <option value="A">(0; π)</option>
        <option value="B">(π; 2π)</option>
        <option value="C">(π/2; 3π/2)</option>
      </select>
    </div>

    <div class="question">🔟 Công thức nhân đôi: sin2x =
      <select>
        <option value="">-- Chọn đáp án --</option>
        <option value="A">2sinxcosx</option>
        <option value="B">sinx + cosx</option>
        <option value="C">cos²x − sin²x</option>
      </select>
    </div>

    <button type="button" onclick="checkAnswers()">Kiểm tra</button>
    <button type="button" onclick="resetForm()">Làm lại</button>
    <div id="result" class="result"></div>
  </form>
</div>

<script>
const correctAnswers = ["A","A","A","A","A","A","A","A","A","A"];

function checkAnswers() {
  const selects = document.querySelectorAll("select");
  let score = 0;
  selects.forEach((s, i) => {
    const selected = s.value;
    if (selected === correctAnswers[i]) {
      s.style.border = "2px solid green";
      score++;
    } else {
      s.style.border = "2px solid red";
    }
  });
  document.getElementById("result").innerHTML = 
    `✅ Bạn đúng ${score}/10 câu`;
}

function resetForm() {
  document.querySelectorAll("select").forEach(s => {
    s.value = "";
    s.style.border = "1px solid #ccc";
  });
  document.getElementById("result").innerHTML = "";
}
</script>
</body>
</html>
