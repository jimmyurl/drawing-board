# drawing-board.
This is a simple web-based application using HTML, Vanilla Javascript and CSS styling that allows users to create drawings and sketches on a canvas using various tools and options. 

Here's an explanation of how the app works and its key features:

1. **Canvas**: The app provides a canvas element where users can draw. This canvas is essentially an HTML element that acts as a drawing surface.

2. **Tools**: Users can select different drawing tools from a set of options. The available tools in the app include:
   - **Brush**: This tool allows users to draw freehand lines or shapes using a brush-like stroke.
   - **Eraser**: The eraser tool acts like a brush but erases the content on the canvas.
   - **Rectangle**: Users can draw rectangles on the canvas.
   - **Circle**: This tool lets users draw circles.
   - **Triangle**: Users can draw triangles.
   - **Line**: For drawing a straight line.
   - **Random Draw**: For drawing irregular shapes.

3. **Options**: The app provides various options to customize the drawing experience. These options include:
   - **Brush Size**: Users can adjust the size of the brush or line they draw using a slider.
   - **Colors**: Users can select different colors for their drawings. The app offers a set of predefined colors and a color picker to choose any color.
   - **Fill Color**: Users can choose whether to fill shapes with color or just draw their outlines.

4. **Clear Canvas**: There's a button that allows users to clear the entire canvas, removing all drawings and starting fresh.

5. **Save as Image**: Another button lets users save their drawings as images, typically in JPEG format. This allows users to download and share their artwork.

6. **Random Drawing**: You wanted to add a feature for drawing random shapes. However, in the provided code, this feature is not fully implemented. It currently draws random polygons when you click the "Random Draw" button, but you can customize this function to draw any random shapes or figures you like.

7. **Event Listeners**: The app listens for user interactions like mouse clicks and movements. For example, when the mouse is clicked and dragged, it draws lines or shapes on the canvas based on the selected tool.

8. **Customization**: Users can customize their drawing experience by selecting different tools, brush sizes, and colors, making it versatile for various artistic creations.

9. **Save and Load**: Users can save their drawings as image files and load existing images into the canvas to edit or continue their work.

**script.js**

This script effectively manages the drawing app's functionality, enabling users to draw, customize their drawing experience, and interact with the canvas and user interface elements. Here's a breakdown of the key components and their functions:

1. **Canvas and Context Setup**:
   - `const canvas = document.querySelector("canvas")`: This line selects the HTML `<canvas>` element and assigns it to the `canvas` variable.
   - `const ctx = canvas.getContext("2d")`: It obtains a 2D rendering context for the canvas, allowing you to draw on it.

2. **User Interface Elements**:
   - Various `const` declarations select HTML elements by their IDs or classes to interact with them later. These include buttons, sliders, and color pickers, which are used for selecting tools, adjusting settings, and more.

3. **Global Variables**:
   - `let prevMouseX, prevMouseY, snapshot`: These variables store information about the previous mouse position and a snapshot of the canvas, allowing you to track and undo changes.
   - `let isDrawing = false`: This variable indicates whether the user is currently drawing on the canvas.
   - `let selectedTool = "brush"`: It stores the currently selected drawing tool, initially set to "brush."
   - `let brushWidth = 5`: This variable represents the brush size, initially set to 5 pixels.
   - `let selectedColor = "#000"`: It stores the currently selected drawing color, initially set to black.

4. **Canvas Initialization**:
   - `setCanvasBackground()`: This function sets the initial canvas background color to white and the brush color to the selected color.

5. **Window Load Event**:
   - `window.addEventListener("load", () => { ... })`: This event listener triggers when the page finishes loading. It initializes the canvas size and background.

6. **Drawing Functions**:
   - `drawRect(e)`, `drawCircle(e)`, `drawTriangle(e)`: These functions are responsible for drawing rectangles, circles, and triangles on the canvas based on user input.

7. **Start Drawing Function**:
   - `startDraw(e)`: This function is called when the user starts drawing. It sets up the drawing environment, such as brush size, color, and snapshot.

8. **Drawing Function**:
   - `drawing(e)`: This function handles the actual drawing process based on the selected tool. It checks if the user is currently drawing and updates the canvas accordingly.

9. **Event Listeners**:
   - Several event listeners are added to different elements:
     - Tool buttons: When a tool button is clicked, it updates the selected tool.
     - Brush size slider: Adjusts the brush size based on the slider value.
     - Color buttons: Change the selected drawing color.
     - Color picker: Allows users to pick a custom color.
     - Clear Canvas and Save Image buttons: Perform the respective actions.
     - Mouse events on the canvas: Handle the drawing process based on mouse interactions.

