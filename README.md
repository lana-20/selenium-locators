# Selenium Locators

With WebDriver methids I can:
1. Identify an element
2. Perform action (on the web element)

Locators are used to identify web elements. The type of locators used depends on the contect, application and types of elements themselves.

## Types of Locators
- Identify various elements on the web using __Locators__.
- __Locators__ are addresses that identify a web element uniquely within the page.

__Default / Built-in__ Locators:
1. id
2. name
3. class_name
4. link_text
5. partial_link_text
6. tag_name

__Customized__ Locators:

7. css_selector:
  - Tag and Id
  - Tag and Class
  - Tag and Attribute
  - Tag, Class and Attribute
8. xpath: 
  - Absolute Xpath
  - Relative Xpath



I cannot  directly find CSS and Xpath in HTML. I have to generate a selector.

Sometimes, even if the correct ID is provided, I can't identify the element. When working with many complex pages, I might encounter this challenge. In this situation, I use another locator combination like 'Tag and ID'.

