from flask import Flask, render_template, request
from flask_mysqldb import MySQL
app = Flask(__name__)


app.config['MYSQL_HOST'] = 'localhost'
app.config['MYSQL_USER'] = 'teja'
app.config['MYSQL_PASSWORD'] = 'teja8352'
app.config['MYSQL_DB'] = 'MySql'

mysql = MySQL(app)

@app.route('/')
def index():
        cur = mysql.connection.cursor()
        cur.execute('''CREATE TABLE details(firstname varchar(30), lastname varchar(30), age int(5), hobby varchar(30)''')
        mysql.connection.commit()
        cur.close()
        return 'success'


if __name__ == '__main__':
    app.run(host="0.0.0.0",port=80)
