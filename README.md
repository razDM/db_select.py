# db_select.py

import cx_Oracle

class Oracle():
    def __init__(self,sql):
        self.sql = sql
    def query(self):
        db = cx_Oracle.connect('raz','admin01','xe')
        self.cur = db.cursor()
        self.query = self.cur.execute(self.sql)
        return print(self.cur.fetchmany(5))
        cur.close()
        db.close()
v_raz = "select * from EMP"
v_raz1 = "select sysdate||' raz1' from dual"

raz = Oracle(v_raz)
raz1 = Oracle(v_raz1)

raz.query()
raz1.query()
