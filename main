import tkinter

# a function for controlling weight and height data
def control_data(value):
    if value=='.':
        return False
    elif value.count('.')>1:
        return False
    elif int(value)<=0:
        return False
    for i in value:
        if not (i.isnumeric() or i.count('.')==1):
            return False

# create window

window = tkinter.Tk()
window.title("BMI Calculator")
window.minsize(width=300,height=400)
window.config(pady=10)


#label for weight

label_1 = tkinter.Label(text="Enter Your Weight (kg)")
label_1.config(pady=10)
label_1.pack()

# entry for weight

entry_1 = tkinter.Entry(width=15)
entry_1.pack()



#label for height

label_2 = tkinter.Label(text="Enter Your Height (m)")
label_2.config(pady=10)
label_2.pack()

# entry for height

entry_2 = tkinter.Entry(width=15)
entry_2.pack()



# Calculate Button

    # labels for writing BMI and weight range
last_label = tkinter.Label()
last_label_2 = tkinter.Label()

def button_func():

    if (control_data(entry_1.get()) != False) and (control_data(entry_2.get()) != False):
        weight = float(entry_1.get())
        height = float(entry_2.get())
        bmi = weight / (height**2)

        if 0<bmi and bmi<18.5:
            last_label.config(text=f"Your bmi is {bmi}")
            last_label.place(x=150 - 45, y=160)
            last_label_2.config(text="You are underweight")
            last_label_2.place(x=150 - 45, y=180)

        elif bmi>=18.5 and bmi<25:
            last_label.config(text=f"Your bmi is {bmi}")
            last_label.place(x=150 - 45, y=160)
            last_label_2.config(text="You are normal")
            last_label_2.place(x=150 - 45, y=180)

        elif bmi>=25 and bmi<30:
            last_label.config(text=f"Your bmi is {bmi}")
            last_label.place(x=150 - 45, y=160)
            last_label_2.config(text="You are overweight")
            last_label_2.place(x=150 - 45, y=180)

        elif bmi>=30:
            last_label.config(text=f"Your bmi is {bmi}")
            last_label.place(x=150 - 45, y=160)
            last_label_2.config(text="You are obese")
            last_label_2.place(x=150 - 45, y=180)

    else:
        last_label_2.config(text="")
        last_label.config(text="Please enter a valid data!")
        last_label.place(x=150-63, y=160)


button_1 = tkinter.Button(text="Calculate",command=button_func)
last_label.config(text="")
last_label_2.config(text="")
button_1.place(x=150-30,y=130)

window.mainloop()
