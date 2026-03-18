
<html>
<head>
    <title>Ajith Login</title>
</head>
<body style="text-align:center; margin-top:100px; font-family:Arial;">

    <h2>Login</h2>

    <form onsubmit="return loginUser()">
        <input type="text" id="username" placeholder="Enter Email" required><br><br>
        <input type="password" id="password" placeholder="Enter Password" required><br><br>
        <button type="submit">Login</button>
    </form>

    <script>
        function loginUser() {
            var user = document.getElementById("username").value;
            var pass = document.getElementById("password").value;

            if(user === "ajithkumar06042003@gmail.com" && pass === "ajithkumar06042003@gmail.com") {
                window.location.href = "dashboard.html";
                return false;
            } else {
                alert(" Thanks ajithkumar");
                return false;
            }
        }
    </script>

</body>
</html>
<!-- dashboard.html -->
<html>
<head>
    <title>Dashboard</title>
</head>
<body style="text-align:center; margin-top:50px; font-family:Arial;">
    <h2>Welcome to Dashboard</h2>
    <p id="welcomeMessage"></p>

    <script>
        // Function to get URL parameters
        function getParameterByName(name) {
            const url = new URL(window.location.href);
            return url.searchParams.get(name);
        }

        const user = getParameterByName('user');
        document.getElementById('welcomeMessage').innerText = "Welcome, " + user;
    </script>
</body>
</html>
