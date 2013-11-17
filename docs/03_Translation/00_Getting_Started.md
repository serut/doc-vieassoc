We try our best to correctly place the language files for each page.
For the page 

	http://association.vieassoc.lo/1/edit/general-informations#

You will found language keys-values on
	
	\app\lang\fr\association\edit\general-informations.php
 
Please follow these simples rules - it will help for maintenance and the future translation of the website.


## For developers 
You just need to call this method :
	
	Lang::get()

And in a blade view, you will write 

	{{Lang::get()}}

For exemple, you can access to /folder1/folder2/folder3/file for the key KEY by using

	{{Lang::get('folder1/folder2/folder3/file.KEY')}}

