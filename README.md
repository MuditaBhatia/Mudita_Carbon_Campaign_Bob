# Carbon Campaign Application

IBM Verify Identity Governance Campaign Application built with Carbon Design System and React + TypeScript.

## Features

- **Empty State Page**: Initial landing page when no campaigns exist
- **Campaign List Page**: View all campaigns with status cards and data table
- **Create Campaign Modal**: Multi-step wizard to create new campaigns
  - Step 1: Select campaign type (User entitlement, Account, Role composition)
  - Step 2: Enter campaign details (Name, Description, Type)
- **Carbon Design System**: Full IBM Carbon UI components and dark theme
- **TypeScript**: Type-safe development
- **React Router**: Client-side routing

## Tech Stack

- **React 18** - UI library
- **TypeScript** - Type safety
- **Vite** - Build tool
- **Carbon Design System** - IBM's design system
- **React Router** - Routing
- **Sass** - CSS preprocessing

## Project Structure

```
carbon-campaign-app/
├── src/
│   ├── components/
│   │   ├── campaign/
│   │   │   ├── CreateCampaignModal.tsx
│   │   │   └── InfoModal.tsx
│   │   └── layout/
│   │       ├── AppHeader.tsx
│   │       └── AppBreadcrumb.tsx
│   ├── pages/
│   │   ├── EmptyStatePage.tsx
│   │   └── CampaignListPage.tsx
│   ├── types/
│   │   └── campaign.ts
│   ├── styles/
│   │   └── index.scss
│   ├── App.tsx
│   └── main.tsx
├── index.html
├── package.json
├── tsconfig.json
├── vite.config.ts
└── README.md
```

## Getting Started

### Prerequisites

- Node.js 18+ and npm

### Installation

1. Navigate to the project directory:
```bash
cd carbon-campaign-app
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:5173`

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## Features Implemented

### 1. Empty State Page
- Displays when no campaigns exist
- Shows informational content about campaigns
- "Learn more" section with documentation links
- "Create campaign" button to start

### 2. Campaign List Page
- Status cards showing campaign statistics (Running, Scheduled, Paused, Closed)
- Tabs for filtering campaigns by status
- Data table with:
  - Checkbox selection
  - Campaign name, type, services
  - Progress indicators
  - End date and time left
  - Recommendations status tags
  - Sortable columns
  - Search functionality

### 3. Create Campaign Modal
- Multi-step wizard with progress indicator
- Step 1: Campaign Type Selection
  - Radio tile cards for User entitlement, Account, Role composition
  - Descriptive text for each type
- Step 2: Campaign Details
  - Name input (required)
  - Description textarea (optional)
  - Type dropdown selector
  - Form validation

### 4. Carbon Design System Integration
- Dark theme (g100)
- UI Shell header with navigation
- Breadcrumb navigation
- Carbon components throughout
- Consistent IBM design language

## Design Decisions

1. **Carbon Design System**: Used IBM's official design system for authentic IBM look and feel
2. **Dark Theme**: Implemented g100 theme to match the screenshots
3. **TypeScript**: Strong typing for better development experience
4. **Component Architecture**: Modular components for reusability
5. **State Management**: React hooks for local state management
6. **Routing**: React Router for navigation structure

## Future Enhancements

- Backend API integration
- Campaign detail view
- Campaign editing and deletion
- Advanced filtering and sorting
- User authentication
- Real-time updates
- Export functionality
- Bulk operations

## License

MIT