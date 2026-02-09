# Cookwise Pro Sync Feature Documentation

## Overview of Sync Functionality

The Cookwise Pro application includes a cross-device synchronization system that allows users to keep their recipe data consistent across multiple devices. The sync system is built around a cloud-based server architecture.

## How Sync Works

### 1. Sync Initialization
- The sync system initializes when the app loads
- Checks if sync is enabled via `isSyncEnabled()` function
- Starts periodic synchronization if enabled

### 2. Authentication & Credentials
- Users need a `userId` and `authToken` to enable sync
- Credentials are stored in browser's localStorage:
  - `syncEnabled` - Flag indicating if sync is active
  - `syncUserId` - User identifier
  - `syncAuthToken` - Authentication token

### 3. Data Types Synchronized
The following data types are synchronized between devices:
- **Recipes** - All recipe information including ingredients, directions, images, etc.
- **Meal Plans** - Weekly meal planning data
- **Shopping Lists** - Current shopping list items
- **Pantry** - Ingredient inventory with quantities and expiration dates
- **Collections** - Custom recipe collections

### 4. Sync Process
- **Periodic Sync**: Runs every 10 minutes when enabled
- **Data Collection**: Gathers all local data from IndexedDB stores
- **Cloud Upload**: Sends data to the sync server via POST request
- **Cloud Download**: Receives updated data from other devices
- **Local Update**: Updates local IndexedDB with received data
- **Timestamp Tracking**: Maintains last sync timestamp

### 5. Sync Server Architecture
- The sync server URL is defined as `https://cookwise-sync-server.example.com`
- Uses HTTPS POST requests with JSON payloads
- Authentication via Bearer token in Authorization header
- Payload includes user ID, all data types, timestamps, and sync history

### 6. Conflict Resolution
- The system downloads changes from the cloud and applies them locally
- Last-write-wins approach for conflicting changes
- Maintains modification timestamps to determine most recent changes

### 7. Manual Sync
- Users can force a sync using the `forceSync()` function
- Sync status can be checked via the `getSyncStatus()` function

## Enabling Sync

```javascript
// Enable sync with user credentials
await enableCloudSync(userId, authToken);

// Disable sync
disableCloudSync();

// Force immediate sync
await forceSync();

// Check sync status
const status = getSyncStatus();
```

## Technical Implementation

### Key Functions:
- `enableCloudSync(userId, authToken)` - Enables sync with credentials
- `disableCloudSync()` - Disables sync and stops periodic sync
- `isSyncEnabled()` - Checks if sync is currently enabled
- `startPeriodicSync()` - Starts automatic sync every 10 minutes
- `syncDataWithCloud()` - Performs actual sync with cloud server
- `forceSync()` - Forces immediate sync
- `getSyncStatus()` - Returns current sync status

### Data Flow:
1. Local IndexedDB → Collect all data → JSON payload
2. JSON payload → HTTP POST → Cloud sync server
3. Cloud sync server → Process and merge → Return updated data
4. Updated data → Apply to local IndexedDB → Update UI

## Limitations

Based on the code, the sync feature appears to be:
- Still in development (server URL is a placeholder)
- Designed for authenticated users only
- Dependent on an external sync server infrastructure
- Implemented with a polling mechanism rather than real-time updates

## Security
- Authentication tokens stored in localStorage (potential security concern)
- HTTPS used for all sync communications
- User-specific data isolation via userId

## Status
The sync functionality is implemented in the client-side code but relies on a backend server that appears to be represented by a placeholder URL. Actual deployment would require a functioning sync server at the specified endpoint.