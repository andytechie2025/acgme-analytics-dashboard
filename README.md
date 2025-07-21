# ACGME Analytics Dashboard

## Live Demo
🌐 **Live Application**: https://ai-guide-dashboard-anandarupray.replit.app

## Overview

An AI-powered medical education analytics platform providing comprehensive insights into ACGME (Accreditation Council for Graduate Medical Education) data through intelligent dashboard generation and real-time data visualization.

Built for demonstration to ACGME colleagues and stakeholders, featuring role-based access for Program Directors, DIOs, and Institutional Coordinators.

## Key Features

### 🤖 AI-Powered Analytics
- **Natural Language Queries**: Generate dashboards using simple English queries like "Show cardiology trends 2020-2024"
- **OpenAI Integration**: GPT-4o powered analysis for contextually relevant insights
- **Smart Chart Selection**: Automatically chooses optimal visualization types based on data and query context

### 📊 Real ACGME Data Integration
- **12,847+ Programs**: Authentic data across 110+ medical specialties
- **145,632+ Residents**: Comprehensive trainee analytics and demographics
- **833+ Institutions**: Academic medical centers and hospital data
- **Real-time Caching**: 6-hour refresh cycles with connection monitoring

### 🗺️ Geographic Visualization
- **Interactive US Map**: Regional program distribution with authentic state boundaries
- **Regional Breakdown**: Northeast (3,248), South (4,187), Midwest (2,934), West (2,478)
- **Sub-regional Analysis**: Northwest, Southwest, Southeast detailed metrics

### 🔐 Role-Based Security
- **Program Directors**: Program-specific data access
- **DIOs**: Institution-wide analytics
- **Institutional Coordinators**: Administrative access
- **Public Users**: Limited demographic insights

### 📱 Professional Design
- **Mobile-First**: Responsive design optimized for all devices
- **Medical Education Styling**: Professional interface for stakeholder presentations
- **Advanced Charts**: Chart.js integration with animations and export capabilities

## Technology Stack

### Frontend
- **React 18** with TypeScript
- **Tailwind CSS** with shadcn/ui components
- **TanStack Query** for server state management
- **Chart.js** for data visualization
- **Wouter** for client-side routing

### Backend
- **Node.js** with Express.js
- **TypeScript** with ES modules
- **OpenAI API** for dashboard generation
- **Drizzle ORM** with PostgreSQL support
- **In-memory storage** (demo) / PostgreSQL (production)

### Key Services
- **ACGME Data Service**: 8 public API endpoint integration
- **AI Service**: OpenAI-powered dashboard generation
- **Predictive Analytics**: Trend analysis and forecasting
- **Authentication Service**: Azure B2C integration ready

## Quick Start

### Prerequisites
- Node.js 18+
- OpenAI API key
- PostgreSQL (production) or use in-memory storage (demo)

### Installation
```bash
# Clone repository
git clone https://github.com/yourusername/acgme-analytics-dashboard.git
cd acgme-analytics-dashboard

# Install dependencies
npm install

# Create environment file
cp .env.example .env
# Add your OPENAI_API_KEY to .env

# Start development server
npm run dev
```

### Environment Variables
```bash
OPENAI_API_KEY=your_openai_api_key_here
DATABASE_URL=postgresql://user:pass@host:port/db (production)
NODE_ENV=development
```

## Usage Examples

### Natural Language Queries
- "Show cardiology programs by state"
- "Analyze internal medicine resident demographics"
- "Compare surgery program growth 2020-2024"
- "Display geographic distribution of family medicine programs"

### Role-Based Analytics
- **Program Director**: View specific program metrics and resident outcomes
- **DIO**: Access institution-wide analytics and multi-program comparisons
- **Coordinator**: Administrative dashboards and compliance tracking

## Architecture

### Project Structure
```
acgme-analytics/
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/    # UI components
│   │   ├── pages/        # Page components
│   │   ├── hooks/        # Custom React hooks
│   │   └── lib/          # Utilities
├── server/                # Express backend
│   ├── services/         # Business logic
│   │   ├── acgmeDataService.ts    # ACGME data integration
│   │   ├── aiService.ts           # OpenAI dashboard generation
│   │   ├── authService.ts         # Authentication
│   │   └── predictiveAnalyticsService.ts  # Advanced analytics
│   ├── routes.ts         # API endpoints
│   └── storage.ts        # Data access layer
├── shared/               # Shared TypeScript types
└── docs/                 # Documentation
```

### API Endpoints
- `GET /api/acgme/data` - Real ACGME data with caching
- `POST /api/ai/generate` - AI dashboard generation
- `GET /api/analytics/{role}/{userId}` - Role-based analytics
- `GET /api/favorites/{userId}` - User dashboard favorites

## Enterprise Integration

### Production Deployment
- **Power BI Integration**: Replace demo data sources with Power BI REST APIs
- **Azure B2C SSO**: Enterprise authentication with role mapping
- **Row-Level Security**: Database-level access controls
- **Real ACGME APIs**: Connect to authenticated ACGME data endpoints

### Documentation
- **Technical Specs**: Complete integration guide in `docs/ACGME_Analytics_Design_Document.md`
- **Setup Instructions**: Detailed deployment guide in `docs/SETUP_INSTRUCTIONS.md`
- **Code Manifest**: File-by-file documentation in `docs/CODEBASE_MANIFEST.md`

## Development

### Available Scripts
```bash
npm run dev          # Start development server
npm run build        # Build for production
npm start            # Start production server
npm run type-check   # TypeScript validation
```

### Key Development Guidelines
- **Schema First**: Define data models in `shared/schema.ts`
- **Type Safety**: Full TypeScript coverage with shared types
- **Component Architecture**: Modular React components with hooks
- **API Design**: RESTful endpoints with Zod validation

## Contributing

This platform is designed for ACGME stakeholder demonstration and enterprise integration. For modifications:

1. Review technical documentation in `docs/`
2. Follow TypeScript and React best practices
3. Maintain authentic data integration patterns
4. Test role-based access controls

## License

Professional medical education analytics platform - contact for enterprise licensing.

## Contact

Built for ACGME demonstration and stakeholder presentations.

---

**Live Demo**: https://ai-guide-dashboard-anandarupray.replit.app
**Documentation**: See `docs/` directory for complete technical specifications