# School of Management Business Intelligence (SoM.BI)

A comprehensive business intelligence dashboard for the School of Management, designed to track and visualize KPIs across various domains including teaching, research, and administrative performance.

## Features

- 📊 Interactive performance dashboards
- 🔐 Secure authentication with Firebase
- 📱 Fully responsive design for mobile and desktop
- 📈 Real-time KPI tracking and visualization
- 🎯 Domain-specific performance metrics
- 📋 Role-based access control (Admin, Dean, Lecturer)

## Tech Stack

- **Frontend Framework**: Nuxt.js 3
- **UI Framework**: Tailwind CSS
- **Authentication**: Firebase Auth
- **Database**: Mysql
- **Charts**: Chart.js
- **Icons**: Heroicons

## Prerequisites

- Node.js (v16 or higher)
- npm or yarn
- Firebase project with Authentication and Mysql enabled

## Setup

1. Clone the repository:
```bash
git clone <repository-url>
cd senior_project
```

2. Install dependencies:
```bash
npm install
# or
yarn install
```

3. Create a Firebase configuration:
- Create a new file `plugins/firebase.ts`
- Copy the Firebase configuration from your Firebase Console
- Use the following template:
```typescript
export default {
  apiKey: "your-api-key",
  authDomain: "your-auth-domain",
  projectId: "your-project-id",
  storageBucket: "your-storage-bucket",
  messagingSenderId: "your-messaging-sender-id",
  appId: "your-app-id"
}
```

4. Create environment variables:
```bash
cp .env
```

## Development

Start the development server:
```bash
npm run dev
# or
yarn dev
```

The application will be available at `http://localhost:3000`

### Backend development

The Express API is a separate application in `api-backend/`. In a second terminal, install its dependencies and start its development server:

```bash
cd api-backend
npm install
npm run dev
```

The API listens on port `8080` by default, or the port specified by `PORT`. Configure its MySQL connection with `DB_HOST`, `DB_PORT`, `DB_USER`, `DB_PASSWORD`, and `DB_NAME` in `api-backend/.env`. Protected routes also require Firebase Admin credentials for the project's Firebase environment.

Set `NUXT_PUBLIC_BACKEND_API_URL=http://localhost:8080` in the frontend environment and restart Nuxt to use the local API. Both applications must be running to develop features backed by this API.

## Build

Build the application for production:
```bash
npm run build
# or
yarn build
```

## Project Structure

```
├── components/       # Reusable Vue components
├── composables/      # Composable functions
├── layouts/          # Page layouts (admin, dean, lecturer)
├── pages/            # Application pages and routes
├── plugins/          # Nuxt plugins
├── public/           # Static files
└── types/            # TypeScript type definitions
```

## Security

- Firebase configuration is gitignored for security
- Environment variables are used for sensitive data
- Authentication state is managed securely
- Role-based access control is implemented

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is private and confidential. All rights reserved.
npm run dev

# pnpm
pnpm dev

# yarn
yarn dev

# bun
bun run dev
```

## Production

Build the application for production:

```bash
# npm
npm run build

# pnpm
pnpm build

# yarn
yarn build

# bun
bun run build
```

Locally preview production build:

```bash
# npm
npm run preview

# pnpm
pnpm preview

# yarn
yarn preview

# bun
bun run preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.
