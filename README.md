# Assignment 2 — Advanced CSS: Flexbox & Grid

## Student Information

**Name:** [Your Name]  
**Group:** [Your Group]  
**Course:** Web Technologies  

---

# Project — Azeke Industries

Azeke Industries is a bicycle store website focused on fixed-gear bicycles, framesets, components, and cycling accessories.

The main purpose of this project is to demonstrate the practical use of modern CSS layout techniques, especially **Flexbox** and **CSS Grid**.

The website includes:

- Navigation bar
- Sticky sidebar
- Introduction section
- Brand showcase
- Product cards
- Image gallery
- About section
- Contact information
- Footer
- Hover effects and CSS transitions
- Smooth navigation between sections

---

# Part 1 — Flexbox

## Task 0 — Navigation Bar

The navigation bar was created using **CSS Flexbox**.

The header contains the website logo and name on the left side and navigation links on the right side.

The main Flexbox properties used are:

```css
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
```

`justify-content: space-between` places the logo and navigation on opposite sides of the header.

`align-items: center` vertically centers the elements.

The navigation links also use Flexbox:

```css
.nav {
    display: flex;
    gap: 15px;
}
```

The `gap` property creates consistent spacing between navigation links.

The header also uses `position: sticky`, which keeps it visible while scrolling.

### Screenshot

<img width="614" height="186" alt="image" src="https://github.com/user-attachments/assets/2b37895e-09d9-4d0d-9729-251bb24420b7" />

---

## Task 1 — Card Row

The product section contains multiple bicycle product cards.

Each card contains:

- Product image
- Product name
- Model or color
- Price
- View Product button

The product container uses Flexbox:

```css
.product-list {
    display: flex;
    justify-content: space-evenly;
    align-items: stretch;
    gap: 20px;
    padding: 20px;
}
```

Flexbox is used to arrange the cards horizontally and provide equal spacing between them.

The cards have equal dimensions and include a hover animation.

```css
.product1 {
    width: 300px;
    height: 400px;
    transition: transform 0.3s ease;
}

.product1:hover {
    transform: scale(1.05);
}
```

When the user moves the cursor over a product, the card smoothly increases in size.

The View Product buttons also have hover effects that change their color and size.

### Screenshot

<img width="2250" height="1290" alt="image" src="https://github.com/user-attachments/assets/69ed21b5-1289-400e-8e15-9782cd2a9401" />

---

# Part 2 — CSS Grid

## Task 2 — Page Layout

CSS Grid is used to create the main page structure.

The page is divided into two columns:

- Sidebar — 95px
- Main content — remaining available space

```css
.page-layout {
    display: grid;
    grid-template-columns: 95px 1fr;
}
```

The sidebar is positioned on the left side while the main website content is displayed on the right.

The sidebar also uses:

```css
position: sticky;
```

This allows the navigation menu to remain visible while the user scrolls through the website.

The header is located at the top of the website and the footer is located at the bottom.

### Screenshot

<img width="3072" height="602" alt="image" src="https://github.com/user-attachments/assets/1a0efd65-851f-449e-bdeb-eaffaa0769f2" />

<img width="3070" height="394" alt="image" src="https://github.com/user-attachments/assets/792b636b-0b26-4930-b288-ef9f7f1ebd67" />

---

## Task 3 — Image Gallery

The website contains a **Featured Builds Gallery** with nine bicycle images.

CSS Grid is used to organize the gallery into three equal columns:

```css
.gallery-images {
    display: grid;
    grid-template-columns: repeat(3, 400px);
    justify-content: center;
    gap: 30px;
}
```

The gallery contains three columns and uses a consistent `30px` gap between images.

Each gallery image uses:

```css
object-fit: cover;
```

This allows all gallery images to have the same dimensions without stretching the original image.

Each image also includes a caption overlay.

Normally, the caption is hidden:

```css
.image-caption {
    opacity: 0;
    transition: opacity 0.3s ease;
}
```

When the user moves the cursor over an image, the image becomes darker and slightly larger:

```css
.gallery img:hover {
    transform: scale(1.05);
    filter: brightness(40%);
}
```

At the same time, the image caption becomes visible:

```css
.gallery-item:hover .image-caption {
    opacity: 1;
}
```

This creates an interactive gallery with smooth CSS transitions.

### Screenshot

<img width="2782" height="1436" alt="image" src="https://github.com/user-attachments/assets/a49720fc-27f6-4db1-ac10-087add968735" />

---

# Part 3 — Combining Flexbox & Grid

## Task 4 — Combined Layout

The Azeke Industries website combines **Flexbox and CSS Grid** in the same interface.

### Flexbox

Flexbox is used for:

- Header navigation
- Logo and website name
- Product card rows
- Brand logos
- Footer

For example:

```css
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
```

and:

```css
.product-list {
    display: flex;
    justify-content: space-evenly;
    align-items: stretch;
    gap: 20px;
}
```

### CSS Grid

CSS Grid is used for the main page structure:

```css
.page-layout {
    display: grid;
    grid-template-columns: 95px 1fr;
}
```

It is also used for the image gallery:

```css
.gallery-images {
    display: grid;
    grid-template-columns: repeat(3, 400px);
    gap: 30px;
}
```

Using both technologies makes it possible to create a structured page while keeping individual components flexible and properly aligned.

### Screenshot

![Flexbox and Grid](screenshots/task4.png)

---

# Additional Features

## Smooth Scrolling

The website uses smooth scrolling:

```css
html {
    scroll-behavior: smooth;
}
```

Navigation links use section IDs such as:

```html
<a href="#introduction">Home</a>
<a href="#gallery">Gallery</a>
<a href="#about">About</a>
```

This allows users to navigate between sections without loading another page.

---

## Sticky Navigation

Both the header and sidebar remain accessible while navigating through the website.

The header uses:

```css
position: sticky;
top: 0;
```

The sidebar also uses sticky positioning to stay visible next to the main content.

---

## Brand Section

The introduction section contains logos from several bicycle brands.

Flexbox is used to distribute the logos:

```css
.brands {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    flex-wrap: wrap;
    gap: 30px;
}
```

The logos also have a hover animation.

---

## About Section

The About section provides information about Azeke Industries, its products, mission, brands, customer service, and contact information.

It gives the website the appearance and structure of a complete bicycle store website.

---

# Technologies Used

- HTML5
- CSS3
- Flexbox
- CSS Grid
- CSS Transitions
- CSS Transform
- Sticky Positioning
- Smooth Scrolling

No external CSS frameworks were used.

---

# Project Structure

```text
project/
│
├── index.html
├── style.css
├── logo.jpg
├── introbg.jpg
│
├── 1.jpg
├── 2.jpg
├── 3.jpg
├── 4.jpg
├── 5.jpg
├── 6.jpg
├── 7.jpg
├── 8.jpg
├── 9.jpg
│
├── vigor.webp
├── vigob.webp
├── cost1.webp
├── cost2.webp
├── cost3.webp
├── disp1.webp
├── disp2.webp
├── disp3.webp
```

---

# Work Process

First, I created the basic HTML structure of the website and added the header, sidebar, main content, and footer.

After that, I used Flexbox to create the navigation bar and organize the product cards and brand logos.

CSS Grid was used to create the main page layout and the three-column image gallery.

I then added hover effects, transitions, sticky navigation, smooth scrolling, product buttons, image captions, and an About section.

Finally, I adjusted the spacing, image sizes, colors, and alignment to make the website more consistent and user-friendly.

---

# Conclusion

This assignment helped me practice the differences between **Flexbox and CSS Grid**.

Flexbox was useful for arranging elements in rows and controlling alignment, while CSS Grid was useful for creating larger page layouts and the image gallery.

By combining both techniques, I created a structured bicycle store website with navigation, products, gallery images, hover effects, and responsive layout components.

---

© 2026 Azeke Industries
