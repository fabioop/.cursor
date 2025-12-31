---
description: Next.js with JavaScript best practices
globs: **/*.tsx, **/*.ts, **/*.js
---

# Next.js Best Practices

## Project Structure

- Use the App Router directory structure
- Place components in `app` directory for route-specific components
- Organize shared components in `components` directory with subfolders:
  - `components/analytics/` - tracking and analytics components
  - `components/animations/` - animation and motion components
  - `components/core/` - base UI components (buttons, inputs, cards, etc.)
  - `components/pages/` - page-level layout components
  - `components/providers/` - context providers and wrapper components
- Place utilities related to external services in `lib` directory
- Place utilities related to the project in `utils` directory
- Place hooks in `hooks` directory
- Place API utilities requests on `services` directory
- Use lowercase with dashes for directories (e.g., `components/auth-wizard`)
- Never read environment variables from .env or .env.local files directly, always use `process.env.VARIABLE_NAME`

## Components

- Use Server Components by default
- Mark client components explicitly with 'use client'
- Wrap client components in Suspense with fallback
- Use dynamic loading for non-critical components
- Implement proper error boundaries
- Place static content and interfaces at file end

## Performance

- Optimize images: Use WebP format, size data, lazy loading
- Minimize use of 'useEffect' and 'setState'
- Favor Server Components (RSC) where possible
- Use dynamic loading for non-critical components
- Implement proper caching strategies

## Data Fetching

- Use Server Components for data fetching when possible
- Implement proper error handling for data fetching
- Use appropriate caching strategies
- Handle loading and error states appropriately

## Routing

- Use the App Router conventions
- Implement proper loading and error states for routes
- Use dynamic routes appropriately
- Handle parallel routes when needed

## Forms and Validation

- Use Formik and Yup for form validation
- Implement proper server-side validation
- Handle form errors appropriately
- Show loading states during form submission

## State Management

- Minimize client-side state
- Use React Context sparingly
- Prefer server state when possible
- Implement proper loading states

## SEO and Metadata

- Follow existing project SEO patterns; if none exist, use `next-seo` package
- Create a reusable `SEO` component in `components/seo/` for consistency
- Define default metadata in root `layout.tsx`, override per-page as needed
- Include `title`, `description`, `canonical`, Open Graph, and Twitter Card metadata
- Use `noindex` for private/duplicate pages; JSON-LD for rich snippets when applicable
