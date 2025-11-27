# Resume
This project is a responsive CV website built using HTML and CSS. It includes a left sidebar with a profile image container and a right section, which divided into 2 colums and 1 raw at the bottom for personal details, skills, education, and experience and contact deatails. The layout is lightweight, easy to edit, and works well on all screen sizes.

# Features
Left sidebar with a profile picture container
Clean and professional CV layout
Fully responsive design for mobile and desktop
Easy to customize text, colors, and structure

# Project_Structure
/
│── index.html          # Main HTML page
│── style.css           # CSS styles for all sections
│── /images             # Profile image & assets (optional)
│── README.md           # Documentation

# How It Works
# index.html
Builds the page structure
Contains the image container in the left sidebar as well as expertise, reference, eduaction & certification column *goup1*
Right section/colum holds experience, awards, & interest column *group-2*
The bottom raw contains contact information, and the social details raw *group3*

# style.css
Controls the layout of the project
Styles the sidebar and content area
Adds spacing, typography, and responsive behavior

# structual Layout based on group Format
# .group-1,
# .group-2 {
	display: flex;
	flex-direction: column;
	gap: 5rem;
}
.group-1 and .group-2 are flex containers.
flex-direction: column; → Items inside are arranged vertically.
gap: 5rem; → Adds 5rem space between the child elements.

# .group-3 {
	max-width: 700px;
	width: 100%;
	margin: 0 auto;
	grid-column: 1/-1;
	display: flex;
	flex-direction: row;
	gap: 5rem;
}
# Explanation
max-width: 700px; - Limits the container to 700px wide.
width: 100%; - Expands to full width of parent container (up to 700px).
margin: 0 auto; - Centers the container horizontally.
grid-column: 1/-1; - Suggests .group-3 is inside a CSS Grid container and spans all columns.
display: flex; - Makes .group-3 a flex container
flex-direction: row; - Items inside are arranged horizontally.
gap: 5rem; - Horizontal spacing of 5rem between items.

# Children of Group 3
.group-3 > div {
	flex: 1;
}
# Explanation:
Targets direct child <div> elements of .group-3.
flex: 1; → Each child takes equal horizontal space, sharing the container evenly.

# Overall Layout Interpretation
.group-1 - Left column content (stacked vertically).
.group-2 - Right column content (stacked vertically).
.group-3 - Bottom row content (horizontal, equal widths).
gap ensures spacing is consistent and flexible.
grid-column: 1/-1 only works if parent is a CSS grid; otherwise it does nothing.


# Google Fonts Import (Inter by Rasmus Andersson)
This project uses the Inter font designed by Rasmus Andersson, imported directly into the CSS file using the @import rule.
# Font Import (CSS)
Added at the very top of the style.css file:
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@200;300;400;500;600;700&display=swap');

# Applying the Font
The imported font is applied globally:
body {
    font-family: 'Inter', sans-serif;
}

# Icons Using Feather_Icons
Feather Icons is a lightweight, open-source icon library that provides beautiful, scalable SVG icons.
How to use it
Step 1: Include the script in your HTML <head> or just before </body>
<script src="https://unpkg.com/feather-icons"></script>

# Step 2: Add icon placeholders in your HTML
<i data-feather="user"></i>
<i data-feather="mail"></i>
<i data-feather="msg"></i>

# Step 3: Initialize the icons
<script>
feather.replace(); // This replaces all placeholders with SVG icons
</script>
It's placed at the bottom of the html before the </body> closing tag






