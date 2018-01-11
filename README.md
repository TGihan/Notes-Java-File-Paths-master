# Java-File-Paths-Tutorials

#1. SWING App image icon load in different situations

<b>When run in Local IDE</b></br>
when you want to load ImageIcon and you run in local machine IDE
FlogClient.class.getClassLoader().getResource("images//comment.gif"));  

//NOTE DUBBLE SLASH AND NOT LEADING SLASH LIKE /images//..

<b>After build JAR</b></br>
But when you build your app to maven single jar you can't use such path you will get null Exception when load image.use below 
new ImageIcon(getClass().getResource("/images/magnify.gif")); 

//NOTE NO DUBBLE SLASH AND LEADING SLASH 

<b>This will work fine in both jar and local so use second</b>

#2. File Object Access in JAR 
By default after build jar all resource files includes in classes folder so directly can use as follows
musicfile = new File("classes//sounds//america.mp3");

<b>but this is not working in local IDE</b>



