

---

# 🚀 On-Demand Projects Showcase

Welcome to the **On-Demand Projects Showcase** — a responsive React application that categorizes and displays a curated collection of web development projects. Explore projects by category: Static, Responsive, or Dynamic.

## 🔗 Live Demo

<a href="https://ondemandnaga.ccbp.tech/" target="_blank">
  <img    src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExYmMwNjhtajFwNDdrbDNicXN5Y3Y3OGw5ZXZhMDhkemF4M2ZxdHZjNSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/mBRLcBE5qCbe1xvwQ3/giphy.gif" 
    alt="Visit On-Demand Projects Showcase" 
    width="300" 
    height="300"
  />
</a>

> Click the GIF above to launch the app!

---

## 🧠 Overview

This application allows users to:

- **Browse Projects**: View a list of projects categorized as Static, Responsive, or Dynamic.
- **Filter by Category**: Click on category tabs to filter projects accordingly.
- **View Project Details**: Each project displays an image, title, and description.

---

## 🛠️ Technologies Used

- **React**: JavaScript library for building user interfaces.
- **CSS**: Styling the components and layout.
- **JavaScript (ES6+)**: Logic and interactivity.

---

## 📂 Project Structure

- `App.js`: Main component managing state and rendering the application.
- `components/TabItem.js`: Renders individual category tabs.
- `components/ProjectItem.js`: Displays individual project details.
- `components/Header.js`: Navigation header with social media icons.

---

## 🔍 Code Explanation

### State Management

```javascript
state = {
  activeTabId: tabsList[0].tabId,
};
```

- Initializes the state with the first tab (Static) as active.

### Handling Tab Clicks

```javascript
clickTabItem = tabValue => {
  this.setState({ activeTabId: tabValue });
};
```

- Updates the active tab in the state when a tab is clicked.

### Filtering Projects

```javascript
getFilteredProjects = () => {
  const { activeTabId } = this.state;
  return projectsList.filter(
    project => project.category === activeTabId
  );
};
```

- Filters the `projectsList` based on the active category.

### Rendering Components

```javascript
<ul className="tabs-container">
  {tabsList.map(tab => (
    <TabItem
      key={tab.tabId}
      tabDetails={tab}
      clickTabItem={this.clickTabItem}
      isActive={activeTabId === tab.tabId}
    />
  ))}
</ul>

<ul className="project-list-container">
  {filteredProjects.map(project => (
    <ProjectItem
      key={project.projectId}
      projectDetails={project}
    />
  ))}
</ul>
```

- Renders the tabs and the filtered list of projects.

---

## 📸 Screenshot

![On-Demand Projects Showcase](https://user-images.githubusercontent.com/your-username/your-repo/your-screenshot.png)

---

## 📌 Getting Started

1. **Clone the repository**:

   ```bash
   git clone https://github.com/your-username/your-repo.git
   ```

2. **Navigate to the project directory**:

   ```bash
   cd your-repo
   ```

3. **Install dependencies**:

   ```bash
   npm install
   ```

4. **Start the development server**:

   ```bash
   npm start
   ```

5. **Open in browser**:

   Visit `http://localhost:3000` to view the application.

---

## 🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements.

---
