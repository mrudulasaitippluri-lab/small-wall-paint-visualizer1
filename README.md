# HueRoom – Smart Wall Paint Visualizer

## 1. Abstract

HueRoom is a web-based Smart Wall Paint Visualizer that helps users preview different paint colours on their room walls before actually painting them. Users can upload a photograph of their room, select a specific wall area, and apply different colours to see how the room may look after painting.

The main purpose of this project is to make colour selection easier, save time, and help users make better interior-design decisions. The application can also be extended with a paint product catalogue, price details, room inspiration, and a paint cost calculator.

## 2. Introduction

Painting is an important part of home decoration. However, selecting the right wall colour can be difficult because people cannot always imagine how a particular shade will look in their room.

HueRoom provides a digital solution by allowing users to upload their room images and experiment with different paint colours. Users can compare colour combinations before purchasing paint or starting painting work.

The project combines web development and image visualization to provide an interactive and user-friendly experience.

## 3. Problem Statement

Traditional paint selection methods require customers to depend on colour cards, small samples, or their imagination. Testing several colours physically can consume time and money.

Therefore, a system is needed that allows users to preview different paint colours on their actual room photographs before making a final decision.

HueRoom aims to solve this problem through an interactive web-based colour visualization platform.

## 4. Objectives

- To develop a user-friendly wall paint visualization application.
- To allow users to upload room photographs.
- To provide tools for selecting specific wall areas.
- To apply different colours to selected wall regions.
- To help users compare different paint shades.
- To provide options to save or download designs where implemented.
- To provide a foundation for integrating paint products and pricing information.
- To make interior colour selection easier and more convenient.

## 5. Existing System

In the existing traditional system, users select paint colours using physical colour cards, sample paints, or photographs from the internet.

### Disadvantages
- Users may find it difficult to imagine the final appearance.
- Physical sample testing can take additional time.
- Comparing many shades can be inconvenient.
- The selected colour may look different under room lighting.
- Users may need assistance from painters or interior designers.

## 6. Proposed System

HueRoom provides an interactive platform where users can upload a room image and preview different colours on selected walls.

### Advantages
- Easy visualization of wall colours.
- Convenient comparison of different shades.
- Reduced dependence on physical colour samples.
- Better support for interior-design decisions.
- Interactive and visually attractive interface.
- Potential integration with paint products and online shopping.

## 7. Technologies Used

The proposed application uses the MEAN stack.

### Frontend
**Angular:** Used to create the user interface, upload controls, colour selection tools, and visualization components.

**HTML and CSS:** Used to structure and style the application.

**TypeScript and JavaScript:** Used to implement interactive functionality and application logic.

### Backend
**Node.js:** Provides the JavaScript runtime for server-side operations.

**Express.js:** Handles backend routes, API requests, and application logic.

### Database
**MongoDB:** Can store user information, paint product details, and saved project metadata when database functionality is implemented.

### Other Technologies
**Canvas or image-processing APIs:** Can support wall selection and colour-preview functionality.

**JWT:** Can provide authentication if user login and registration are implemented.

The final technology list should match the technologies actually used in the source code.

## 8. System Architecture

The application can be divided into three layers.

### 8.1 Presentation Layer
The Angular frontend allows users to interact with the application, upload images, select walls, choose colours, and view previews.

### 8.2 Application Layer
The Node.js and Express.js backend can process API requests, manage authentication, retrieve product information, and handle saved projects.

### 8.3 Database Layer
MongoDB can store user records, paint catalogue information, and saved-project metadata.

### Architecture Flow

User → Angular Interface → Image Upload → Wall Selection → Colour Application → Room Preview

For features requiring persistent storage:

Angular Interface → Express.js API → Node.js → MongoDB

## 9. Main Modules

### 9.1 Home Page
The home page introduces HueRoom and provides navigation to the visualizer and other available sections.

### 9.2 Image Upload Module
Users can upload a photograph of their room from their device. The application displays the uploaded image for visualization.

Supported image formats may include JPG, JPEG, and PNG, depending on the implementation.

### 9.3 Wall Selection Module
Users select the wall area they want to recolour. Depending on the available implementation, selection may be performed using a brush, polygon, or similar manual tool.

Accurate selection helps the application apply the paint effect to the intended wall area.

### 9.4 Colour Selection Module
Users select a colour from the available palette or colour picker. Different shades can be tested to find a suitable colour combination.

### 9.5 Paint Visualization Module
The selected colour is applied to the selected wall region to generate a room preview. An opacity adjustment can help retain some original wall texture and lighting.

### 9.6 Save and Download Module
Where implemented, users can save their design or download the resulting preview for future reference.

### 9.7 Paint Catalogue Module
A possible extension is a catalogue containing paint shade names, colour codes, finishes, coverage, prices, and ratings.

### 9.8 User Authentication Module
If implemented, users can register and log in to access personal features and saved projects.

## 10. System Requirements

### Hardware Requirements
- Computer or laptop.
- Minimum 4 GB RAM recommended.
- Sufficient storage for source code and room images.
- Internet connection for online services and package installation.

### Software Requirements
- Windows, Linux, or macOS.
- Modern web browser such as Google Chrome.
- Node.js and npm for a MEAN application.
- Angular CLI if used by the project.
- MongoDB if database integration is enabled.
- Code editor such as Visual Studio Code.

## 11. Functional Requirements

1. The application should display the home page.
2. Users should be able to open the room visualizer.
3. Users should be able to upload a supported room image.
4. The uploaded image should be displayed.
5. Users should be able to select the required wall region.
6. Users should be able to choose a paint colour.
7. The preview should update when the selected colour changes.
8. The application should provide feedback for invalid uploads.
9. Users should be able to save or download designs if those features are implemented.
10. Authentication and database features should work correctly if included.

## 12. Non-Functional Requirements

**Usability:** The application should be easy to understand and operate.

**Performance:** Image previews and colour changes should respond promptly.

**Reliability:** The application should handle invalid inputs and unexpected errors.

**Security:** User data and backend APIs should be protected.

**Compatibility:** The interface should work in modern browsers.

**Maintainability:** The code should be organized into reusable components and modules.

**Responsiveness:** The interface should adapt to different screen sizes where supported.

## 13. Database Design

The following are proposed MongoDB collections for a version that includes the corresponding features.

### Users Collection
- User ID
- Name
- Email
- Password hash
- Role
- Created date

### Paint Products Collection
- Product ID
- Shade name
- Hex colour code
- Finish type
- Coverage
- Price in INR
- Category
- Product image URL

### Saved Projects Collection
- Project ID
- User ID, if accounts are enabled
- Project name
- Image reference
- Wall selection coordinates
- Selected colour
- Created date
- Updated date

These collections should be created only as required by the implemented application.

## 14. Algorithm and Working Procedure

1. Start the HueRoom web application.
2. Display the home page.
3. Open the visualizer.
4. Select and upload a room photograph.
5. Display the uploaded image.
6. Select the wall area using the available selection tools.
7. Choose a colour from the colour palette.
8. Apply the selected colour to the wall region.
9. Display the updated room preview.
10. Repeat the process to compare different colours.
11. Save or download the preview if the feature is available.
12. End the process.

## 15. Testing

| Test Case | Expected Result |
|---|---|
| Open the application | Home page displays correctly |
| Upload a valid image | Image appears in the visualizer |
| Upload an unsupported file | Error message is displayed |
| Select a wall region | Selected region is identified |
| Choose a different colour | Preview updates |
| Change opacity | Paint effect changes |
| Upload another image | New image is displayed |
| Download the preview | Image downloads if the feature is implemented |
| Test on a mobile-sized screen | Interface remains usable where responsive support exists |

Actual test results should be recorded after testing the application.

## 16. Advantages

- Makes wall colour selection easier.
- Provides a visual preview before painting.
- Allows comparison of different colour options.
- Can reduce unnecessary physical sample testing.
- Provides an interactive user experience.
- Can be extended with paint product information.
- Supports creative interior-design experimentation.

## 17. Limitations

- The quality of the preview depends on the uploaded image.
- Manual wall selection may require careful tracing.
- Shadows and lighting can affect the preview.
- Screen colours may not exactly match actual paint.
- Authentication, database storage, and product features require additional implementation if they are not already available.

## 18. Future Enhancements

- Automatic wall detection using artificial intelligence.
- More realistic lighting and wall-texture preservation.
- Multiple wall selections and colour combinations.
- Room inspiration gallery.
- Paint quantity and cost calculator.
- Paint product catalogue with maintained pricing.
- User accounts and cloud storage.
- Sharing and comparing saved room designs.
- Improved mobile experience.

## 19. Conclusion

HueRoom – Smart Wall Paint Visualizer is designed to make wall colour selection more convenient through interactive room-image previews. Users can upload room photographs, select wall areas, and explore different paint colours before making a final painting decision.

The application demonstrates how web technologies can be used to improve the interior-design experience. In the future, it can be expanded with automatic wall detection, secure user accounts, product catalogues, cost estimation, and persistent design storage.
