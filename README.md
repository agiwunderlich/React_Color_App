# Color Palette Compiling Application // created with React

The "React_Color_App" is a React application that provides a responsive and interactive user interface, with features such as creating new palettes, viewing individual palettes, selecting specific colors, and smooth transitions between different routes. </br> </br>
Colors can be pinned on the palette with HEX, RGB or RGBA codes. </br> 
Saturation level can be changed, a selected emoji can be used to save the finished palette. </br>
Palettes can be deleted from the main board.

![image](https://user-images.githubusercontent.com/35004717/138964904-feda884d-19d3-4a82-9100-982d539bdbe9.png)


![image](https://user-images.githubusercontent.com/35004717/138964835-f1089fe8-344a-4423-806d-453d0c880382.png)

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

## App Overview

The App component is a class-based component that serves as the main entry point of the application. 
It sets up the routing and handles the state management for the application, allowing users to create, view, and delete color palettes.

+ It initializes the state with the palettes array, which is either loaded from local storage or set to the default seedColors if no saved palettes are found.
+ The savePalette method is responsible for adding a new palette to the state and synchronizing the state with local storage.
+ The findPalette method finds a palette in the palettes array based on the provided id.
+ The deletePalette method removes a palette from the state by filtering out the palette with the specified id. 
+ It also synchronizes the state with local storage. The syncLocalStorage method saves the palettes array to local storage.

+ The render method renders the application's components based on the current route using react-router-dom.
+ The TransitionGroup and CSSTransition components from react-transition-group provide smooth transitions between different routes.
+ Inside the Switch component, different Route components are defined for different paths. Each Route specifies the component to render and provides necessary props to the components.
  + The PaletteList component is rendered on the root path ("/") and displays a list of palettes.
  + The NewPaletteForm component is rendered on the "/palette/new" path and allows users to create a new palette.
  + The Palette component is rendered on the "/palette/:id" path and displays a single palette based on the provided id.
  + The SingleColorPalette component is rendered on the "/palette/:paletteId/:colorId" path and shows a palette with a specific color selected. 
+ If none of the above routes match, the PaletteList component is rendered as a fallback.
