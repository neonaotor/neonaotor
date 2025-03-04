from flask import Flask, render_template_string, request, redirect, url_for, session

app = Flask(__name__)
app.secret_key = "supersecretkey"

# Simulierter Benutzer-Datenbank (ersetzbar mit echter DB)
users = {"admin": "password123"}

# HTML-Templates als Strings
login_page = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login</title>
</head>
<body>
    <h2>Login</h2>
    {% if error %} <p style="color:red;">{{ error }}</p> {% endif %}
    <form method="POST">
        <input type="text" name="username" placeholder="Benutzername" required>
        <input type="password" name="password" placeholder="Passwort" required>
        <button type="submit">Login</button>
    </form>
    <h3>Registrierung</h3>
    <form method="POST" action="{{ url_for('register') }}">
        <input type="text" name="username" placeholder="Benutzername" required>
        <input type="password" name="password" placeholder="Passwort" required>
        <button type="submit">Registrieren</button>
    </form>
</body>
</html>
"""

dashboard_page = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dashboard</title>
</head>
<body>
    <h2>Willkommen, {{ user }}!</h2>
    <ul>
        <li><a href="{{ url_for('dashboard') }}">Dashboard</a></li>
        <li><a href="{{ url_for('pins') }}">Pins</a></li>
        <li><a href="{{ url_for('results') }}">Results</a></li>
        <li><a href="{{ url_for('strings') }}">Strings</a></li>
        <li><a href="{{ url_for('downloads') }}">Downloads</a></li>
        <li><a href="{{ url_for('logout') }}">Logout</a></li>
    </ul>
    <h3>PC-Checker</h3>
    <button onclick="alert('PC Check gestartet!')">PC-Checker starten</button>
</body>
</html>
"""

other_pages = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>{{ title }}</title>
</head>
<body>
    <h2>{{ title }}</h2>
    <ul>
        <li><a href="{{ url_for('dashboard') }}">Dashboard</a></li>
        <li><a href="{{ url_for('pins') }}">Pins</a></li>
        <li><a href="{{ url_for('results') }}">Results</a></li>
        <li><a href="{{ url_for('strings') }}">Strings</a></li>
        <li><a href="{{ url_for('downloads') }}">Downloads</a></li>
        <li><a href="{{ url_for('logout') }}">Logout</a></li>
    </ul>
    <p>Hier ist die Seite für {{ title }}.</p>
</body>
</html>
"""

@app.route("/", methods=["GET", "POST"])
def login():
    if "user" in session:
        return redirect(url_for("dashboard"))

    if request.method == "POST":
        username = request.form["username"]
        password = request.form["password"]

        if username in users and users[username] == password:
            session["user"] = username
            return redirect(url_for("dashboard"))
        else:
            return render_template_string(login_page, error="Falscher Benutzername oder Passwort!")

    return render_template_string(login_page, error=None)

@app.route("/register", methods=["POST"])
def register():
    username = request.form["username"]
    password = request.form["password"]

    if username in users:
        return render_template_string(login_page, error="Benutzername existiert bereits!")
    
    users[username] = password
    return render_template_string(login_page, error="Registrierung erfolgreich! Bitte einloggen.")

@app.route("/dashboard")
def dashboard():
    if "user" not in session:
        return redirect(url_for("login"))
    return render_template_string(dashboard_page, user=session["user"])

@app.route("/pins")
def pins():
    if "user" not in session:
        return redirect(url_for("login"))
    return render_template_string(other_pages, title="Pins")

@app.route("/results")
def results():
    if "user" not in session:
        return redirect(url_for("login"))
    return render_template_string(other_pages, title="Results")

@app.route("/strings")
def strings():
    if "user" not in session:
        return redirect(url_for("login"))
    return render_template_string(other_pages, title="Strings")

@app.route("/downloads")
def downloads():
    if "user" not in session:
        return redirect(url_for("login"))
    return render_template_string(other_pages, title="Downloads")

@app.route("/logout")
def logout():
    session.pop("user", None)
    return redirect(url_for("login"))

if __name__ == "__main__":
    app.run(debug=True)
