# Nu-result
#<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>National University Result</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body{font-family:Arial;background:#eef2f6;margin:0}
.header{background:#fff;padding:10px;border-bottom:2px solid #0a8}
.header h2{margin:0}
.box{background:#fff;margin:15px;padding:15px;border-radius:6px}
input,select,button{
  width:100%;padding:10px;margin:8px 0;font-size:15px
}
button{background:#0a8;color:#fff;border:none}
img{width:100%;margin-top:15px;display:none;border:1px solid #ccc}
.footer{text-align:center;font-size:13px;color:#666;padding:10px}
</style>
</head>

<body>

<div class="header">
  <h2>National University, Bangladesh</h2>
  <p>Bachelor Degree (Honours) 1st Year Examination – 2024</p>
</div>

<div class="box">
  <h3>Result Search</h3>

  <input id="roll" placeholder="Exam Roll No">
  <input id="reg" placeholder="Registration No">

  <select id="year">
    <option value="">Select Exam Year</option>
    <option value="2024">2024</option>
  </select>

  <button onclick="searchResult()">Search Result</button>

  <img id="resultImg">
</div>

<div class="footer">
  © National University, Bangladesh
</div>

<script>
function searchResult(){
  let r=roll.value;
  let g=reg.value;
  let y=year.value;

  if(!r||!g||!y){
    alert("All fields required");
    return;
  }

  let imgPath="images/"+r+"_"+g+"_"+y+".jpg";
  let img=document.getElementById("resultImg");

  img.src=imgPath;
  img.style.display="block";

  img.onerror=function(){
    alert("Result Not Found");
    img.style.display="none";
  }
}
</script>

</body>
</html>
