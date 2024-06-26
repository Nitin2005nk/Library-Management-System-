# Library-Management-System-

# Objective

The objective of this is to create a GUI based  Library Management System. To build this, you will need intermediate understanding of the SQLite API and its commands, intermediate understanding of  Tkinter library, Ttk module’s Treeview, and basic understanding of messagebox module.

# Import Library
# Importing all necessary modules
import sqlite3

from tkinter import *
import tkinter.ttk as ttk
import tkinter.messagebox as mb
import tkinter.simpledialog as sd

# Connecting to Database
connector = sqlite3.connect('library.db')
cursor = connector.cursor()

connector.execute(
'CREATE TABLE IF NOT EXISTS Library (BK_NAME TEXT, BK_ID TEXT PRIMARY KEY NOT NULL, AUTHOR_NAME TEXT, BK_STATUS TEXT, CARD_ID TEXT)'
)
