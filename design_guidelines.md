# Instagram Follower Analysis Tool - Design Guidelines

## Design Approach
**Selected Approach**: Design System (Material Design)
**Justification**: This is a utility-focused tool requiring clear information hierarchy, efficient data processing workflows, and straightforward user interactions. Material Design's emphasis on clarity and functional design patterns suits this analytical application.

## Core Design Elements

### Color Palette
**Light Mode:**
- Primary: 234 89% 53% (Instagram-inspired purple-pink)
- Surface: 0 0% 98%
- Background: 0 0% 100%
- Text: 222 84% 5%

**Dark Mode:**
- Primary: 234 89% 63%
- Surface: 222 47% 11%
- Background: 222 84% 5%
- Text: 210 40% 98%

### Typography
- **Primary Font**: Inter (Google Fonts)
- **Headers**: 600-700 weight
- **Body**: 400-500 weight
- **Data/Stats**: 500-600 weight

### Layout System
**Spacing Units**: Tailwind units of 4, 6, 8, and 12
- Consistent padding: p-6, p-8
- Section spacing: space-y-8, space-y-12
- Component margins: m-4, m-6

### Component Library

#### Core Components
- **Upload Cards**: Prominent drag-and-drop zones with clear visual feedback
- **Progress Indicators**: Linear progress bars for data processing
- **Data Tables**: Clean, sortable tables for displaying non-followers
- **Statistics Cards**: Elevated cards showing key metrics (followers, following, non-followers)
- **Action Buttons**: Primary button for analysis, secondary for export

#### Navigation
- Simple header with tool title and minimal navigation
- Breadcrumb-style progress indicators for multi-step process

#### Forms & Data Input
- File upload dropzones with clear format instructions
- Validation states and error messaging
- Format examples and help text

#### Data Displays
- Tabular data with Instagram usernames
- Profile link integration
- Sorting and filtering capabilities
- Export functionality with download buttons

#### Overlays
- Loading states during data processing
- Success/error modals for user feedback
- Help tooltips for data extraction guidance

## Key Design Principles
1. **Clarity First**: Every step clearly explained with visual cues
2. **Data Transparency**: Show processing steps and validation
3. **Efficient Workflow**: Minimize clicks between upload and results
4. **Mobile Responsive**: Ensure tables and uploads work on mobile devices
5. **Privacy Focus**: Visual indicators that data stays local/private

## Layout Structure
- **Header**: Tool branding and navigation
- **Main Content**: Step-by-step workflow cards
- **Results Section**: Statistics overview + detailed table
- **Footer**: Privacy notice and export options

## Images
No large hero image required. Instead, use:
- **Iconography**: Upload icons, analysis icons, and social media icons
- **Illustrations**: Simple vector graphics showing the data flow process
- **Screenshots**: Example Instagram data export screenshots for guidance