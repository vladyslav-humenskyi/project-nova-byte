# WildSketch

WildSketch is a responsive one-page website developed as the final team project
for the **HTML & CSS** module of the GoIT course.

The project is based on a provided Figma design and focuses on semantic HTML5
markup, responsive design, modern CSS, optimized assets, and collaborative
development using Git and GitHub.

## Getting Started

### Prerequisites

Make sure you have the LTS version of [Node.js](https://nodejs.org/) installed.

### Installation

1. Clone the repository:

```bash
git clone <repository-url>
```

2. Navigate to the project directory:

```bash
cd project-NovaByte
```

3. Install the project dependencies:

```bash
npm install
```

### Development

Start the local development server:

```bash
npm run dev
```

Vite will provide the local development URL, usually:

```text
http://localhost:5173
```

The page will automatically reload when project files are changed.

### Production Build

Create a production build:

```bash
npm run build
```

## Design

[Figma mockup](https://www.figma.com/design/n9IyoxHkRQEIRHwdqlDPOf/Wild-Sketch?node-id=8202-63498&t=BGKz6hSkEhiYpOBi-0)

## Technologies

- HTML5
- CSS3
- Vite
- Git & GitHub
- modern-normalize
- Prettier

## Responsive Design

The website is developed using the **Mobile First** approach with `min-width`
media queries.

Breakpoints:

- **Mobile:** from `375px`
- **Tablet:** from `768px`
- **Desktop:** from `1440px`

The layout adapts to different screen sizes according to the provided design.

## Project Structure

The page consists of the following sections:

- Header
- Hero
- Benefits
- Gallery
- Events
- Team
- Feedbacks
- Register
- Footer
- Mobile menu

Each page section is implemented as a separate HTML partial and connected to the
main `index.html` file.

## Main Requirements

### General

- Semantic HTML5 markup
- Valid HTML and CSS
- Mobile First responsive design
- `modern-normalize` for consistent browser styling
- Google Fonts
- Source code formatted with Prettier
- Optimized raster and vector graphics
- Retina-ready raster images (`1x` and `2x`)
- Responsive content and background images
- SVG sprite for icons
- SVG logo
- Favicon from the UI Kit
- Hover effects for interactive elements according to the design
- Pointer cursor for clickable elements

### Header

The Header contains:

- SVG logo
- Site navigation
- Register link

Navigation is implemented using anchor links to the corresponding page sections.

### Hero

The Hero section contains:

- Main page heading: **“Unleash Your Creativity in Nature's Embrace”**
- Description
- Content image
- **Register** link leading to the Register section
- **Learn More** link leading to the Events section

### Benefits

The Benefits section contains:

- Heading: **“Reconnect with yourself through the art of outdoor drawing”**
- Content image
- List of three benefits

Each benefit contains:

- SVG icon
- Heading
- Description

### Gallery

The Gallery section contains:

- Heading: **“Artistic Showcase”**
- Description
- Seven artwork images

The gallery is implemented as a list using Flexbox. All images are implemented
as content images.

### Events

The Events section contains:

- Heading: **“Explore Our Upcoming Workshop Schedule”**
- Description
- List of upcoming workshop cards implemented using Flexbox

Each workshop card contains:

- Image
- Workshop title
- Location
- SVG location icon
- Link to the location on a map
- Date and time
- Register link leading to the Register section

### Team

The Team section contains:

- Heading: **“Our team”**
- Description
- List of artists

Each team member card contains:

- Photo
- Name
- Position

### Feedbacks

The Feedbacks section contains:

- Heading: **“Customer testimonials”**
- List of customer reviews

Each review contains:

- Rating represented by SVG icons
- Review text
- Author

### Register

The Register section contains:

- Heading: **“Register”**
- Content image
- Registration form

The form contains:

- Name field
- Email field
- Comment field
- Submit button

The name and email fields are required and use HTML validation.

Name validation:

```text
^[a-zA-Z\s\.]{5,64}$
```

Email validation:

```text
^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$
```

The comment field supports a maximum of **500 characters**.

### Footer

The Footer contains:

- SVG logo
- Anchor navigation links
- Consumer rights / copyright information

### Mobile Menu

The mobile menu:

- Contains the required navigation elements
- Matches the width defined in the design
- Occupies the full viewport height
- Is hidden by default
- Becomes visible when the `is-open` class is added

## File Structure

```text
src/
├── css/
│   └── ...
├── img/
│   └── ...
├── partials/
│   ├── header.html
│   ├── mobile-menu.html
│   ├── hero.html
│   ├── benefits.html
│   ├── gallery.html
│   ├── events.html
│   ├── team.html
│   ├── feedbacks.html
│   ├── register.html
│   └── footer.html
└── index.html
```

- HTML components are stored in `src/partials`.
- CSS files are stored in `src/css`.
- Images and graphical assets are stored in `src/img`.
- Static public assets such as the favicon can be stored in `public`.

## Code Quality

The project follows the recommendations of [Code Guide](https://codeguide.co/).

HTML can be validated using:

- [W3C Markup Validation Service](https://validator.w3.org/)

CSS can be validated using:

- [W3C CSS Validation Service](https://jigsaw.w3.org/css-validator/)

Source code is formatted using **Prettier**.

## Deployment

The production version of the project is automatically built and deployed to
**GitHub Pages** when changes are merged or pushed to the `main` branch.

The Vite build command in `package.json` must contain the correct repository
name:

```json
"build": "vite build --base=/project-NovaByte/"
```

Deployment is handled through GitHub Actions.

The deployment status can be checked in the repository's **Actions** section.

## Team Workflow

The project is developed collaboratively using Git and GitHub.

Each team member works on a separate feature branch and submits changes through
a pull request. Changes are reviewed before being merged into the `main` branch.

Recommended workflow:

```text
main
  ↑
Pull Request
  ↑
feature/<feature-name>
```

Examples of feature branches:

```text
feature/header
feature/hero
feature/benefits
feature/gallery
feature/events
feature/team
feature/feedbacks
feature/register
feature/footer
```

## Authors

Developed by the project team as part of the **GoIT HTML & CSS course**.
