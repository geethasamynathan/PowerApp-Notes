Steps to PowerApp Creation

Download the data from below link

https://github.com/geethasamynathan/PowerApp-Notes/blob/main/Products.xlsx

upload the excel.xlsx file into Onedrive 

![alt text](image.png)

appName ==> ProductDisplay ==> 
![alt text](image-1.png)

from the left pane ==> ![alt text](image-2.png)

![alt text](image-3.png)
![alt text](image-4.png)


![alt text](image-5.png)
![alt text](image-6.png)

![alt text](image-7.png)

![alt text](image-8.png)
![alt text](image-9.png)

Go back to Treeview of your app

choose the screen1
 
 ![alt text](image-10.png)

 By default it will be showing the sample data

 ![alt text](image-11.png)

 let us add our datasource to display our products

 Select Gallery1 ==> on the top you can find Data => click that ==> choose the datasource

 ![alt text](image-12.png)

 once you click the onedrive it takes few minutes to attach the data into our Gallery
 ![alt text](image-13.png)

 ![alt text](image-14.png)

 ![alt text](image-15.png)
 ![alt text](image-16.png)

 ![alt text](image-17.png)



 add a Form for CRUD OPeration

 ![alt text](image-18.png)

 Data ==> Choose the table from onedrive ==>
 ![alt text](image-19.png)

 ![alt text](image-20.png)

 Add fields ==> choose the columns to add in the form
 select the Form ==> column = 1
 ![alt text](image-21.png)

 After reorder the fields in the form .

 Next we will change cateroy control should be dropdownlist

 select the CategoryDatacard ==> Delete categoryDatacardValue field ==>
 in that place insert dropdownlist


 ![alt text](image-22.png)

 Insert ==> dropdownlist
 ![alt text](image-23.png)
Categorydatacard
update  = ddlCategory.Selected.Value
![alt text](image-24.png)

![alt text](image-25.png)

![alt text](image-26.png)

While running if the form is not visible change Form DEfaultMode property= New

then run


Select the Form1 from Left pane
insert ==> Button ==> 
change the Text Property as Save Changes


Button placed outside of the form
but we need place it inside the form

![alt text](image-27.png)

![alt text](image-28.png)

Form should the selected prodcut details from gallery

![alt text](image-29.png)

Form DEfaultMode ==>Edit 


Select the button ==> On select = sunbmitForm(Form1)

Run  

update the product  click savechanges it will update in datasource too



Next we will Add New Product


Addnew button on the top form

onselect = NewForm(Form1);UpdateContext({isNewRecord:true})


select the SaveChanges(button1)  property

![alt text](image-30.png)

Onselect event of Button (save changes) 
If(
    isNewRecord,
    SubmitForm(Form1); 
    UpdateContext({isNewRecord: false}),  // Reset the flag after saving new record
    SubmitForm(Form1) // Normal Save for existing records
)

![alt text](image-31.png)