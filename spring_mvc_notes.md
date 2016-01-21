spring MVC
============

Components:
-----------

1. Model

  > This contains the business logic, Rules , entity classes

2. View 

  > This contains the jsp , html, and all other view related code

3. Controller

  > This acts as a facilitator/ orchestrator for requests that coming up and map them to correspoding classes , serves the request and redirects to the appropriate view and populate view with the values.
  
Basic Requirements:
-------------------

1. Jdk
2. Spring Tool suite / Eclipse
3. A web server

Create Project:
---------------

> In IDE, selecte New->Spring Project-> Spring MVC.

Important Annotation & Code Fragments:
--------------------------------------

`@Controller` 

> To denote that the class is going to be acts as controller.

> The controller package has to be mentioned in servler-context.xml (context for DispatcherServlet)

> ` <context:component-scan base-package="com.saftware.firstmvc" /> `

> ` <annotation-driven /> `


`@RequestMapping` 

>On method / class level to map the method with the request URL.

> The following options are available.

> `value` - To specify the url pattern (includes path param)

> `method` - To specify the request method. GET,POST...

> `params` - To specify the query param

`Model class` 

> This is a map class used to pass values from controller to the jsp page

> The reference can be get by passing Model as parameter in Request methods.

> At runtime, spring mvc will put the values and pass it to view

`Return view page`

> The String returned by the requestmethod will be used by the InternalResourceViewResolver for next view page to be returned.

> The prefix and suffix will be used from the xml configuration.

> `<!-- Resolves views selected for rendering by @Controllers to .jsp resources in the /WEB-INF/views directory -->`
>	`<beans:bean class="org.springframework.web.servlet.view.InternalResourceViewResolver">`
>	`	<beans:property name="prefix" value="/WEB-INF/views/" />`
>	`	<beans:property name="suffix" value=".jsp" />`
>	`</beans:bean>`

`Redirect:`

> Instead of view name, if we want complete redirection (ie to another controller method, use redirect)

> In return value of method, prefix it with "redirect:"





