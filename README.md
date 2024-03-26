# weather-forecast-python-project
from tkinter import *
from tkinter import  ttk
import requests


city_name="Kannauj"
data=requests.get("https://api.openweathermap.org/data/2.5/weather?q={city name}"+city_name+"&appid=d04a9f74e2e5105c164967190d086254".json())
print(data)

root=Tk()
root.title("Weather Forecast")
root.geometry("500x500")
root.config(bg="blue")

Title=Label(root,text="Weather Forecast",font=("time new roman",40,"bold"))
Title.place(x=25,y=50)

list_name=["Andhra Pradesh","Arunachal Pradesh","Assam","Bihar","Chhattisgarh","Goa","Gujarat","Haryana","Himachal Pradesh","Jharkhand","Karnataka","Kerala","Maharashtra","Madhya Pradesh","Manipur","Meghalaya","Mizoram","Nagaland","Odisha","Punjab","Rajasthan","Sikkim","Tamil Nadu","Tripura","Telangana","Uttar Pradesh","Uttarakhand","West Bengal","Andaman & Nicobar","Chandigarh","Dadra & Nagar Haveli and Daman & Diu","Delhi","Jammu & Kashmir","Ladakh","Lakshadweep","Puducherry"]
com=ttk.Combobox(root,text="Weather Forecast",values=list_name,font=("time new roman",20,"bold"))
com.place(x=25,y=150)

but=Button(root,text="Done",font=("time new roman",25,"bold"),bg="orange")
but.place(x=150,y=200)

climate=Label(root,text="Weather climate",font=("time new roman",20,"bold"))
climate.place(x=25,y=280)
climate1=Label(root,text="",font=("time new roman",20,"bold"))
climate1.place(x=300,y=280)

wd=Label(root,text="Weather Description",font=("time new roman",17,"bold"))
wd.place(x=25,y=320)
wd1=Label(root,text="",font=("time new roman",17,"bold"))
wd1.place(x=300,y=320)

temp=Label(root,text="Temperature",font=("time new roman",20,"bold"))
temp.place(x=25,y=355)
temp1=Label(root,text="",font=("time new roman",20,"bold"))
temp1.place(x=300,y=355)

press=Label(root,text="Pressure",font=("time new roman",20,"bold"))
press.place(x=25,y=395)
press1=Label(root,text="",font=("time new roman",20,"bold"))
press1.place(x=300,y=395)

root.mainloop()
