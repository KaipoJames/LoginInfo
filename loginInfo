from tkinter import *
import tkinter as tk
import os

from Member import Member

os.system('clear')

root = tk.Tk()
root.title("Sample Desktop App")
root.geometry("600x600")

login_info = []
user_id_list = []
members = []

count = 99
for num in range(10):
    count += 1
    user_id_list.append(count)
# root.configure(background="white")


def create_member():
    inoa = real_name.get()
    idade = age.get()
    kelepona = telephone.get()
    email = email_address.get()
    username = name.get()
    password = p_word.get()

    print("1:")
    print(user_id_list)
    user_id = user_id_list[0]

    new_member = Member(inoa, user_id, idade, kelepona, email, username, password)
    print(new_member.member_id)

    deleted = user_id_list.pop([0])
    print(deleted)
    print("2:")
    print(user_id_list)

def save_login_info():
    create_member()

    username = name.get()
    password = p_word.get()
    login_info.append(username)
    login_info.append(password)

    file = 'login_information.txt'
    with open(file, 'w') as f:
        for data in login_info:
            f.write("Username: " + data + ",")


frame = Frame(root, bg = "white", height=390, width=590)
frame.pack(side = TOP)

#Prompt for name
label = Label(frame, text="Enter your name: ")
label.pack()
real_name = Entry(frame, width=40)
real_name.pack()

#Prompt for age
label = Label(frame, text="Age: ")
label.pack()
age = Entry(frame, width=40)
age.pack()

#Prompt for phone number
label = Label(frame, text="Phone Number: ")
label.pack()
telephone = Entry(frame, width=40)
telephone.pack()

#Prompt for email
label = Label(frame, text="Email: ")
label.pack()
email_address = Entry(frame, width=40)
email_address.pack()

#Prompt for username
label = Label(frame, text="Enter your username: ")
label.pack()
name = Entry(frame, width=40)
name.pack()

#Prompt for password
label = Label(frame, text="Enter your password: ")
label.pack()
p_word = Entry(frame, width=40)
p_word.pack()

button = Button(frame, text="Submit", command=save_login_info)
button.pack()


root.mainloop()
