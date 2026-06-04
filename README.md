AutoPalette String Art Generator — User Guide
What This App Is
The AutoPalette String Art Generator is an offline HTML app that converts a photo or image into a set of string-art instructions. It is designed for making physical string art using pins or nails placed around a circle, square, or rectangle.
The app analyzes your uploaded image, places virtual pins around the chosen canvas shape, and calculates thousands of pin-to-pin thread paths. These paths are grouped by thread color so you can build the design physically, one color pass at a time.
The app runs directly in your browser. It does not require an internet connection once the HTML file is opened.
What the App Does
This app lets you:
• Upload a photo.
• Choose a canvas shape: circle, square, or rectangle.
• Set the number of pins.
• Set the total number of string lines.
• Choose a background canvas color.
• Use a default KYRGB + black refinement + white highlight palette.
• Automatically create a palette from the uploaded image.
• Edit thread colors, opacity, and line weights.
• Generate a string-art rendering.
• Export written pin-to-pin instructions as a TXT file.
• Export the finished thread layout as an SVG file.
• Copy the instructions to your clipboard.
Basic Workflow
Use the app in this order:
• Choose your canvas shape.
• Set the canvas size.
• Set the number of pins.
• Upload your image.
• Drag or pinch the image to frame it.
• Tap Set Image.
• Adjust or auto-generate the thread palette.
• Tap Generate.
• Export the TXT instructions or SVG file.
Main Controls
Upload Image Button
The camera button opens your device’s image picker.
Use this to choose the photo you want to convert into string art. Portraits, high-contrast images, and clear subject photos usually work best.
After uploading, a small thumbnail appears under the controls.
Copy Button
The clipboard button copies the generated pin-to-pin instructions.
Use this after generation is complete. If no instructions exist yet, the app will tell you there is nothing to copy.
Pins
The Pins box controls how many pins are placed around the canvas.
Default: 400
More pins allow finer detail, but they also make the project harder to build physically. Fewer pins are easier to build but give less detail.
Suggested ranges:
• Simple designs: 100–200 pins
• Portraits: 300–500 pins
• High-detail work: 600+ pins
Lines
The Lines box controls the total number of thread lines the app will calculate.
Default: 12000
More lines usually create more detail and stronger shading, but they also make the physical build take much longer.
Suggested ranges:
• Quick test: 500–1500 lines
• Basic art: 3000–6000 lines
• Detailed portrait: 8000–15000 lines
• Very dense art: 20000+ lines
Canvas Shape
The app supports three canvas shapes:
Circle
Pins are placed evenly around a circular border.
Pin 0 is located at the very top of the circle, like the 12 o’clock position on a clock. Pin numbers then continue clockwise around the circle.
Use this shape for traditional round string-art portraits.
Square
Pins are placed evenly around the outside edge of a square.
Pin 0 begins near the top-left area of the square border. Pins continue along the top edge, then down the right edge, then across the bottom edge, then up the left edge.
Use this shape for framed square artwork.
Rectangle
Pins are placed evenly around the full rectangular perimeter.
Pin 0 begins near the top-left corner. Pins continue across the top edge, down the right side, across the bottom edge, and up the left side.
Use this shape for portrait-format or landscape-format string art.
Width and Height
These boxes set the virtual canvas size.
For circles and squares, the app forces the width and height to match. It uses the smaller of the two dimensions.
For rectangles, width and height can be different.
Example:
• 480 × 720 creates a tall portrait rectangle.
• 720 × 480 creates a wide landscape rectangle.
• 600 × 600 creates a square or circular canvas.
Pin Spacing Information
When Rectangle is selected, the app shows a pin spacing box.
This box tells you:
• Canvas width
• Canvas height
• Total pin count
• Perimeter
• Approximate distance between pins
• Approximate pins per side
• Exact side ratios
The app calculates rectangular spacing like this:
Pin spacing = total perimeter ÷ total pins
For a rectangle:
Perimeter = 2 × (width + height)
Example:
If the canvas is 480 × 720 and uses 400 pins:
Perimeter = 2 × (480 + 720)
Perimeter = 2400 units
Pin spacing = 2400 ÷ 400
Pin spacing = 6 units between pins
Longer sides automatically receive more pins than shorter sides because the pins are distributed evenly around the entire perimeter.
Background Canvas Color
This color picker sets the background color of the virtual canvas.
White is the default and is usually best for traditional string art.
Use black or dark backgrounds only if you are intentionally designing light-thread art.
Set Image
After uploading and positioning your image, tap Set Image.
This locks the currently visible image placement into the canvas.
You must tap Set Image before using:
• Generate
• AutoPalette From Image
If you change the image position but do not tap Set Image, the app will not use the new placement.
Generate
The Generate button starts the string-art calculation.
The app will:
• Build the pins.
• Build a cache of possible pin-to-pin lines.
• Compare possible string lines against the image.
• Choose lines that reduce the difference between the current canvas and the target image.
• Run each color pass according to the palette.
• Display the finished result.
• Create the pin-to-pin instructions.
The progress bar updates after each thread color pass.
Generation may take time, especially with high pin counts and high line counts.
Reset
The Reset button clears the current project.
It removes:
• Uploaded image
• Locked image data
• Generated line data
• Instructions
• Progress bar
• Thumbnail
• Current pins and line cache
It keeps the current canvas shape, size, background color, and palette settings.
Export TXT
This downloads the generated instructions as a text file.
The TXT file contains each color pass with pin-to-pin steps, such as:
BLACK FOUNDATION
0 -> 184
184 -> 72
72 -> 301
You can use this file as your physical build guide.
Export SVG
This downloads a vector SVG file of the generated string lines.
The SVG includes:
• Background color
• Canvas shape clipping
• Separate line groups for each thread color
• Actual generated pin-to-pin line positions
Use the SVG for previewing, printing, scaling, or editing in vector software.
You must generate the string art before exporting SVG.
Thread Palette
The Thread Palette controls which thread colors are used and how strongly each color affects the image.
Each palette row has:
• Color picker
• Name
• Weight
• Opacity
• Delete button
Color Picker
This sets the actual thread color.
Choose colors that match thread you can physically buy.
Name
This names the color pass.
The name appears in the instruction output.
Example:
BLACK FOUNDATION
YELLOW
RED
GREEN
BLUE
BLACK REFINEMENT
WHITE HIGHLIGHT
Weight
Weight controls how many lines that color receives.
Higher weight means more lines for that color.
For example, if black has a high weight, the app will assign more of the total line count to black.
Use higher weights for important colors and lower weights for accent colors.
Opacity
Opacity controls how strongly each string line affects the preview and SVG.
Higher opacity creates darker or stronger lines.
Lower opacity creates softer, more transparent thread effects.
For physical string art, opacity should usually stay fairly low because real thread builds up gradually.
Default Palette
The default palette is:
• Black Foundation
• Yellow
• Red
• Green
• Blue
• Black Refinement
• White Highlight
This is a KYRGB + K2 + White system.
Black Foundation builds the main shadows and structure.
Yellow, Red, Green, and Blue add color information.
Black Refinement strengthens final dark detail.
White Highlight adds light detail in bright areas.
AutoPalette From Image
The AutoPalette From Image button analyzes your locked image and chooses several dominant colors.
You must upload and set the image first.
AutoPalette creates:
• Black Foundation
• Several automatic image colors
• Black Refinement
• White Highlight
Use this when you want the thread colors to match the uploaded image more closely.
If the image does not contain enough distinct colors, AutoPalette may warn you that it could not find enough colors.
Add Color
This adds a new custom thread color to the palette.
Use this if you want to include a specific thread color, such as brown, orange, purple, tan, gray, or skin tone.
Delete Color
The red × button removes a color from the palette.
The app requires at least one color to remain.
How Pins Are Numbered
Circle Pin Numbering
For a circular canvas:
• Pin 0 is at the top center.
• Pins continue clockwise.
• The final pin is just before returning to the top.
Think of the circle like a clock:
• Top = Pin 0
• Right side = about one-quarter of the pin count
• Bottom = about one-half of the pin count
• Left side = about three-quarters of the pin count
Square and Rectangle Pin Numbering
For square and rectangle canvases:
• Pin 0 starts near the top-left corner.
• Pins move across the top edge first.
• Then they move down the right edge.
• Then across the bottom edge.
• Then up the left edge.
This means the build path follows the perimeter clockwise.
How to Build the Physical String Art
• Build your frame or canvas.
• Place pins or nails evenly around the chosen shape.
• Number the pins according to the app’s layout.
• Open the generated instructions.
• Start with the first color pass.
• Tie the thread to the first listed pin.
• Follow each instruction in order.
• When that color pass ends, tie off the thread.
• Move to the next color pass.
• Repeat until all color passes are complete.
Example instruction:
184 -> 72
This means:
Run the current thread color from pin 184 to pin 72.
Tips for Better Results
Use a clear, high-contrast image.
Portraits usually work better when the face is centered.
Avoid cluttered backgrounds.
Use more pins for better detail.
Use more lines for smoother shading.
Start with a test using fewer lines before running a huge project.
Use white or light background color unless your project specifically needs a dark canvas.
Do not set opacity too high, or the preview and SVG may become too heavy and dark.
Use AutoPalette only after setting the image.
Recommended Starting Settings
For a portrait rectangle:
• Shape: Rectangle
• Size: 480 × 720
• Pins: 400
• Lines: 12000
• Background: White
• Palette: Default or AutoPalette
• Image: Centered face, cropped close
For a round portrait:
• Shape: Circle
• Size: 600 × 600
• Pins: 300–500
• Lines: 8000–15000
• Background: White
For testing:
• Pins: 150–250
• Lines: 1000–3000
Important Notes
This app creates a simulation and instruction plan. Real thread, nail spacing, thread thickness, tension, lighting, and physical materials will affect the final result.
The SVG is a visual guide, but the TXT instructions are the main build guide.
Very high pin counts and line counts may slow down phones or older devices.
If the app feels slow, reduce either the pin count or the line count.
Summary
The AutoPalette String Art Generator is a browser-based tool for turning an image into buildable string art. It lets you choose the canvas shape, pin count, line count, background color, and thread palette. It can automatically extract colors from the image, generate pin-to-pin instructions, and export both TXT and SVG files.
Use it to design circular, square, or rectangular string art projects that can be physically built with nails, pins, and colored thread.
