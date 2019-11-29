# Project-Using-Class-File-Handling-
I have used File Handling and Class to create a hospital and Library management system.
Hospital   CODE:
class hospt():
    def __init__(hospital,patientname,doctorassigned,ward,disease,hospitalcharge,medicines):
        hospital.patientname=patientname
        hospital.doctorassigned=doctorassigned
        hospital.ward=ward
        hospital.disease=disease
        hospital.hospitalcharge=hospitalcharge
        hospital.medicines=medicines
    def show(hospital):
        a=open("y.txt","r")
        q=a.readlines()
        for i in q:
            o=i.split()
            print("Patient's name is ",o[0])
            print("Doctor's name is ",o[1])
            print("Admitted in Ward no.  ",o[2])
            print("Patient is having diease",o[3])
            print("Hospital Bill is ",o[4])
            print("Medicines charges are  ",o[5])
            print("\n\n\n")
        a.close()
    def avg(hospital):
        a=open("y.txt","r")
        q=a.readlines()
        x=0
        for i in q:
            o=i.split()
            x=x+float(o[4])+float((o[5]))
        print("Average of all patients total amount is ",x/len(q))
        a.close()
    def mxx(hospital):
        a=open("y.txt","r")
        q=a.readlines()
        x=0
        y=""
        for i in q:
            o=i.split()
            w=float(o[4])+float(o[5])
            if w>x:
                x=w
                t=o
        print("Maximum bill amount is ",x)
        print("Patient's name is ",t[0])
        print("Doctor's name is ",t[1])
        print("Patient is in ward no. ",t[2])
        print("Patient is suffering from disease ",t[3])
        print("Medicines charges are ",t[5])
        print("Hospital charges are ",t[4])
        a.close()
    def mnn(hospital):
        a=open("y.txt","r")
        q=a.readlines()
        x=10000000000000000
        for i in q:
            o=i.split()
            w=float(o[4])+float(o[5])
            if w<x:
                x=w
                t=o
        print("Minimum bill amount is ",x)
        print("Patient's name is ",t[0])
        print("Doctor's name is ",t[1])
        print("Patient is in ward no. ",t[2])
        print("Patient is suffering from disease ",t[3])
        print("Medicines charges are ",t[5])
        print("Hospital charges are ",t[4])
        a.close()
    def ds(hospital):
        a=open("y.txt","r")
        t=input('Enter name of the disease:')
        q=a.readlines()
        p=[]
        for i in q:
            e=i.split()
            if t==e[3].lower():
                p.append(e)
        for i in p:
            print("Patient's name is ",i[0])
            print("Doctor's name is ",i[1])
            print("Patient is in ward no. ",i[2])
            print("Patient is suffering from disease ",i[3])
            print("Medicines charges are ",i[5])
            print("Hospital charges are ",i[4])
            print('\n\n\n')
        a.close()
x=10
while(x):
    p=int(input("Looking for Something,here is a list of items you can do:-\n1 for Give Inputs\n2 for Display all the patient details\n3 for Calculate average bill of a patient\n4 for Calculate Maximum bill among all patients\n5 for Calculate Minimum bill among all patients\n6 for search people with particular disease\n0 to exit\n "))
    if(p==1):
        a1=int(input("No. of inputs you wants to give:"))
        for i in range(a1):
            b1=input("Enter Patient's Name:")
            b2=input("Enter Doctor's Name:")
            b3=input("Enter ward number:")
            b4=input("Disease of the patient:")
            b5=input("Hospital charges:")
            b6=input("Medicines charges:")
            print("\n\n\n")
            m=hospt(b1,b2,b3,b4,b5,b6)
            a=open("y.txt","a")
            a.write(b1+" ")
            a.write(b2+" ")
            a.write(b3+" ")
            a.write(b4+" ")
            a.write(b5+" ")
            a.write(b6+"\n")
            a.close()
    elif(p==2):
          m.show()
    elif(p==3):
          m.avg()
    elif(p==4):
          m.mxx()
    elif(p==5):
          m.mnn()
    elif(p==6):
          m.ds()
    elif(p==0):
        x=0
    else:
         print("Enter a valid number!!!!!!!!!!!!!!!")



Library Code:
