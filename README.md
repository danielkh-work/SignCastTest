# Digital Signage Content Management System

## Overview
This project is a simple digital signage content management system that consists of two main components:

1. **Web Dashboard**: A user-friendly interface for creating, managing, and organizing digital signage content.
2. **Electron Display Application**: A full-screen display application that synchronizes with the dashboard to showcase the content.

## Features

### Web Dashboard
- Simple content creation interface using Fabric.js (text, images, basic layouts).
- Content preview functionality.
- Optional content scheduling options.
- Content list with status indicators.
- Basic content organization (folders/categories).
- Display device status monitoring.

### Electron Display Application
- Full-screen content display.
- Support for text and image content.
- Manual sync button with status indicator.
- Auto-sync toggle option.
- Offline content playback.
- System tray controls.
- Connection status indicator.
- Basic error notifications.

### Offline Capabilities
- Local content storage for offline playback.
- Content caching mechanism.
- Automatic content sync when connection is restored.
- Local content backup.
- Offline status indication.

## Technical Specifications
- **WebSocket Implementation**: For real-time updates between the dashboard and the display application.
- **Local Storage**: To support offline content playback and caching.
- **Clean, Responsive UI**: Designed for usability on both desktop and mobile devices.
- **Basic Security**: Implementation of secure communications and data handling.
- **Error Logging and Handling**: Comprehensive error detection and reporting.

## Setup Instructions

### Web Dashboard
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/digital-signage-cms.git
   cd digital-signage-cms
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm run dev
   ```
4. Deploy the dashboard using Vercel:
   - Install the Vercel CLI: `npm install -g vercel`
   - Run `vercel` in the project directory and follow the prompts.

### Electron Display Application
1. Navigate to the `electron-app` directory:
   ```bash
   cd electron-app
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the application in development mode:
   ```bash
   npm start
   ```
4. Build the application for production:
   ```bash
   npm run build
   ```

## Architecture Overview
The system follows a client-server model:
- **Web Dashboard**: Hosts the content management functionality, communicates with the Electron app via WebSocket for real-time updates.
- **Electron Display Application**: Serves as the content viewer, with capabilities for offline playback and local storage.
- **WebSocket**: Facilitates bi-directional communication for immediate synchronization.

## WebSocket Implementation
- **Purpose**: Real-time updates between the dashboard and the display application.
- **Usage**:
  - Dashboard pushes updates (e.g., new content, status changes).
  - Electron app receives updates and synchronizes content.
- **Libraries**: `ws` for Node.js backend, WebSocket API for the Electron app.

## Offline Functionality
- **Content Caching**: Content is stored locally on the Electron app for playback during offline periods.
- **Automatic Sync**: Content automatically syncs when the network connection is restored.
- **Backup Mechanism**: Ensures that content is retrievable even after unexpected failures.

## Known Limitations
- Scheduling feature is optional and not fully implemented.
- No advanced user management or permissions system.
- Limited error notifications and diagnostics.

## Future Improvements
- Add advanced scheduling options (e.g., recurring schedules).
- Implement user roles and permissions.
- Extend support for additional content types (e.g., video, interactive elements).
- Enhance error reporting with detailed diagnostics.
- Improve security measures (e.g., encryption, authentication).


