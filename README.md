# Developing a Simple Webserver

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```python
from http.server import HTTPServer, BaseHTTPRequestHandler

content = '''
<!doctype html>
<html>
<head>
<title> my web server </title>
</head>
<body>
<h1>Top Five Web Application Development Frameworks</h1>
<h2>1.Django</h2>
<h2>2. MEAN Stack</h2>
<h2>3. React </h2>
</body>
</html>



class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200)
        self.send_header("content-type", "text/html")
        self.end_headers()
        self.wfile.write(content.encode())


print("This is my webserver")
server_address = ('', 8000)
httpd = HTTPServer(server_address, MyServer)
httpd.serve_forever()
#python3 webserver.py
```
## OUTPUT:
![Screenshot 2023-03-25 145445](https://user-images.githubusercontent.com/118423842/227708850-45e1dd7f-beb0-4683-844c-49d71c33d518.png)
## RESULT:
The program is executed succesfully
