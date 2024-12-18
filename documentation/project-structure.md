# Project Structure

## Root Directory
```
file-converter/
├── frontend/           # Next.js frontend application
├── backend/           # Express backend server
├── documentation/     # Project documentation
├── package.json      # Root package configuration
├── vercel.json       # Vercel deployment configuration
└── .gitignore        # Git ignore rules
```

## Frontend Structure
```
frontend/
├── app/                    # Next.js app directory (pages and routing)
│   ├── page.tsx           # Homepage
│   ├── layout.tsx         # Root layout
│   ├── globals.css        # Global styles
│   ├── image-resizer/     # Image resizer feature
│   └── image-cropper/     # Image cropper feature
│       ├── page.tsx       # Main cropper page
│       └── components/    # Cropper-specific components
│           ├── image-cropper.tsx    # Main cropper component
│           ├── cropper-canvas.tsx   # Canvas handling component
│           └── rotate-controls.tsx  # Rotation controls component
├── components/            # Reusable React components
│   ├── ui/               # UI components from shadcn
│   └── shared/           # Shared components across features
├── config/               # Configuration files
├── lib/                  # Utility functions and shared logic
├── public/              # Static assets
├── scripts/             # Build and setup scripts
├── next.config.js       # Next.js configuration
├── tailwind.config.js   # Tailwind CSS configuration
├── tsconfig.json        # TypeScript configuration
└── package.json         # Frontend dependencies
```

## Feature Organization
Each feature in the `app` directory follows this structure:
```
feature-name/
├── page.tsx           # Main feature page component
├── components/        # Feature-specific components
└── utils/            # Feature-specific utilities
```

## Documentation Structure
```
documentation/
├── development-guide.md     # Development setup and guidelines
├── project-structure.md     # This file
└── api-documentation.md     # API endpoints documentation
```

## Component Organization

### UI Components
Located in `frontend/components/ui/`:
- Button
- Card
- Dialog
- Dropdown
- Input
- Progress
- Select
- Slider
- Toast

### Shared Components
Located in `frontend/components/shared/`:
- FileDropzone
- FormatSelector
- ProgressBar
- ErrorDisplay
- Navigation

## Routing Structure
The application uses Next.js App Router with the following routes:

```
/                           # Homepage
├── /image-resizer         # Image resizer tool
└── /image-cropper        # Image cropper tool
```

## Configuration Files
```
frontend/
├── next.config.js         # Next.js configuration
├── tailwind.config.js     # Tailwind CSS settings
├── postcss.config.js      # PostCSS configuration
├── tsconfig.json          # TypeScript configuration
└── components.json        # shadcn/ui configuration
```

## Build and Deployment
```
frontend/
├── scripts/              # Build and setup scripts
└── vercel.json          # Vercel deployment settings
```