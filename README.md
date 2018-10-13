1.1 搭建WEB项目框架 — 将Maven项目调整为Web目录结构：

    (1) 在main目录下添加webapp目录
    (2) 在webapp目录下，添加WEB-INF目录
    (3) 在WEB-INF目录下，添加web.xml文件

    添加好后IDEA会给个提示：
        Frameworks detected
        Web framework detected in the project Configure...
        点进config后点击配置完成，此时当前项目已变为Web项目。
    
1.2 此项目使用Servlet 3.0框架

        <?xml version="1.0" encoding="UTF-8"?>
        <web-app xmlns="http://java.sun.com/xml/ns/javaee"
                xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                xsi:schemaLocation="http://java.sun.com/xml/ns/javaee
                http://java.sun.com/xml/ns/javaee/web-app_3_0.xsd"
                version="3.0">
        </web-app>
        
        实际上，使用Servlet3.0框架是可以省略web.xml文件的，因为Servlet无须在web.xml文件里配置，只需通过java注解的方式来配置即可。例如：
        @WebServlet("/hello")
        
3. ctrl + F9：手动编译

4. 将代码放入Git仓库中：
    
        VCS菜单 > Import into Version Control/Create Git Repository...
        在弹出的对话框中选择项目根目录，点击OK即可。此时，IDEA就为我们在本地建立了一个Git仓库。
        
        选择项目根目录，单机"Git/Add"菜单项，可将除.gitignore文件中忽略的所有文件添加到本地Git仓库中
        
        Ctrl + Alt + A：选择需要提交的文件(注：如果开启了QQ，需要解决热键冲突问题)
        
        提交时，可勾选"Optimize imports"选项，优化import语句。
        
        提交快捷键：Ctrl+K
        
5. 