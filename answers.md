# Assignment 1 — HTML & CSS
## Part A: Written Questions and Answers

> **Student:** Sujal Taware  
> **Subject:** HTML & CSS  
> **Purpose:** Short answers in simple language for revision and submission.

---

## Q1. What happens when a user opens your portfolio from a link?

**Answer:**

1. The browser sends an HTTP request to the web server for the portfolio page.
2. The server sends the requested HTML file back to the browser.
3. The browser reads the HTML and requests linked files such as CSS stylesheets and images.
4. The browser uses HTML and CSS to display the page.

For a dynamic website, application logic usually runs on the server and communicates with a database. The database stores persistent information. This assignment is a static website, so it does not need a database.

**Client–server diagram:** See `client-server-diagram.png` in the assignment folder.

---

## Q2. Should a contact form use GET or POST? What happens if the method is omitted?

**Answer:**

A contact form should usually use **POST** because it submits a message to the server. GET is mainly used to request information and can place form values in the URL.

If the `method` attribute is omitted, the form uses **GET** by default.

- **Success status codes:** `2xx`, such as `200 OK` or `201 Created`.
- **Server failure status codes:** `5xx`, such as `500 Internal Server Error`.

---

## Q3. What are the three types of CSS? Which one should be used across four pages?

**Answer:**

| CSS type | Where it is written |
|---|---|
| Inline CSS | In an element's `style` attribute |
| Internal CSS | Inside a `<style>` element in the HTML page |
| External CSS | In a separate `.css` file linked to the HTML page |

When normal declarations compete for the same property, inline styles generally take precedence over ordinary internal and external rules. Specificity and source order also affect the result.

For four pages, I would use **external CSS** because one shared stylesheet keeps the design consistent and makes updates easier.

---

## Q4. Which CSS selector applies to `<p id="intro" class="note">Hello</p>`?

**Answer:**

If all four rules set a different colour for this paragraph, `#intro` wins because an ID selector has higher specificity than a class or element selector.

From strongest to weakest for these selectors:

1. `#intro` — ID selector
2. `.note` — class selector
3. `p` — element selector
4. `*` — universal selector

If competing declarations have equal specificity, the later applicable rule generally wins. Other cascade rules, such as `!important`, can affect precedence.

---

## Q5. Explain padding, margin, border and `box-sizing: border-box`.

**Answer:**

- **Content:** The actual text, image or other content inside an element.
- **Padding:** Space between the content and the border.
- **Border:** The line surrounding the content and padding.
- **Margin:** Space outside the border, separating the element from others.

```text
┌──────────────────────────────┐
│             MARGIN           │
│  ┌────────────────────────┐  │
│  │         BORDER         │  │
│  │  ┌──────────────────┐  │  │
│  │  │     PADDING      │  │  │
│  │  │  ┌────────────┐  │  │  │
│  │  │  │  CONTENT   │  │  │  │
│  │  │  └────────────┘  │  │  │
│  │  └──────────────────┘  │  │
│  └────────────────────────┘  │
└──────────────────────────────┘
```

`box-sizing: border-box` makes the declared width and height include the content, padding and border. This makes element sizing easier to manage.

---

## Q6. Where does JavaScript run, and what is a JavaScript engine?

**Answer:**

JavaScript can run in a browser using its JavaScript engine. For example, Chrome uses the **V8** engine. The engine parses and executes JavaScript and may compile parts of it internally, so developers normally do not need to compile it manually.

Two things JavaScript can do that HTML and CSS alone cannot provide are:

- Validate form data before it is submitted.
- Update page content in response to a button click.

---

## Q7. What happens when JavaScript assigns `5` and then `"hello"` to the same variable?

**Answer:**

JavaScript is dynamically typed, so a variable can hold values of different types.

```javascript
let a = 5;        // a holds a number
a = "hello";      // now a holds a string
```

Three basic JavaScript data types are:

- **Number** — for example, `5`
- **String** — for example, `"hello"`
- **Boolean** — either `true` or `false`

Using `let` or `const` is preferable to assigning to an undeclared variable.

---

## Q8. Explain the four values of the CSS `position` property.

**Answer:**

| Value | Meaning |
|---|---|
| `static` | The default position; the element follows normal document flow. |
| `relative` | The element stays in normal flow but can be offset from its original position. |
| `absolute` | The element is positioned relative to its nearest positioned ancestor. |
| `fixed` | The element is positioned relative to the browser viewport and generally stays in place while scrolling. |

The `top`, `right`, `bottom` and `left` properties set offsets for positioned elements. They do not normally move a `static` element.

---

## Q9. How are flex items sized when their flex values are 1, 2 and 1?

**Answer:**

The `flex` values share the available free space in a **1:2:1 ratio**. If there is no other space taken by gaps, padding or borders, the three boxes receive approximately:

- First box: **25%**
- Second box: **50%**
- Third box: **25%**

`gap` adds space between flex items. `justify-content: center` places the group of items in the centre along the flex container's main axis when there is extra space.

---

## Quick Revision

| Topic | Remember |
|---|---|
| Form `method` omitted | Defaults to `GET` |
| Successful HTTP response | `2xx` status family |
| Server error | `5xx` status family |
| CSS selector specificity here | ID > class > element > universal |
| Padding vs margin | Padding is inside the border; margin is outside |
| `box-sizing: border-box` | Width and height include padding and border |
| JavaScript engine | Executes JavaScript in the browser |
| `position: fixed` | Positioned relative to the viewport |
| Flex values `1, 2, 1` | Share free space in a 1:2:1 ratio |

---

*Prepared for Assignment 1 — HTML & CSS.*
