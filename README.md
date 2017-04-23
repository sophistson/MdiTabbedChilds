# MdiTabbedChilds
Easy way to use a MDI Windows Form application with Child-Forms in TabControls. No limits in sublevels. 

It is written in VB .NET uses FW 4.6. 

This is my first "solution" with .NET. Please be genereous. I am using VB .NET only since 2 weeks. April 2017 But I think this project template can be really used and it should be easy for advanced coders to implement better code in this frame.
Getting Started

Installation process 
Download und import project template.  
In the project there are 7 forms, 3 of them are only for example running; named: Z1/2*. You can delete them Then there are 2 forms which must be used; FrmMain, which is the MDI Parent and FrmStart which is the first TabControlContainer. The other 2 forms should be ONLY used as a form template. 1) sfrmSubFormTabbed is a container template. Just add to the parent Container, do not code there. 2) sfrmSubForm is a template for "normal" forms. You can do your code work there.

Hints: The first level must be set in FrmStart !!

   - Do not use sfrmSubFormTabbed or sfrmSubForm as instances, only use them as a template !!! see below
   -  Use frmStart and sfrmSubFormTabbed only as a container. Do not add any controls or stuff like this !!!
   - The init method is used, because I wasn't able to realise an overload for "NEW" with additional parameters.
        The overloaded "NEW" was not inherited by the childs. (Welcome to newbie land ;) 

HowTo: 
1) Be sure that the project is builded (Create)

2) Add new form you want to use as a child You must add a new form: Project/ Add Form / Inherited form (vererbte Form) / chose then the template you want 2.1) (-- sfrmSubFormTabbed --) = Child form with tabs, to put more child forms into and nothing else 2.2) (-- sfrmSubForm --) = "Standard" form without a TabControl for child forms. Do here your normal coding

3) Now, declare the direct sub form childs. '######### You can delete this here. It is just an example, also delete the 3 classes: Z1/2*. You find the third call in "Z1Tabbed.vb" Private _Z1Tabbed As Z1Tabbed Private _Z1Standard As Z1Standard '#########

4) The last step is to init this form in Me.Load, only: MyExampleChild = New SfrmSubForm and: MyExampleChild.Init(Me)

    Software dependencies Non dependencies, just use Windows Forms
    Latest releases >> No
    API references >> No

Build and Test
No real testing, it is just a V0.9

Contribute
Explain how other users and developers can contribute to make your code better. 
Ask me :-)
