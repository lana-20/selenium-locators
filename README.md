# Selenium Locators

With WebDriver methods I can:
1. Identify an element
2. Perform action (on the web element)

Locators are used to identify web elements. The type of locators used depends on the context, application and types of elements themselves.

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

![image](https://user-images.githubusercontent.com/70295997/205466365-8564f15b-61d4-4c72-9a5f-1795302a921a.png)

I cannot  directly find CSS and Xpath in HTML. I have to generate a selector.

Sometimes, even if the correct ID is provided, I can't identify the element. When working with many complex pages, I might encounter this challenge. In this situation, I use another locator combination like 'Tag and ID'.

<img src="https://user-images.githubusercontent.com/70295997/205470966-17b52a76-6a9b-4b01-ac3b-6ddef446bee1.png" width=600></img>

![image](https://user-images.githubusercontent.com/70295997/205473012-4c317cc1-71cd-49e9-b63d-5fcffcab7ff7.png)

70-80% of the time in automation, I prefer to use Xpath. Especially on more complex web pages with dynamic elements, when attributes change dynamically at runtime.

[__Xpath__](https://github.com/lana-20/xpath-locators-selenium/blob/main/Xpath%20Locators%20for%20Selenium.pdf)
 - XML (Extensible Markup Language) path
 - Syntax/language for finding any element on the web page using XML path expression
 - Used to find the location of any element on the web page using HTML DOM structure
 - Used to navigate through elements and attribites in DOM
 - An address of an element

Xpath always works based on the DOM structure, not directly on HTML.

Without an address, there is no element. If there is an element on the web page, that element's address should be there, and the corresponding code should be in the HTML DOM structure.

Sometimes, when an element cannot be identified with any other locator, Xpath will 100% find it. That's the reason I use Xpath most of the times. It works effectively, compared to other locators.

__DOM__
- DOM is an API interface provided by the browser
- When a web page is loaded, the browser creates a __D__ ocument __O__ bject __M__ odel of the page.

![image](https://user-images.githubusercontent.com/70295997/205520803-e9566aef-afcd-4a93-ab8f-8d81b078b2ea.png)

Whenever I open an app in my browser, it automatically creates the DOM structure for the particular page elements. Browser has an internal interface that creates that DOM structure.

Xpath navigates through DOM nodes to find the element. If the browser properly generates the DOM, then Xpath properly works.

  __Types of Xpath__
  
  1) Absolute Xpath
  2) Relative Xpath

![image](https://user-images.githubusercontent.com/70295997/205524355-44ca5738-e7f6-4a09-8195-d50ec05cd677.png)

__Difference between Absolute and Relative Xpath__

<img src="https://user-images.githubusercontent.com/70295997/205525960-5e66f25f-0381-4bf5-907c-ffc49c5262ab.png" width=300></img>

1) Absolute Xpath starts from the root html node and traverses through the node tree until it identifies the desired element. ⟺ Relative Xpath directly jumps to the desired element in DOM. Relative Xpath does not start at the beginning/root. It works based on a certain attribute (id, name, etc.). It goes/jumps to the element whose attribute I specify, and the rest of the path is then followed.

2) Absolute path starts with __/__. ⟺ Relative path starts with __//__.

3) In Absolute Xpath, use only tags/nodes. ⟺ In Relative Xpath, use only attributes.
  
__Relative Xpath Syntax__

//tagname[@atribute='value']  ->  can replace __tagname__ with __*__: //*[@atribute='value']
  
__Capture Xpath automatically__

1) Firebug, Firepath - for Firefox -> deprecated
2) Browser itself started providing options for captioning Xpath:
    - Select the element tag in DevTools
    - Right-click > Copy > Copy Xpath (or Copy Full Path)
3) SelectorsHub browser extension 
    - multi-browser, rich features
    - suggests multiple locators, not just Xpath
    - can right-click on the element and use SelectorHub options directly.
  
__[Which Xpath Do You Prefer to Use?](https://github.com/lana-20/xpath-locators-selenium/blob/main/Which%20Xpath%20Do%20You%20Prefer%20to%20Use.pdf)__

__Relative Xpath__
- starts with __//__, which means it can search for an alement anywhere on the page
- the path starts in the middle of the HTML DOM structure
- no need to write a long Xpath
- more stable than Absolute Xpath
      
 __Xpath Options__ (methods):
 - and
 - or
 - contains()
 - starts-with()
 - text()

![image](https://user-images.githubusercontent.com/70295997/205553488-41420d60-ef89-4dc7-8e8f-da202420f41e.png)
