# Smart India Hackathon Workshop
# Date:27-10-2026
## Register Number: 212225040236
## Name: Mithun Kumar V
## Problem Title
SIH 1710: Enhancing Navigation for Railway Station Facilities and Locations
## Problem Description
Background: Railway stations are complex environments with numerous facilities and locations such as ticket counters, platforms, restrooms, food courts, and waiting areas. Passengers often face difficulties in navigating these spaces, especially in large or unfamiliar stations. Efficient and user-friendly navigation systems are crucial for improving passenger experience, reducing congestion, and ensuring timely travel connections. Description: The problem involves developing a comprehensive navigation solution for railway stations that assists passengers in locating various facilities and destinations within the station premises. This includes creating detailed maps, providing real-time directions, and integrating features such as accessibility options for individuals with disabilities. The solution should be intuitive, easy to use, and accessible via multiple platforms, including mobile devices and digital kiosks. Key challenges include updating navigation information in real-time, ensuring accuracy, and accommodating the diverse needs of all passengers. Expected Solution: The expected solution is a multi-platform navigation system that provides detailed, real-time directions to all facilities and locations within a railway station. This system should include: A mobile application with 3D interactive maps and step-by-step navigation. Digital kiosks located throughout the station with touch-screen interfaces. Voice-guided navigation for visually impaired passengers. Regular updates to reflect changes in station layout and facility locations. Integration with existing railway apps and services for seamless user experience. The solution should enhance the overall passenger experience by reducing confusion, saving time, and improving accessibility within the station.

## Problem Creater's Organization
Ministry of Railway
## 1. Idea

### RailNav AI – Smart Railway Station Indoor Navigation System

RailNav AI is a smart and accessible navigation system designed to help passengers find railway station facilities such as platforms, ticket counters, restrooms, food courts, waiting halls, lifts, and exits. The system provides interactive 2D and 3D station maps, shortest-path navigation, step-by-step directions, and voice assistance for visually impaired passengers. It uses QR codes to identify passenger locations and updates routes when paths are closed or facilities become unavailable. The system also includes wheelchair-accessible routes, multilingual support, digital kiosks, and an administration dashboard for railway staff. Its main objective is to reduce passenger confusion, save time, improve accessibility, and reduce congestion inside railway stations.

## 2. Proposed Solution / Architecture Diagram

RailNav AI consists of a passenger application, digital kiosk interface, navigation engine, backend server, database, and railway staff dashboard.

### System Architecture

```text
+--------------------------------------+
|          Passenger Interfaces        |
|  Mobile App | Web App | Digital Kiosk|
+------------------+-------------------+
                   |
                   v
+--------------------------------------+
|       Navigation Application        |
| Facility Search | QR Location        |
| Interactive Maps | Voice Guidance    |
+------------------+-------------------+
                   |
                   v
+--------------------------------------+
|       Routing and Accessibility      |
|       A* / Dijkstra Algorithm        |
| Wheelchair Routes | Closed-Path Avoid|
+------------------+-------------------+
                   |
                   v
+--------------------------------------+
|          Backend API Server          |
| Node.js | Express.js | Socket.IO     |
+------------------+-------------------+
                   |
                   v
+--------------------------------------+
|             Database                 |
| MongoDB: Maps, Facilities, Routes    |
| Accessibility Data and Updates       |
+--------------------------------------+
                   ^
                   |
+--------------------------------------+
|      Railway Staff Dashboard         |
| Update Maps | Manage Facilities      |
| Report Closures | Update Information |
+--------------------------------------+
```

### Working Process

1. The passenger opens the application or a digital kiosk.
2. The passenger scans a QR code or selects their current location.
3. The passenger searches for a destination, such as Platform 4 or the nearest restroom.
4. The navigation engine calculates the best route using the A* or Dijkstra algorithm.
5. The system displays the route on an interactive map and provides step-by-step voice or text directions.
6. Railway staff can update facility information, report closed paths, and mark unavailable lifts.
7. The system recalculates routes whenever relevant station information changes.

## 3. Use Cases

- **Platform Navigation:** Guide passengers from station entrances to their required platforms.
- **Facility Discovery:** Help passengers locate ticket counters, restrooms, drinking water, food stalls, waiting halls, lifts, and exits.
- **Accessible Navigation:** Provide wheelchair-friendly routes and voice assistance for visually impaired passengers.
- **QR-Based Indoor Positioning:** Identify passenger locations using QR codes installed at entrances and important junctions.
- **Dynamic Route Updates:** Recalculate routes when corridors are blocked or facilities become unavailable.
- **Digital Kiosk Navigation:** Allow passengers without smartphones to search for facilities and obtain directions.
- **Multilingual Assistance:** Provide navigation instructions in English, Hindi, Tamil, and other supported languages.
- **Staff Management:** Enable authorized railway staff to update maps, facilities, and temporary closures.
- **Train Connection Assistance:** Help passengers navigate to their assigned platforms using verified train information.
- **Emergency Route Support:** Display authorized alternative routes when paths are restricted or emergencies occur.

## 4. Technology Stack

| Technology Layer | Tools / Technologies | Purpose |
|---|---|---|
| User Interface | HTML, CSS, JavaScript | Create a responsive interface |
| Frontend Framework | React.js | Build interactive navigation screens |
| Map Visualization | MapLibre GL JS | Display interactive station maps |
| 3D Navigation | Three.js | Visualize station layouts in 3D |
| Backend Services | Node.js and Express.js | Handle requests and navigation services |
| Database | MongoDB | Store station facilities, locations, and map information |
| Pathfinding | A* Algorithm and Dijkstra's Algorithm | Calculate optimal routes |
| Indoor Positioning | QR Codes and Bluetooth Beacons | Identify passenger locations |
| Voice Assistance | Web Speech API | Provide spoken navigation instructions |
| Real-Time Communication | Socket.IO | Send live facility and route updates |
| Authentication | JSON Web Tokens (JWT) | Secure passenger and administrator access |
| Deployment | Vercel and Render | Host the application and backend |
| Version Control | Git and GitHub | Manage source code and collaboration |

## 5. Dependencies

### Frontend Dependencies

- **React.js:** Build the user interface.
- **React DOM:** Render the application in the browser.
- **MapLibre GL JS:** Display interactive station maps.
- **Three.js:** Create 3D station visualizations.
- **Axios:** Communicate with backend APIs.
- **React Router DOM:** Navigate between application pages.
- **Lucide React:** Provide interface icons.
- **Socket.IO Client:** Receive real-time updates.

### Backend Dependencies

- **Node.js:** Execute backend JavaScript.
- **Express.js:** Create REST APIs and server routes.
- **Mongoose:** Connect the application to MongoDB.
- **Socket.IO:** Handle real-time communication.
- **JSON Web Token:** Manage authentication tokens.
- **bcrypt:** Securely hash passwords.
- **CORS:** Configure permitted frontend-to-backend requests.
- **dotenv:** Manage environment configuration.
- **A* / Dijkstra Implementation:** Calculate routes through station maps.

### Development Requirements

- Node.js and npm
- MongoDB or MongoDB Atlas
- Visual Studio Code
- Git and GitHub
- A modern web browser
- Internet connection for hosted services and map resources

### Expected Outcome

RailNav AI will provide passengers with a convenient and accessible way to navigate railway stations. By combining interactive maps, shortest-path routing, QR-based location identification, voice guidance, and real-time facility updates, the system aims to improve passenger experience, reduce confusion, and support more efficient movement within railway stations.
