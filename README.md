from flask import Flask, render_template_string

app = Flask(__name__)

html_page = """
<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Free Telegram Reward</title>

<style>
body{
font-family: Arial;
background:#fff3e6;
text-align:center;
padding:30px;
}

.box{
background:white;
padding:25px;
border-radius:15px;
box-shadow:0 0 15px rgba(0,0,0,0.1);
max-width:400px;
margin:auto;
}

h1{
color:#ff6a00;
}

.reward{
font-size:38px;
font-weight:bold;
margin:20px;
color:#000;
}

.btn{
display:block;
background:#ff6a00;
color:white;
padding:15px;
border-radius:30px;
text-decoration:none;
font-size:18px;
margin-top:15px;
}

.btn:hover{
background:#ff4d00;
}

.small{
font-size:12px;
margin-top:20px;
color:#555;
}
</style>
</head>

<body>

<div class="box">
<h1>Limited Giveaway</h1>
<p>Join our Telegram channel and participate in giveaways</p>

<div class="reward">₹1 - ₹2</div>

<a class="btn" href="https://t.me/+6zo1SukLRFs5MDhl">Join Telegram & Claim</a>

<p class="small">
Rewards are distributed randomly during channel events.
</p>

</div>

</body>
</html>
"""

@app.route("/")
def home():
    return render_template_string(html_page)

if __name__ == "__main__":
    app.run(debug=True)
