# Class-and-object

from datetime import date
name="mohitha"
print(type(name))
print(dir(name))


class Student:
    pass
st1=Student()
st2=Student()

st1.name="Mohitha"
st1.dob=2003
st1.regno=128

st2.name="Mathan"
st2.dob=2006
st2.regno=200

print(st1.name)
print(st2.name)


class Students:
    fee=20000
    no_stu=0
    def __init__(self,name,rollno,dob):
        self.name=name
        self.rollno=rollno
        self.dob=dob
        Students.no_stu=Students.no_stu + 1
        
    def address(self):
        add=f"name : {self.name}\nrollno : {self.rollno}\ndob : {self.dob}"
        return(add)
    
    def age(self):
        current_year=date.today().year
        return(current_year-self.dob)

    def pay_fee(self,amount):
        self.fee=self.fee-amount
        return(self.fee)

    
stu1=Students("Mohitha",142,2003)
stu2=Students("Mathan",153,2006)
stu1.pay_fee(5000)
print(stu1.name)
print(stu2.dob)
print(stu1.address())
print(stu2.address())
print(stu1.age())
print(stu2.age())
print(stu1.fee)
print(stu1.__dict__)
print(stu1.fee)
print(stu2.fee)
print(Students.no_stu)
