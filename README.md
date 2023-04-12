# Front End Development with Vue.js - IT Academy

## **Sprint 6 - Vue I**

This sprint introduces Vue! The project brief is the following:

> A client has a business management website developed with Vue as the main product and has asked us to develop a tutorial. In this tutorial, new users can advance or go back in tips using two buttons, and the help text and background image will be modified accordingly.

---

### ⭐ **Level 1** ⭐

**— Exercise 1**

- Make two components, `Home` and `Escena`. `Home` is imported inside `App`, and `Escena` is imported inside `Home`.

##### ✅ Finished: 09/04/2023

**— Exercise 2**

- Import a JSON file in `Home` and store its contents in the component data, then pass it to `Escena` as a prop. Render the value of the prop (which is an array of phrases) as a list with `v-for`.

##### ✅ Finished: 10/04/2023

**— Exercise 3**

- Apply (very light) styling to 'Escena'.

**— Exercise 4**

- Add `Botons` component, which contains two buttons ("Back" and "Next") that, when clicked on, highlights the next or previous sentence in our list of phrases. This is done by having the buttons emit an event that the parent component (`Home`) catches and performs a method with it, and then passes the result to `Escena` via a prop.

##### ✅ Finished: 12/04/2023

---

### ⭐⭐ **Level 2** ⭐⭐

**— Exercise 5**

- Make a Welcome page that shows before the list of phrases, and add a start button that displays the phrases when clicked on. I had to use the `v-if` directive for this.

##### ✅ Finished: 12/04/2023

---

### ⭐⭐⭐ **Level 3** ⭐⭐⭐
