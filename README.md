<h1 align="center"> To Do Appliacation</h1> 
 <p align="center"> <img src="application.png" title="To Do"><br>Welcome To our Application: TO DO  </p>
 
<h2 align="center">Objective</h2> 

The goal of the homework is to create an application to manage your tasks. It should have all the features of main application such as menues, actions and toolbar. The application must store an archive of all the pending and finished tasks.


<h2 align="center"> Use Cases</h2> 

Here is a list of cases that the user could perform with our app:
* A user should be able to close the application of course.
* A Todo application cannot be useful, unless it offers the possibility of creating new tasks.
* The essential components of a task will be defined later
* The View of the main widget should be split in three areas:

* The first (en persistent) area shows the list of today tasks.
* The second one is reserved for pending task (tasks for the future).
* Finally, the third one shows the set of finished tasks.
* Each category must be shown with a custom icon.

* The user could either hide/show the pending and finished views.
* Finally, the tasks entered to your application must remains in the app in future use.
* Meaning, If I create a task and I close the application, next time I opened the application, I should find my tasks and not start from scratch.

* You should write a report on the following concepts:
* A detailled description of an Item based solution for your widgets.
* A second part which contains an MVC Model using either:an **QAbstractTableModel or QSqlQueyrModel**.

<h2 align="center"> Introduction</h2> 

Welcome to our Application,**To Do** is a simple application help users to organize the tasks,is like a calender,you put your tasks that you want do it in the future or may be a task for today and you can also add the finished tasks.It **very usefull and simple** to use it.

<h2 align="center"> Steps to use the application</h2> 

* To access to the application you should to log in by using your login and password in order to enhance the privacy.<br>
* When you login in, first of all you should to do is to go to **file** and click add **new_Task**. <br>
* Than fill the description,choose the date,the corresponding tag and click on **ok**.<br>
* you will see that your task is added in one of the list it depends on the date you choose.<br>
* you can delete the task if you make a mistake when you are filling by clicking on **delete**.<br>
* you can quit the application and if you open the application next time,you find yours tasks and not start from scratch.<br>
* you have the choise of **show/hide** pending and finished tasks.<br>
* Finally I leave you to discover yourself the rest of fuctionalities.<br>

<h2 align="center"> Version</h2> 

 We are creating this application in two version different but have the same work:<br>

* **Version 1:** Using Items Based Widgets in this version we are using **Qlistwidget** to store the tasks added and **Qfile** to to save the content of the application.<br>
* **Version 2:** Using MVC Model,in this version we are using **QlistView** to store the tasks added ,and **QSqlTableModel** base to save the content of the application.<br>
* For More information about this Course **Developing IHM with QT C++** and specific this chapter [click on this link](https://anassbelcaid.github.io/CS311/lectures/widgets2/#mvc-model)<br>

<h1 align="center"> Version 1</h1> 
 <h3>Description</h3>
 
* In the first version we are creating the application using the **Itembased**.
* Our application contain a menu bar this later have **File,Options and Help** as **Menus**,each menu have **Actions**.
* The **menu file** have **new task, delete task and quit**,**new_task**  allow user to add a new task by filling the description ,choosing the date and the tag for this task,**delete** is to delete the task if you make an mistake and **quit**if you want to quit the appliction.
* The **menu options** have **pending and finished** this both allow user to **hide or show** widgets .
* The **menu Help** have two action **About Application** that show information avout TODO and **About_QT** that show information about QT.
* All this is showing in **the listwidget** ,if the user choose the date of today the task will be added in listwidjet 1,but if choose the future it will be added in listwidget2 else in the last listwidget.
* We are adding a **Toolbar**,is contains the **icons** of all our Action.
* We are adding a **calender** to display the date.
* If you **quit** the application and newt time when you opened the application, you **find youurs tasks** and  you will not start from scratch. 
* **For more details about our code you will find comment in all classes**.

<h4 align="center"> Good Reading </h4>



<details>
 
<summary> todo.h</summary>
 
``` 
#ifndef TODO_H
#define TODO_H

#include <QMainWindow>
#include <QTextStream>
#include <QMessageBox>
#include<QListView>
#include<QStringListModel>
#include<QListWidget>
#include <QDate>

QT_BEGIN_NAMESPACE
namespace Ui { class todo; }
QT_END_NAMESPACE

class todo : public QMainWindow
{
    Q_OBJECT

public:
    todo(QWidget *parent = nullptr);
    ~todo();

    void chargerTasks(QString myFile);//method to save the content of each listwidget


private slots:

        void on_actionAbout_Application_triggered();//slot gives information about application
    
        void on_actionAbout_QT_triggered();//slot gives information about QT 
    
        void on_actionNew_Task_triggered();
    
        void on_actionQuit_Task_triggered();//slot allow user to quit the application
    
void on_actiondepending_triggered();//slot allow user to hide/show the pending tasks
    
void on_actionFinished_task_triggered();//slot allow user to hide/show the finished tasks
    
 //void ourelmnt(QIcon icon, QString str1, QDate thedate, QString str2, QListWidget *list);
    
void on_actionDelete_Task_triggered(); //slot allow user to delete tasks 
private:
Ui::todo *ui;
void  addelement(); //method contain the implmentation of adding new task when user click on add new task    
};
#endif // TODO_H
 
```
 
 
</details>
 
https://user-images.githubusercontent.com/93345744/150689247-884d69ac-2ca4-4ccd-b962-67d673cba027.mp4
 

https://user-images.githubusercontent.com/93345744/150689426-3b72b559-4d67-4b13-bf5c-f948b33a3dae.mp4



<h2 align="center"> Inhancements</h2> 
 
 In the two version we are adding :
 * Drag and drop. 
 * Login with user and password.
 * Delete task.

 <h2 align="center"> Conclusion</h2> 

This homework allowed us to practice well all our knowledge learned in this course, in addition to practice very well the container Item based and MVC,byreading 
 the Documentation and look for the porprities and fuctions that should use,also how to create the database and how to insert and select by the way we are apply our knowledge of SQL and connect the both,finally the way to solve the problem occur during the programming.
 
  <h2 align="center"> Email</h2> 
 
 ayoub.hsaine@eidia.ueuromed.org
 <br>
 hsaineayoub77@gmail.com
 

