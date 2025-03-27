Set up the frontend according to the following prompt:
  <frontend-prompt>
  Create detailed components with these requirements:
  1. Use 'use client' directive for client-side components
  2. Make sure to concatenate strings correctly using backslash
  3. Style with Tailwind CSS utility classes for responsive design
  4. Use Lucide React for icons (from lucide-react package). Do NOT use other UI libraries unless requested
  5. Use stock photos from picsum.photos where appropriate, only valid URLs you know exist
  6. Configure next.config.js image remotePatterns to enable stock photos from picsum.photos
  7. Create root layout.tsx page that wraps necessary navigation items to all pages
  8. MUST implement the navigation elements items in their rightful place i.e. Left sidebar, Top header
  9. Accurately implement necessary grid layouts
  10. Follow proper import practices:
     - Use @/ path aliases
     - Keep component imports organized
     - Update current src/app/page.tsx with new comprehensive code
     - Don't forget root route (page.tsx) handling
     - You MUST complete the entire prompt before stopping
  </frontend-prompt>

  <summary_title>
Financial Analysis Dashboard with Market Intelligence Interface
</summary_title>

<image_analysis>
1. Navigation Elements:
- Primary navigation: 股指信息, 公司快讯, 研究报告, 行业分析, 搜索公司, 市场概况
- Secondary navigation: Located top-right, includes login/user controls
- Logo: Positioned top-left, light color scheme
- Header height: 60px with gradient background
- Search functionality integrated in header

2. Layout Components:
- Main container: 1200px max-width
- Top banner section: Full-width, 400px height
- Content grid: 3-column layout
- Card containers: 280px width, variable height
- Spacing: 20px gutters between components

3. Content Sections:
- Data visualization area: Charts and graphs
- News feed section: List-based content
- Market analysis blocks: Grid-based layout
- Statistical displays: Pie charts and bar graphs
- Company information cards: Uniform width containers

4. Interactive Controls:
- Search bar: Full-width with autocomplete
- Filter buttons: Pill-shaped toggles
- Data refresh controls: Icon-based buttons
- Dropdown menus: Custom styled selects
- Interactive charts with hover states

5. Colors:
- Primary: #1E88E5 (blue)
- Secondary: #00BCD4 (cyan)
- Background: #0A192F (dark blue)
- Text: #FFFFFF (white)
- Accent: #4CAF50 (green)
- Charts: Multi-color palette for data visualization

6. Grid/Layout Structure:
- 12-column grid system
- Responsive breakpoints at 768px, 992px, 1200px
- Fixed-width containers for data displays
- Flexible content areas with min/max constraints
</image_analysis>

<development_planning>
1. Project Structure:
```
src/
├── components/
│   ├── layout/
│   │   ├── Header
│   │   ├── Navigation
│   │   └── Dashboard
│   ├── features/
│   │   ├── MarketData
│   │   ├── CompanyNews
│   │   └── Analysis
│   └── shared/
│       ├── Charts
│       └── Controls
├── assets/
├── styles/
├── hooks/
└── utils/
```

2. Key Features:
- Real-time market data integration
- Interactive data visualization
- Company search and filtering
- News aggregation system
- Analysis tools integration

3. State Management:
```typescript
interface AppState {
  market: {
    indices: MarketIndex[];
    trends: TrendData[];
    statistics: Statistics;
  },
  company: {
    details: CompanyDetail[];
    news: NewsItem[];
    analysis: AnalysisData[];
  },
  user: {
    preferences: UserPreferences;
    watchlist: WatchlistItem[];
  }
}
```

4. Component Architecture:
- DashboardContainer (parent)
  - MarketOverview
  - CompanyNews
  - AnalysisTools
  - SearchSystem
  - DataVisualizations

5. Responsive Breakpoints:
```scss
$breakpoints: (
  'mobile': 320px,
  'tablet': 768px,
  'desktop': 992px,
  'wide': 1200px
);
```
</development_planning>