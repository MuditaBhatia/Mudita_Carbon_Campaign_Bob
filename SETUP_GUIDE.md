# Carbon Campaign Application - Setup Guide

## Overview

This is a complete recreation of the IBM Verify Identity Governance Campaign application using IBM's Carbon Design System. The application features a dark theme (g100) and implements all the screens shown in the reference screenshots.

## What's Been Built

### 1. **Project Structure** ✅
- Modern React + TypeScript + Vite setup
- Carbon Design System integration
- Proper folder structure for scalability

### 2. **Configuration Files** ✅
- `package.json` - All dependencies including Carbon React and Icons
- `tsconfig.json` - TypeScript configuration with path aliases
- `vite.config.ts` - Vite build configuration
- `.eslintrc.cjs` - ESLint configuration

### 3. **Type Definitions** ✅
- `src/types/campaign.ts` - Complete type definitions for campaigns, stats, and forms

### 4. **Layout Components** ✅
- `AppHeader.tsx` - IBM Carbon UI Shell header with navigation icons
- `AppBreadcrumb.tsx` - Breadcrumb navigation component

### 5. **Campaign Components** ✅
- `CreateCampaignModal.tsx` - Multi-step wizard modal
  - Step 1: Campaign type selection with radio tiles
  - Step 2: Campaign details form
  - Progress indicator sidebar
  - Form validation
- `InfoModal.tsx` - Reusable informational modal

### 6. **Pages** ✅
- `EmptyStatePage.tsx` - Initial state when no campaigns exist
  - Large icon and informative text
  - "Learn more" section with documentation links
  - Call-to-action to create first campaign
- `CampaignListPage.tsx` - Main campaigns view
  - Status cards (Running, Scheduled, Paused, Closed)
  - Tabs for filtering
  - Data table with all campaign information
  - Search and create functionality

### 7. **Main Application** ✅
- `App.tsx` - Main app component with routing and state management
- `main.tsx` - Application entry point
- `styles/index.scss` - Carbon theme configuration (g100 dark theme)

## Features Implemented

### Empty State (Screenshot 1 & 5)
- ✅ "No campaigns yet" heading
- ✅ Descriptive text about certification campaigns
- ✅ Large icon on the left
- ✅ "Learn more" section on the right with links
- ✅ Create campaign button in header

### Create Campaign Modal - Type Selection (Screenshot 2)
- ✅ Modal with "Create campaign" title
- ✅ Progress indicator showing "Type" and "Details" steps
- ✅ Three radio tile options:
  - User entitlement
  - Account
  - Role composition
- ✅ Each tile has title and description
- ✅ Cancel, Back (disabled), and Next buttons

### Create Campaign Modal - Details (Screenshot 3)
- ✅ Progress indicator showing step 2 active
- ✅ Name input field (required)
- ✅ Description textarea (optional)
- ✅ Type dropdown selector
- ✅ Cancel, Back, and Create buttons
- ✅ Form validation

### Campaign List (Screenshot 4)
- ✅ Status cards showing metrics:
  - Running (4/5)
  - Scheduled (0)
  - Paused (1)
  - Closed (3)
- ✅ Tabs: All campaigns, Running, Scheduled, Closed
- ✅ Data table with columns:
  - Checkbox for selection
  - Name
  - Type
  - Services
  - Progress (percentage and count)
  - End date
  - Time left
  - Recommendations (with status tags)
- ✅ Search functionality
- ✅ Create campaign button
- ✅ Sortable columns (End date with arrow icon)

### Additional Features
- ✅ Dark theme (Carbon g100)
- ✅ IBM Carbon UI Shell header
- ✅ Breadcrumb navigation
- ✅ Responsive layout
- ✅ TypeScript type safety
- ✅ Sample campaign data

## Installation & Running

### Prerequisites
- Node.js 18 or higher
- npm or yarn

### Steps

1. **Navigate to project directory:**
```bash
cd carbon-campaign-app
```

2. **Install dependencies** (if not already done):
```bash
npm install
```

3. **Start development server:**
```bash
npm run dev
```

4. **Open browser:**
Navigate to `http://localhost:5173`

## Project Structure

```
carbon-campaign-app/
├── src/
│   ├── components/
│   │   ├── campaign/
│   │   │   ├── CreateCampaignModal.tsx    # Multi-step campaign creation
│   │   │   └── InfoModal.tsx              # Informational modal
│   │   └── layout/
│   │       ├── AppHeader.tsx              # Carbon UI Shell header
│   │       └── AppBreadcrumb.tsx          # Breadcrumb navigation
│   ├── pages/
│   │   ├── EmptyStatePage.tsx             # No campaigns state
│   │   └── CampaignListPage.tsx           # Campaign list with table
│   ├── types/
│   │   └── campaign.ts                    # TypeScript definitions
│   ├── styles/
│   │   └── index.scss                     # Carbon theme & styles
│   ├── App.tsx                            # Main app with routing
│   └── main.tsx                           # Entry point
├── index.html                             # HTML template
├── package.json                           # Dependencies
├── tsconfig.json                          # TypeScript config
├── vite.config.ts                         # Vite config
├── .eslintrc.cjs                          # ESLint config
├── .gitignore                             # Git ignore rules
├── README.md                              # Project documentation
└── SETUP_GUIDE.md                         # This file
```

## Key Technologies

- **React 18** - UI library
- **TypeScript** - Type safety
- **Vite** - Fast build tool
- **Carbon Design System (@carbon/react)** - IBM's design system
- **Carbon Icons (@carbon/icons-react)** - IBM's icon library
- **React Router DOM** - Client-side routing
- **Sass** - CSS preprocessing for Carbon styles

## Carbon Components Used

- `Header`, `HeaderName`, `HeaderGlobalBar`, `HeaderGlobalAction` - UI Shell
- `Breadcrumb`, `BreadcrumbItem` - Navigation
- `Button` - Actions
- `ComposedModal`, `Modal` - Dialogs
- `RadioTile`, `TileGroup` - Type selection
- `TextInput`, `TextArea`, `Select` - Form inputs
- `DataTable`, `Table`, `TableHead`, `TableBody` - Data display
- `Tabs`, `TabList`, `Tab`, `TabPanels` - Content organization
- `Tag` - Status indicators
- `ProgressIndicator`, `ProgressStep` - Wizard navigation
- `Tile` - Content containers
- `Content` - Page layout

## Sample Data

The application includes 5 sample campaigns with various statuses:
1. Yearly Account Certification for RACF Accounts (Processing)
2. User Access Certification on RACF (Available)
3. NAB Yearly campaign for machine identities
4. NAB Access Certification
5. Corporate GCP Service

## Next Steps

To extend this application, you could:

1. **Backend Integration**
   - Connect to REST API
   - Implement real data fetching
   - Add authentication

2. **Additional Features**
   - Campaign detail view
   - Edit/delete campaigns
   - Advanced filtering
   - Export functionality
   - Bulk operations

3. **Enhanced UI**
   - Loading states
   - Error handling
   - Toast notifications
   - Confirmation dialogs

4. **Testing**
   - Unit tests with Jest
   - Component tests with React Testing Library
   - E2E tests with Playwright

## Troubleshooting

### TypeScript Errors
The TypeScript errors you see before running `npm install` are expected. They will be resolved once all dependencies are installed.

### Port Already in Use
If port 5173 is already in use, Vite will automatically try the next available port.

### Styling Issues
Make sure Sass is installed (`npm install sass`) as Carbon requires it for theming.

## Resources

- [Carbon Design System](https://carbondesignsystem.com/)
- [Carbon React Components](https://react.carbondesignsystem.com/)
- [Carbon Icons](https://www.carbondesignsystem.com/guidelines/icons/library/)
- [React Documentation](https://react.dev/)
- [TypeScript Documentation](https://www.typescriptlang.org/)
- [Vite Documentation](https://vitejs.dev/)

## Support

For issues or questions about:
- **Carbon Design System**: Check the [Carbon GitHub](https://github.com/carbon-design-system/carbon)
- **This Implementation**: Review the code comments and component structure

---

**Built with ❤️ using IBM Carbon Design System**