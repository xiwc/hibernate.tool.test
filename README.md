# thymeleaf.test
Html5(thymeleaf & semantic-ui & jQuery) + Spring(webMVC & jpa) testing.

### Front-end
>
* html+js+css (thymeleaf+jquery+semantic-ui) 
* html5 (http://www.w3school.com.cn/html5/)
* thymeleaf (http://www.thymeleaf.org/documentation.html)
* Dropzone file uploader (http://www.dropzonejs.com/)
* toastr notification (http://codeseven.github.io/toastr/)
* fancyBox slide show (http://fancyapps.com/fancybox/)
* wangEditor (https://github.com/wangfupeng1988/wangEditor)
* wysiwyg.js editor (http://wysiwygjs.github.io/)
* async iframe upload file (http://cmlenz.github.io/jquery-iframe-transport/)
* Font-Awesome (http://fortawesome.github.io/Font-Awesome/)
* CKEditor (http://ckeditor.com/)
* bootstrap (http://getbootstrap.com/)
* bootstrap-markdown (https://github.com/toopay/bootstrap-markdown)
* bootstrap-markdown-doc (http://www.codingdrama.com/bootstrap-markdown/)
* jquery.hotkeys (https://github.com/jeresig/jquery.hotkeys)
* markdown-js (https://github.com/evilstreak/markdown-js)

### Back-end
>
* spring-boot (web+jpa+h2) 
* spring-framework http://projects.spring.io/spring-framework/
* spring-boot (http://projects.spring.io/spring-boot/)
* spring-data-jpa (http://projects.spring.io/spring-data-jpa/)
* implement the image file upload store

### jquery features test
>
* jQuery (http://jquery.com/)
* jQuery.Deferred
* jQuery.Callbacks
* jQuery.html5Uploader

### semantic-ui features test
>
* semantic-ui (http://semantic-ui.com/)
* ui form
* api
* table sort (https://github.com/kylefox/jquery-tablesort)
* radioButtion `th:field value == th:value` set checked attribute

### spring web
>
* ModelMap
* jpa
* hot reload java class (https://github.com/spring-projects/spring-loaded)
  cmd: java -javaagent:C:/Users/weichx/.m2/repository/org/springframework/springloaded/1.2.3.RELEASE/springloaded-1.2.3.RELEASE.jar -noverify SomeJavaClass
* maven (http://maven.apache.org/pom.html)
* jpa crud testing

### automation build
>
1. clean webapp/upload
2. include external web resources when packaging


### deploy to tomcat server
>
* remote deploy
	1. tomcat manager app users(int conf/tomcat-users.xml) (http://tomcat.apache.org/tomcat-8.0-doc/manager-howto.html)
	2. tomcat7-maven-plugin(in pom.xml) 
 		* configuration (http://tomcat.apache.org/maven-plugin-2.2/tomcat7-maven-plugin/usage.html)
 		* Goals available for this plugin (http://tomcat.apache.org/maven-plugin-2.2/tomcat7-maven-plugin/plugin-info.html)
* core config
```
int conf/tomcat-users.xml
<role rolename="manager-gui"/>
<role rolename="manager-script"/>
<user username="test" password="test" roles="manager-gui,manager-script"/>
-------------------
(in pom.xml)
<plugin>
	<groupId>org.apache.tomcat.maven</groupId>
	<artifactId>tomcat7-maven-plugin</artifactId>
	<version>2.2</version>
	<configuration>
		<url>http://localhost:80/manager/text</url>
		<username>test</username>
		<password>test</password>
		<path>/</path>
		<update>true</update>
	</configuration>
</plugin>
-------------------
(deploy exec cmd)
tomcat7:deploy
```

# TODO
>
* form validation
* api for form (https://github.com/macek/jquery-serialize-object)
* enhance `jQuery.html5Uploader`
* slide show for images
* rich html text editor
* message tooltip
* chart highcharts (http://www.hcharts.cn/index.php) (http://www.highcharts.com/)
* save spring-boot metric info into database.