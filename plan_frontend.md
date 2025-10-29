# Frontend Sprint Plan

## Sprint Goal
Build and deploy a publicly available and responsive frontend for Tren's backend (server: https://hpc.psy.ntu.edu.tw:5000) using AJAX requests and modern CSS frameworks (TailwindCSS/Bootstrap). The frontend will be hosted for free using GitHub Pages.

---

## Objectives
1. **Frontend UI**  
   - Create a user-friendly and responsive design using **TailwindCSS** or **Bootstrap**.
   - Include the following sections:
     - Search interface for terms and logical queries.
     - Results display for the API responses.
     - Error handling for invalid or failed queries.
   - Ensure the frontend is visually appealing and intuitive.

2. **AJAX Functionality**  
   - Implement AJAX to fetch data from Tren's backend server:
     - `/terms`: Fetch and display all available terms.
     - `/terms/<term>`: Search and display terms associated with the input.
     - `/query/<query_string>/studies`: Perform logical searches and display study results.
   - Parse and display results dynamically on the page.
   - Add loading indicators while AJAX requests are in progress.

3. **Hosting with GitHub Pages**  
   - Set up a GitHub repository for the project.
   - Use GitHub Actions (if necessary for builds) and deploy the frontend to GitHub Pages.

4. **Testing & Debugging**  
   - Verify API integration works with different endpoints and query examples.
   - Test responsiveness across common screen sizes.
   - Ensure error-free deployment and proper handling of edge cases (e.g., missing data, invalid inputs).

---

## Tasks Breakdown  
### 1. Initial Setup
- [ ] Install and configure TailwindCSS/Bootstrap for styling.
- [ ] Set up a basic HTML layout and include necessary frameworks (JS libraries like jQuery or Fetch API for AJAX).

### 2. API Integration
- [ ] Check Tren's backend (server: https://hpc.psy.ntu.edu.tw:5000) function and data
- [ ] Connect to `/terms` endpoint and display results.
- [ ] Connect to `/terms/<term>` endpoint with user input and display associated terms.
- [ ] Connect to `/query/<query_string>/studies` endpoint with user queries and display logical search results.
- [ ] Implement proper error handling for API failures.

### 3. UI/UX Enhancements
- [ ] Style and organize results with TailwindCSS/Bootstrap.
- [ ] Add a search bar and input validation for queries.
- [ ] Show loading spinners or messages during data fetch.

### 4. Deployment
- [ ] Set up `index.html` as the entry point for GitHub Pages.
- [ ] Push code to the repository.
- [ ] Enable GitHub Pages under repository settings (use the main branch for hosting).
- [ ] Test the deployment link to ensure the website is live.

### 5. Testing & Final Touches
- [ ] Test endpoint functionality on various scenarios (e.g., valid inputs, empty inputs, edge cases).
- [ ] Ensure mobile responsiveness for smaller screens.
- [ ] Optimize the codebase and ensure good performance.

---

## Deliverables
- A fully functional frontend hosted on GitHub Pages.
- AJAX-enabled API integration with Tren's backend.
- Responsive design styled with TailwindCSS/Bootstrap.
- Publically accessible GitHub repository for the project.

---

## Notes
- Ensure all API endpoints are accessible and functioning correctly.
- Use tools like Postman or browser dev tools for troubleshooting API responses.
- If time permits, add additional features like more advanced search filters, or pagination for large datasets.