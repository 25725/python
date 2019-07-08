import pymysql as sql
db=sql.connect(host='localhost',port=3306,user='root',password='',database='internbatch2')
c=db.cursor()
#cmd="create table student(int id(10),name varchar(100),address var(100),age varchar(30))"
#c.execute(cmd)
o=int(input("1.insert\n2.fetch"))
if o==1:
    while True:
        id1=int(input("Enter your id: "))
        name=input("Enter your name : ")
        address=input("Enter your address : ")
        age=input("Enter your age : ")
        cmd="insert into student values({},'{}','{}','{}')".format(id1,name,address,age)
        c.execute(cmd)
        db.commit()
        opt=input("Do you want to continue(yes/no)?")
        if opt=='no':
            break
elif o==2:
    table=input("Enter table name")
    cmd="select * from {}".format(table)
    c.execute(cmd)
    data=c.fetchall()
    for var in data:
        print(f"id-{var[0]}\nname-{var[1]}\naddress-{var[2]}\nage-{var[3]}\n")


