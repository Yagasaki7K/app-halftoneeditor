![image](https://github.com/user-attachments/assets/df8b39a5-1719-46d6-a29f-bc847949135b)

# Halftone Editor like a OpenAI

This project implements a **Halftone Image Processing Tool**. The tool allows users to upload images or videos, apply halftone effects, and export the results as PNG files. Here's a breakdown of its structure and functionality like a OpenAI.

---

## File Structure
- **HTML**: The interface layout and structure.
- **CSS**: Styling and responsive design.
- **JavaScript**: Dynamic functionalities like file uploads, processing, and exporting.

---

## HTML Structure

### Key Features:
1. **File Upload**:
   - Accepts both images and videos.
   - Allows drag-and-drop or click-to-upload functionality.

2. **Control Panel**:
   - Sliders for adjusting:
     - **Grid Size**: Defines the resolution of the halftone grid.
     - **Brightness, Contrast, Gamma, Smoothing**: Basic image adjustments.
   - Dropdown for **Dithering Options**:
     - Floyd-Steinberg, Ordered, Noise, or None.
   - Buttons to **Export PNG** or **Reset Adjustments**.

3. **Main Canvas**:
   - Displays the processed image or video.

---

## CSS Styling

### Key Design Choices:
1. **Responsive Design**:
   - The interface adjusts for desktop and mobile resolutions.
   - A flexible grid layout ensures usability on smaller devices.

2. **Custom Themes**:
   - Light and Dark Mode (based on user preferences).

3. **Interactive Elements**:
   - Buttons and sliders with hover and focus states.
   - Aesthetic panel design with shadows and rounded corners.

---

## JavaScript Logic

### Dynamic Functionalities:
1. **File Handling**:
   - Detects whether the uploaded file is an image or video.
   - Preloads the file and displays it on the canvas.

2. **Halftone Processing**:
   - Divides the image into a grid.
   - Converts each cell into a grayscale halftone dot based on brightness.

3. **Adjustments**:
   - Updates the grid size, brightness, contrast, gamma, and smoothing in real-time.
   - Allows dithering for additional effects.

4. **Performance Optimization**:
   - Uses **debouncing** to limit the frequency of updates during slider adjustments.
   - Implements efficient algorithms for dithering and smoothing.

5. **Export**:
   - Saves the processed image as a PNG.

6. **Reset**:
   - Resets all controls to default values.

---

## Features

### Halftone Generation:
- Converts full-resolution images into halftone representations.
- Adjustable dot size and density for artistic effects.

### Dithering Algorithms:
- **Floyd-Steinberg**: Smooth transitions between colors.
- **Ordered Dithering**: Creates patterns for a retro aesthetic.
- **Noise**: Adds random textures.

### Smoothing:
- Box Blur applied to grid cells for softer transitions.

---

## Key JavaScript Functions

### `generateHalftone(targetCanvas, scaleFactor)`
- **Inputs**: Canvas, scale factor.
- **Processes**:
  - Draws the uploaded image/video onto a temporary canvas.
  - Calculates grayscale brightness for each grid cell.
  - Draws halftone dots on the target canvas.

### `applyFloydSteinbergDithering(cellValues, numRows, numCols)`
- Applies error diffusion to enhance transitions in the halftone effect.

### `setupCanvasDimensions(width, height)`
- Dynamically adjusts the canvas size to fit within the viewport.

---

## Controls and UI Elements

| Control          | Description                                    |
|-------------------|------------------------------------------------|
| **Grid Size**     | Adjusts the density of the halftone pattern.   |
| **Brightness**    | Modifies overall brightness.                  |
| **Contrast**      | Adjusts contrast between light and dark areas.|
| **Gamma**         | Fine-tunes color intensity.                   |
| **Smoothing**     | Applies blur for softer edges.                |
| **Dither Type**   | Selects a dithering algorithm.                |
| **Export PNG**    | Saves the processed canvas as an image.       |
| **Reset All**     | Restores default settings.                    |

---

## Responsive Design

### Desktop:
- Sidebar and main canvas displayed side-by-side.

### Mobile:
- Stack layout for sidebar and canvas for better usability.

---

## Technologies Used

1. **HTML5 Canvas**: For rendering images and videos.
2. **CSS Variables**: Dynamic theming.
3. **JavaScript**: Handles all interactivity and processing.

---

