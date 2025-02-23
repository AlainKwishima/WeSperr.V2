# WeSperr Messenger

This is a feature-rich chat application built with React, Appwrite, Chakra UI and other modern technologies. The app allows users to engage in real-time messaging, create and manage group chats, update their profiles, and more.


## Features

- **Real-Time Messaging:** Instant messaging with support for text, images, and voice messages.
- **Group Chats:** Create and manage group conversations with multiple participants.
- **User Authentication:** Secure registration and login functionality for user accounts (OAuth and Email)
- **Profile Customization:** Personalize your profile with avatars, and more.
- **Multimedia Sharing:** Share files, documents, and locations within the chat.

## Getting Started

### Prerequisites

- Node.js and npm installed on your machine.

## Running WeSperr

1. Clone the repository:

   ```bash
   git clone https://github.com/VincentMukuna/WeSperr.git

   ```

2. Change to the project directory:

   ```bash
   cd WeSperr
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

4. Copy the `.env.example` file to `.env`:

   ```bash
   cp .env.example .env
   ```

5. Install appwrite CLI:

   ```bash
   npm install -g appwrite-cli
   ```

## Appwrite Setup

1. Open the [Appwrite Console](https://cloud.appwrite.io/) and make a new project.

2. Add a new web app platform you can name it anything e.g `Web`, enter
   your local IP address (or `localhost`) in the hostname field.

3. Copy the API endpoint and project ID from the Appwrite project settings and replace them in the `.env` file.

4. Replace projectId and projectName in `appwrite.json` with your project's

5. Create a database and copy its name and id and replace it in `appwrite.json`.

6. Login to appwrite from the cli

   ```bash
      appwrite login
   ```

7. Deploy
   [UPDATE] You need to push the collections one by one in the following order:
   channels, group-messages, chat-messages, user-details, groups

   ```bash
      appwrite push collections
   ```

8. Deploy buckets.
   Edit- Due to appwrite pricing changes you may have to deploy only one bucket then set all bucket config in `src\lib\config.ts` to your bucketId.

   If you are using the free plan you can delete the other buckets and deploy only one.
   Copy the bucketId and replace it in `src\lib\config.ts` for all buckets.

   ```bash
      appwrite push buckets
   ```

9. Start the development server:

```bash
   npm run dev
```

### License

This project is licensed under the MIT License.

### Contact

For any questions or feedback, feel free to reach out at <alainkwishima@gmail.com.com>.
