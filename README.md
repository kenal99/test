# Organizational Hierarchy Visualization

This project is a Vue 3-based web application that visualizes an organization's hierarchy using D3.js. The hierarchy is represented in a tree structure, where each node shows essential employee information such as name, job title, department, location, and cost data.

## Features

- **Interactive Organization Chart**: The application displays an interactive organization hierarchy with collapsible nodes.
- **Dynamic Data**: Hierarchy data is loaded from a CSV file and dynamically rendered.
- **Responsive Layout**: The layout adjusts according to window resizing.
- **Employee Information**: Each node displays details such as employee name, job title, department, location, and various cost metrics.
- **Expand/Collapse Functionality**: Nodes can be expanded or collapsed to show or hide descendant information.
- **Cost Breakdown**: Management and IC (individual contributor) cost, total cost, and management cost ratio are displayed for each node.
- **Decendants Button**: Shows Decendants info in format - [Children Count] / [Non-Leaf Decendants Count] / [Decendants Count]

## Tech Stack

- **Vue 3**: Frontend framework for building user interfaces.
- **D3.js**: A JavaScript library for producing dynamic, interactive data visualizations in web browsers.
- **Tailwind CSS**: A utility-first CSS framework for styling the UI components.

The app will be accessible at `http://localhost:5173/`.

## Project Structure

- `src/`: Contains all source code for the app.
  - `components/`: Vue components, including the org chart and employee node.
  - `utils/`: Utility functions for processing hierarchy data.
  - `public/`: Contains static files, including the `Data.csv` file with people data.
- `App.vue`: The main Vue component that renders the org chart.

## How it Works

1. **Data Loading**: The app loads a CSV file from the `/public` directory using D3's CSV parsing functionality.
2. **Hierarchy Processing**: The data is transformed into a hierarchical structure using D3's `hierarchy` method.
3. **Chart Rendering**: D3 is used to render the hierarchical tree, where each node is an employee.
4. **Employee Nodes**: Each node contains an avatar (initials), name, job title, department, location, cost information and decendants information.
5. **Cost Formatting**: The cost information is formatted in 'K' (thousands) or 'M' (millions) format, depending on the value.

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```
