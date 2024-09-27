## Working with Elastic Search

### Overview

This project is a **San Francisco App Scan Tracker**, which allows users to track and analyze business scans within the San Francisco area. The app provides the ability to search for businesses based on free text (like business names or keywords such as "burger") and filter by zip codes. It visualizes businesses on a map and lists the scanned user information for selected businesses.

This tool integrates multiple technologies to provide real-time tracking and visualization of business activity and user scans. It helps to monitor business performance and user interactions with businesses in a specific region.

### Features

1. **Free Text Search**:
   - Users can search for businesses using keywords (e.g., burger).
   
2. **Business ID and Device ID Search**:
   - You can search businesses by their Business ID.
   - You can search user data by Device ID to track individual scan history.

3. **Visualization**:
   - Maps businesses using OpenStreetMap for a visual understanding of the geographical spread.
   - Pins for each business appear on the map with business details.

4. **User Scans Data**:
   - Displays a table of user scan activity at a particular business, including timestamps, device IDs, and user information (name, birthdate).
   - You can view scan histories for individual users as well.

### Technology Stack

- **Yelp API**: For business search and information.
- **Elasticsearch**: For indexing and efficient searching through business and user scan data.
- **Streamlit**: A Python-based app framework used to create the web application interface.
- **Chrome Browser**: Utilized for rendering web pages and interactive maps.
- **OpenStreetMap**: For map visualizations that display businesses and scans on the interface.

### How It Works

1. **Search Business**:
   - Enter a business keyword in the "Free Text Search" input, and it will return businesses matching that keyword in San Francisco.

2. **Map Visualization**:
   - Results are plotted on an interactive map, making it easy to see where businesses are located.
   
3. **Business ID and User Scan Search**:
   - Input a **Business ID** or **Device ID** to search for user scan activity or business details respectively.

4. **Scan History**:
   - The system tracks and displays scan history of users who visited specific businesses. You can view the scan timestamps, associated device IDs, and user details.

### Setup Instructions

1. Clone the repository:
   ```bash
   git clone <repository-link>
   ```

2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up environment variables for Yelp and Elasticsearch:
   - Set your `YELP_API_KEY` and Elasticsearch credentials in your environment or `.env` file.

4. **Build and Run Containers**:
   Run the following command to build the images and start the services:
   ```bash
   docker-compose up --build
   ```

5. **Access the App**:
   Once the build process is complete, you can access the Streamlit app in your browser at `http://localhost:8501`.

6. **Stop the Containers**:
   To stop the running containers, use:
   ```bash
   docker-compose down
   ```

### Future Improvements

- **Real-Time Updates**: Implement real-time scan tracking.
- **Enhanced Filtering**: Add more filtering options like business category, ratings, etc.
- **User Profiles**: Build detailed profiles of users to track their interactions with multiple businesses over time.
