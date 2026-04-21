# Setup Documentation

## Project Overview

This is a Next.js fullstack application with the following core technologies:

### Frameworks & Libraries
- **Next.js** - React framework for web applications
- **React** - UI library for building components
- **TypeScript** - Type-safe JavaScript

### Development Tools
- **Biome** - Linter and formatter for JavaScript/TypeScript
- **Vercel** - Deployment platform (project appears to be deployed there)

## Project Structure

```
baseline-fullstack-app/
├── public/              # Static assets
├── src/
│   └── app/            # Next.js app directory
│       ├── favicon.ico
│       ├── globals.css
│       ├── layout.tsx
│       └── page.tsx
├── skills/            # Agent skills
│   ├── create-implementation-plan/
│   └── find-skills/
├── .gitignore
├── AGENTS.md          # Agent configuration
├── biome.json         # Linter configuration
├── next.config.ts     # Next.js configuration
├── package.json       # Dependencies
├── postcss.config.mjs # PostCSS configuration
├── README.md          # Project documentation
├── skills-lock.json   # Skills lock file
└── tsconfig.json      # TypeScript configuration
```

## Skills Directory

The project includes two agent skills:

1. **create-implementation-plan** (`skills/create-implementation-plan/`)
   - Purpose: Creates implementation plans for new features, refactoring, upgrades, and infrastructure changes
   - File: `SKILL.md`

2. **find-skills** (`skills/find-skills/`)
   - Purpose: Helps users discover and install agent skills
   - File: `SKILL.md`

## Dependencies

### Production Dependencies
- `next` - Next.js framework
- `react` - React library
- `react-dom` - React DOM renderer

### Development Dependencies
- `@biomejs/biome` - Linter/formatter
- `@types/react` - React type definitions
- `@types/node` - Node.js type definitions
- `@types/react-dom` - React DOM type definitions
- `typescript` - TypeScript compiler

## Configuration Files

- **next.config.ts** - Next.js configuration
- **tsconfig.json** - TypeScript configuration
- **biome.json** - Biome linter configuration
- **postcss.config.mjs** - PostCSS configuration
- **AGENTS.md** - Agent-specific rules and configuration

## Quick Start

1. Install dependencies: `npm install`
2. Run development server: `npm run dev`
3. Build for production: `npm run build`
4. Start production server: `npm start`

## Deployment

The project is configured for deployment on Vercel (based on the git remote URL).



## Next Steps

### Authentication
- **Better-Auth**
  - https://better-auth.com/
  - npx skills add better-auth/skills
  - Modern authentication library for Next.js with built-in providers

### API Development
- **NodeJS API Framework**
  - https://www.npmjs.com/package/express-zod-api
  - https://github.com/anatine/zod-plugins/tree/main/packages/zod-nestjs
  - Create type-safe APIs with Zod validation
  - Choose between Express or NestJS based on project complexity

### API Documentation**
- **Swagger/OpenAPI** - Standardized API documentation
- **tRPC** - End-to-end type-safe APIs
  - `pnpm add @trpc/server @trpc/client`
  - Automatic TypeScript types from resolvers
  - Zero-runtime-cost type validation

### API Testing
- **MSW (Mock Service Worker)**
  - Mock API responses during development and testing
  - Intercepts network requests at the browser level
  - Works seamlessly with Vitest for integration testing

### Git Hooks & Workflow
- **Lefthook**
  - https://github.com/evilmartians/lefthook
  - pnpm add -D lefthook
  - Fast Git hooks manager (alternative to Husky/HookJS)
  - Run linting and tests before commits

### CI/CD & DevOps
   - GitHub Actions VS Code plugin
   - Automated testing and deployment pipeline
   - Integration with Vercel for automatic deployments
   - **Branch Protection Rules** - Require PR reviews and passing checks
   - **Dependabot** - Automated dependency updates
   - **CodeQL** - Static analysis for security vulnerabilities
   - **PR Templates** - Standardized pull request descriptions

### AWS Development
- **Local AWS Mocks**
  - pnpm add -D aws-sdk-client-mock @aws-sdk/client-s3 @aws-sdk/client-dynamodb
  - Test AWS integrations locally without real resources
  - Useful for S3, DynamoDB, SQS integrations
- **AWS CDK** - Infrastructure as Code
  - Define AWS infrastructure in TypeScript/JavaScript
  - Automate infrastructure provisioning and management
  - Version control infrastructure alongside application code
- **AWS Amplify** - Full-stack development
  - Host web apps directly from GitHub
  - Managed authentication with Cognito
  - Serverless functions with Lambda

### Database Options
- **PostgreSQL**
  - Local through rancher-desktop
  - AWS RDS for production
  - Good for structured data with complex queries
  - **Prisma ORM** - Type-safe database access
    - `pnpm add prisma @prisma/client`
    - Automatic type generation from schema
    - Built-in migration system
- **Supabase**
  - Local through rancher-desktop
  - Deployed on production
  - PostgreSQL with built-in auth, storage, and real-time features
  - **Supabase Auth** - Pre-built authentication flows
  - **Supabase Storage** - File uploads and management
  - **Real-time Subscriptions** - Live data updates
- **PlanetScale** - Serverless MySQL database
  - Zero-schema migrations
  - Branching for database changes
  - Good for legacy MySQL databases

### Internationalization (i18n)
- **next-intl** - Internationalization for Next.js
  - `pnpm add next-intl`
  - Type-safe translations
  - Automatic locale detection

### Accessibility (a11y)
- **React Aria** - Accessible component primitives
- **axe-core** - Automated accessibility testing
- **RTL Support** - Right-to-left language support


### Additional Enhancements
- **Storybook** - UI component development and documentation
  - Isolate and document components
  - Add knobs and controls for interactive testing
  - Automatically generate documentation from props

### End-to-end testing ❓
- Maybe not worth ROI
- **Playwright** - Modern E2E framework with cross-browser support
  - `pnpm add -D @playwright/test`
  - Record and replay test scenarios
  - Automatic waiting for elements
- **Cypress** - Developer-friendly E2E testing
  - `pnpm add -D cypress`
  - Visual test runner
  - Time travel debugging

### Infrastructure & Deployment
- **Deploy to AWS**
  - What services? not sure
  - ECS, Fargate, or Lambda for hosting
  - RDS for managed database
- **Infrastructure as Code**
  - Terraform for multi-cloud infrastructure
  - AWS CDK for AWS-specific resources
- **Container Registry**
  - ECS Container Registry (ECR)
  - GitHub Container Registry (GHCR)
- **Docker** - Containerization for consistent environments
  - Create consistent development environments
  - Simplify deployment to any platform
  - Isolate service dependencies (PostgreSQL, Redis, etc.)
  - **Docker Compose** - Multi-container orchestration


### Development Experience
- **Monorepo Setup**
  - Migrate to pnpm workspace for multiple packages
  - Shared types and utilities package
  - Consistent tooling across packages
- **Developer Documentation**
  - Architecture decision records (ADR)
  - Component library documentation
  - API documentation with examples

### Security & Compliance
- **Security Audit**
  - Snyk or Dependabot for vulnerability scanning
  - Secret scanning and prevention
- **Compliance**
  - GDPR compliance tools
  - HIPAA compliance for health data
  - SOC 2 requirements

### Analytics & Insights
- **Analytics Integration**
  - Plausible or Umami for privacy-focused analytics
  - Custom event tracking
  - User behavior analysis
- **A/B Testing**
  - Optimizely or Google Optimize
  - Feature flag management
  - LaunchDarkly integration

### Monitoring & Logging
- **Sentry** - Error tracking and performance monitoring
- **LogRocket** - Session replay and error tracking
- **OpenTelemetry** - Observability standards


### Performance Optimization
- **Image Optimization** - Next.js Image component
- **Font Optimization** - Preload critical fonts
- **Code Splitting** - Lazy load routes and components
- **Bundle Analysis** - Identify large dependencies
