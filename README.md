# 🏛️ Holy Grail Layout Mockup (Advanced CSS Grid)

This project is a highly responsive "Holy Grail" web layout built exclusively using **CSS Grid**, developed as an assignment for **The Odin Project** curriculum. The core challenge was to build a complex, multi-layered layout and responsive card component system without using a single line of Flexbox or traditional Media Queries (`@media`).

## 🎯 Project Requirements Checklist (Self-Check)

I have successfully implemented all the technical constraints required for this exercise:

- [x] **Main Container:** Defined with 2 columns where the second column is exactly 4 times larger than the first (`1fr 4fr`) with a `4px` gap.
- [x] **Header & Footer:** Properly spans across both main grid columns (`grid-column: 1 / 3`).
- [x] **Sidebar:** Restricted to the first column (`grid-row: 2 / 4`), featuring a `50px` gap between its items.
- [x] **Navigation & Articles:** Perfectly aligned to span only across the second column.
- [x] **Sub-Grids:** The `ul` menus inside both `.menu` and `.nav` are converted into independent grid structures for seamless link alignment.
- [x] **Smart Centering:** Sidebar text elements and cards are perfectly centered using Grid alignment properties (`place-items: center` / `align-self`).
- [x] **Responsive Cards:** The `.article` section automatically wraps cards using `repeat(auto-fit, minmax(250px, 1fr))` with a `15px` gap.
- [x] **Card Dimensions:** Every article card is locked to a robust height of `200px`.

---

## 🧠 Core Takeaways & What I Learned

### 1. The Magic of `auto-fit` + `minmax()`

Instead of hardcoding layout breakpoints, I mastered fluid responsiveness. By combining `auto-fit` with `minmax(250px, 1fr)`, the browser handles the mathematical heavy lifting: it squeezes cards down to `250px` on small viewports and stretches them dynamically using `1fr` to fill the entire remaining horizontal space on larger viewports.

### 2. Implicit Grid Behavior

I discovered that you don't always need to explicitly declare row templates. By letting the browser handle the **Implicit Grid**, new rows generated automatically as content (such as the 12 article cards) expanded downwards, keeping the page structural integrity flawlessly intact.

### 3. Grid-in-Grid Component Architecture

Learned that a grid item can simultaneously act as a grid parent for its own children. Converting the header's `.menu` into a grid allowed me to control its inner alignment using properties like `align-self` and `justify-self: start` seamlessly.

---

## 🛠️ Technologies & Tools Used

- **HTML5:** Semantic document structure.
- **CSS3:** Advanced CSS Grid, Custom Selectors, Viewport Units (`100vh`), and Modern Box-Sizing (`border-box`).
- **Google Chrome DevTools:** Heavy usage of the Grid inspector overlay to debug box-model padding math and explicit track lines.

---

## 👤 Author & Acknowledgments

- **Mert Misir** - [arifmertmisir](https://github.com/arifmertmisir)
- **Project Source:** Assignment curated by [The Odin Project](https://www.theodinproject.com/).
- **Custom Changes:** Footer text updated to reflect personal development credits while honoring the original educational framework.
