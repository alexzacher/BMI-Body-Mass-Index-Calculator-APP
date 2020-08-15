# Body Mass Index - App /(Pt-Br) IMC - Aplicativo

 
 ![final](https://user-images.githubusercontent.com/47509134/90312509-f0b8f700-defc-11ea-9672-86da6e9e2899.png)
  _This is a app from a python corse in 2020, as my frist project the code is simple._

You do not know what is BMI check it out > [Wikipedia BMI](https://en.wikipedia.org/wiki/Body_mass_index)
# Create a BMI calculator Program Description
> The program should allow the user to enter a person’s name.

> User has to choose whether to enter the values as Imperial or Metric measurements.

> If the user chooses to use [imperial measurements](https://en.wikipedia.org/wiki/Imperial_units) the height should be entered as __feet and inches__. The weight should be entered as __stones and pounds__. __The program should convert the entered values to metric equivalents and display them.__

> If the user chooses to use [metric measurements](https://en.wikipedia.org/wiki/Metric_system) the height should be entered as centimetres. The weight should be entered as kilograms. The __program should convert the entered values to imperial equivalents and display them__.

> The program should then calculate the BMI and display the result.  The program should also display further information telling the user if the persons BMI indicates if they are __underweight__, __normal__, __overweight__ or obese using the values __shown in this table__.

> Save the name, height and weight, and date/time for each person into a __CSV__ file

 BMI | Values
:---|---:
Underweight | les than 18.5
Normal | between 18.5 and 24.9
Overweight | between 25 and 29.9
Obese | 30 or greater


### Front-end
* Tkinter graphic interaction
  * Whats is it Tkinter?
   * Tkinter is Python's de-facto standard GUI (Graphical User Interface)
   * You can check out on [Wikipedia-Tkinter](https://en.wikipedia.org/wiki/Tkinter).


### Back-end
 * Pyhton program
 * CSV ( Data Base )
   * You can check out on [wikipedia-CSV](https://en.wikipedia.org/wiki/Comma-separated_values)
   * Example below
```
from tkinter.filedialog import askopenfilename

def import_csv_data():
    global v
    csv_file_path = askopenfilename()
    print(csv_file_path)
    v.set(csv_file_path)
    #df = pd.read_csv(csv_file_path)

root = tk.Tk()
tk.Label(root, text='File Path').grid(row=0, column=0)
v = tk.StringVar()
entry = tk.Entry(root, textvariable=v).grid(row=0, column=1)
tk.Button(root, text='Browse Data Set',command=import_csv_data).grid(row=1, column=0)
tk.Button(root, text='Close',command=root.destroy).grid(row=1, column=1)
root.mainloop()
```
