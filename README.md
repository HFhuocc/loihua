
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Thiệp Mở Rộng 💌</title>

<style>
body {
  margin: 0;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(135deg, #ffdde1, #ee9ca7);
  font-family: Arial, sans-serif;
  overflow: hidden;
}

/* PHONG BÌ */
.envelope {
  width: 260px;
  height: 160px;
  background: #fff;
  position: relative;
  cursor: pointer;
  border-radius: 10px;
  box-shadow: 0 8px 20px rgba(0,0,0,0.2);
  overflow: hidden;
  transition: all 0.4s;
}

.flap {
  position: absolute;
  width: 0;
  height: 0;
  border-left: 130px solid transparent;
  border-right: 130px solid transparent;
  border-bottom: 80px solid #f5c6d6;
  top: 0;
  transition: transform 0.5s;
  transform-origin: top;
}

/* KHUNG THIỆP MỚI */
.card {
  display: none;
  width: 80%;
  max-width: 600px;
  background: rgba(255,255,255,0.95);
  padding: 30px;
  border-radius: 20px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.25);
  text-align: center;
  animation: pop 0.5s ease;
}

@keyframes pop {
  from { transform: scale(0.5); opacity: 0; }
  to { transform: scale(1); opacity: 1; }
}

/* TIÊU ĐỀ */
.card h2 {
  font-size: 32px;
  margin-bottom: 15px;
}

/* NỘI DUNG */
.card p {
  font-size: 20px;
  line-height: 1.8;
  white-space: pre-wrap;
}

/* TIM BAY */
.heart {
  position: absolute;
  color: red;
  animation: float 3s linear infinite;
}

@keyframes float {
  0% {transform: translateY(0) scale(1);}
  100% {transform: translateY(-300px) scale(1.5); opacity: 0;}
}

button {
  margin-top: 20px;
  padding: 10px 16px;
  border: none;
  background: #ee9ca7;
  color: white;
  border-radius: 8px;
  cursor: pointer;
  font-size: 16px;
}
</style>
</head>

<body>

<!-- PHONG BÌ -->
<div class="envelope" id="envelope" onclick="openCard()">
  <div class="flap" id="flap"></div>
</div>

<!-- KHUNG THIỆP MỚI -->
<div class="card" id="card">
  <h2>💌 Gửi Em  🩷</h2>
  <p id="content"></p>
  <button onclick="closeCard()">Đóng</button>
</div>

<script>
let message = `Anh có vài điều muốn tâm sự và gửi đến em. 
-Trong thời gian Anh và Em tìm hiểu và yêu nhau Anh cảm thấy rất hạnh phúc và rất vui vì có người luôn sẵn sàng yêu thương lo lắng cho anh vô điều kiện Anh rất vui vì điều đó 🩷
Cảm ơn Em cảm ơn vì Em đã đến quan tâm Anh lo lắng cho Anh cảm ơn sự che chở bao dung sự nhẹ nhàng của Em dành cho Anh cảm ơn Em vì tất cả
-Um thật lòng mà nói tư khi em quen anh anh đã hứa sẽ không làm em buồn hay tổn thương sẽ luôn yêu thương em, anh không phải là người như này người như kia, nhưng anh đã làm sai anh đã trở thành như vậy!!! điều đó thật đáng trách tại sao anh lại trẻ con như vậy tại sao anh lại làm như vậy với em...
-Va em đã nhiều lân muốn buông bỏ anh NHƯNG em đã không làm vậy em chọn tha lỗi cho anh và bao dung cho anh trao thêm cho anh 1 cơ hội để anh sửa chữa sai lầm của anh nhưng... anh lại phạm sai lầm này tới sai lầm khác vào ngày hôm đó anh tưởng chừng mọi chuyện sẽ kết thúc... và anh sẽ không còn được nói chuyện, được em yêu thương nữa anh rât sợ rất sợ nó sẽ xẩy ra vi chính lúc đấy anh thật sự hối lỗi thật sự muốn thay đổi bản thân để tốt hơn với em tưởng chừng anh đã hết cơ hội Nhưng em em đã buông bỏ mọi chuyện nhắm mắt cho qua và lại 1 cơ hội nữa cho anh cảm ơn em, anh rất hối hận về những việc mà anh gây ra 
- Anh biết sự lo lắng của em không phải ở tuổi bây giờ mà về mai sau chúng ta sẽ là gì anh đã thấy thất vọng về bản thân do anh chưa trưởng nên có đòi hỏi em những thứ không nên có um và từ bây giờ thay vào những thứ đó anh và em 2 chúng ta sẽ cùng nhau đi chơi đi ăn những món chưa từng ăn những nơi chưa từng chơi, đến anh sẽ bù đấp lại những ngày qua có lẽ bây giờ anh mới nghĩ và nhận ra thì đã trể rồi nhưng anh hy vọng mình vẫn còn có thể sửa được và mang lại nụ cười trên đôi môi em 🩷
-Tuy anh biết em rất buồn rất thất vọng về anh và dần mất đi sự tin tửng hướng về anh anh đã cảm nhận được những điều đó nhưng không sao em à người ta thường nói 1 lần bị lừa dối cả đời sống trong nghi ngờ mà nên không sao chỉ vì hiện tại anh chưa đủ vững vàng chư đủ tốt để em có thể tin tưởng mà dựa vào vai anh thêm 1 lần nữa anh biết điều đó nên anh sẽ cố gắng cố gắng làm cho bản thân trở nên trưởng thành hơn để em tin tưởng và dựa vào vai anh thêm 1 lần nữa 🩷
-Và em hãy nhớ
"Cuộc đời có khó khăn rất nhiều thử thách nếu 1 ngày em gặp phải chuyện không vui, không vừa ý thì hãy nói với anh anh vẫn ở đây nghe những lời em nói 🩷 VÀ YÊU THƯƠNG EM NHƯ LỜI ANH ĐÃ NÓI"
-Um hẹn em 2 năm khi đôi ta 20 ta sẽ hẹn hò ở biển nhé anh sẽ cầu hôn em ở đó Yêu Em 🩷`;

// GIỚI HẠN 1000 CHỮ
if (message.length > 1000) {
  message = message.substring(0, 1000) + "...";
}

function openCard() {
  document.getElementById("flap").style.transform = "rotateX(180deg)";

  setTimeout(() => {
    document.getElementById("envelope").style.display = "none";
    document.getElementById("card").style.display = "block";
    typeText();
    createHearts();
  }, 500);
}

function closeCard() {
  document.getElementById("card").style.display = "none";
  document.getElementById("envelope").style.display = "block";
  document.getElementById("content").innerHTML = "";
}

function typeText() {
  let i = 0;
  let target = document.getElementById("content");

  function typing() {
    if (i < message.length) {
      target.innerHTML += message.charAt(i);
      i++;
      setTimeout(typing, 20);
    }
  }
  typing();
}

function createHearts() {
  for (let i = 0; i < 15; i++) {
    let heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "💖";
    heart.style.left = Math.random() * 100 + "%";
    heart.style.top = "60%";
    heart.style.fontSize = (20 + Math.random()*25) + "px";
    document.body.appendChild(heart);

    setTimeout(() => heart.remove(), 3000);
  }
}
</script>

</body>
</html>
