# Portfolio Website Workshop from PolyU GCP

A modern, responsive portfolio website built with Next.js, TypeScript, and Tailwind CSS. This project is perfect for developers, students, and professionals who want to showcase their work and skills.

## 🚀 Features

- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices
- **Modern Tech Stack**: Built with Next.js 14, TypeScript, and Tailwind CSS
- **Easy Customization**: Simple configuration files to personalize your content
- **Fast Performance**: Optimized images and modern web practices
- **SEO Friendly**: Built-in SEO optimization with Next.js
- **Professional Components**: Header, project cards, buttons, and more

## 📋 Prerequisites

Before you begin, make sure you have the following installed on your computer:

### 1. Node.js and npm
- **Node.js** (version 18.0 or higher)
- **npm** (comes with Node.js)

**How to install:**
- Visit **[nodejs.org/en/download](https://nodejs.org/en/download)** 
- Click the green **"Get Node.js®"** button to download the LTS (recommended) version
- Follow the installation wizard (accept all default settings)
- **Verify installation** by opening terminal/command prompt and running:
  ```bash
  node --version
  npm --version
  ```
  You should see version numbers like `v18.17.0` and `9.6.7`

### 2. Code Editor
- **VS Code** (recommended): **[code.visualstudio.com](https://code.visualstudio.com/)**
- **Alternative editors**: WebStorm, Sublime Text, or any text editor of your choice

**VS Code Extensions (Optional but helpful):**
- ES7+ React/Redux/React-Native snippets
- Tailwind CSS IntelliSense
- TypeScript Importer

## 🛠️ Installation & Setup

### Step 1: Download the Project
```bash
# Option A: If you have git installed
git clone [your-repository-url]
cd portfolio-website

# Option B: Download ZIP file
# Download the ZIP file from the repository and extract it
# Navigate to the extracted folder in terminal/command prompt
```

### Step 2: Install Dependencies
```bash
# Install all required packages
npm install
```

This will install all the necessary packages including:
- **Next.js**: React framework for production
- **TypeScript**: Type-safe JavaScript
- **Tailwind CSS**: Utility-first CSS framework
- **Tabler Icons**: Beautiful icon library
- **React**: JavaScript library for building user interfaces

### Step 3: Run the Development Server
```bash
# Start the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to see your website!

## 📁 Project Structure

```
src/
├── app/                    # Next.js app directory
│   ├── page.tsx           # Home page
│   ├── layout.tsx         # Root layout
│   ├── about/             # About page
│   │   └── page.tsx
│   └── projects/          # Projects page
│       └── page.tsx
├── components/            # Reusable UI components
│   ├── Button.tsx         # Custom button component
│   ├── Header.tsx         # Navigation header
│   └── ProjectCard.tsx    # Project display card
├── images/                # Image assets
│   ├── avatar.jpg         # Your profile picture
│   ├── hero-image.jpg     # Main hero image
│   └── about.jpg          # About page image
├── misc/                  # Configuration and data
│   └── data.ts           # Your projects and content data
└── styles/               # Styling
    └── tailwind.css      # Tailwind CSS configuration

public/                   # Static files
└── resume.pdf           # Your resume/CV file
```

## 🎨 Customizing Your Portfolio

### 1. Personal Information (`src/app/page.tsx`)

Edit the main page content:

```typescript
// Find these lines and update with your information
<h1 className="text-4xl mt-6 font-bold tracking-tight text-zinc-800 sm:text-5xl">
  Your Title Here (e.g., "Full-stack Developer & Designer")
</h1>

<p className="mt-6 text-base text-zinc-600 font-light">
  Your personal description here...
</p>
```

### 2. Projects Data (`src/misc/data.ts`)

Add your own projects:

```typescript
export const projects = [
  {
    name: "Your Project Name",
    description: "Brief description of your project and what it does.",
    href: "https://github.com/yourusername/project", // Link to your project
    icon: IconBrandGithub, // You can change this icon
  },
  // Add more projects...
];
```

**Available Icons:**
- Browse [Tabler Icons](https://tabler.io/icons) for more options
- Import them at the top: `import { IconName } from "@tabler/icons-react";`

### 3. Images

Replace the default images with your own:

- **Profile Picture**: Replace `src/images/avatar.jpg` with your photo
- **Hero Image**: Replace `src/images/hero-image.jpg` with your preferred image
- **About Image**: Replace `src/images/about.jpg` 
- **Resume**: Replace `public/resume.pdf` with your CV

**Image Requirements:**
- **Avatar**: Square format (e.g., 400x400px) for best results
- **Hero Image**: Landscape format (e.g., 800x600px)
- **Supported formats**: JPG, PNG, WebP

### 4. About Page (`src/app/about/page.tsx`)

Customize your about page with your personal story, skills, and experience.

### 5. Color Scheme

The website uses Tailwind CSS. To change colors:

```typescript
// Example: Change text colors
className="text-zinc-800"  // Dark text
className="text-zinc-600"  // Medium text
className="text-blue-600"  // Blue accent

// Example: Change background colors
className="bg-zinc-100"    // Light background
className="bg-blue-500"    // Blue background
```

### 6. Header Navigation (`src/components/Header.tsx`)

Add or modify navigation links:

```typescript
// Find the navigation section and modify links
<Link href="/your-new-page">Your New Page</Link>
```

## 🚀 Building for Production

When you're ready to deploy your website:

```bash
# Build the production version
npm run build

# Test the production build locally
npm start
```

## 📦 Deployment Options

### 1. AWS Amplify (Recommended - Professional)

[AWS Amplify](https://aws.amazon.com/amplify/) provides everything you need to deploy web and mobile apps with enterprise-grade features. It offers **zero-config Next.js deployments** with global availability and automatic scaling.

### 2. Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.




### Pre-Deployment Checklist
Before deploying to production:

```bash
# 1. Test your build locally
npm run build
npm start

# 2. Check for any console errors
# 3. Test on different devices and browsers
# 4. Optimize images (use tools like TinyPNG)
# 5. Update all placeholder content with your real information
# 6. Verify all links work correctly
# 7. Test contact forms and external links
```

### Production Optimizations(Optional)
```typescript
// Add to next.config.mjs for better performance
const nextConfig = {
  images: {
    formats: ['image/webp', 'image/avif'],
    minimumCacheTTL: 60,
  },
  compress: true,
  poweredByHeader: false,
}
```

## ❗ Troubleshooting

### Common Issues:

**1. "Module not found" errors**
```bash
# Delete node_modules and reinstall
rm -rf node_modules package-lock.json
npm install
```

**2. Port 3000 already in use**
```bash
# Use a different port
npm run dev -- -p 3001
```

**3. Images not loading**
- Check file paths are correct
- Ensure images are in the `src/images/` or `public/` folder
- Use supported formats (JPG, PNG, WebP)

**4. Build errors**
```bash
# Check for TypeScript errors
npm run lint
```

**5. AWS Amplify Deployment Issues**
```bash
# If Amplify build fails, check these:
# - Ensure Node.js version is specified in package.json
# - Verify all dependencies are in package.json (not devDependencies)
# - Check build logs in Amplify console for specific errors

# Add Node.js version to package.json:
"engines": {
  "node": ">=18.0.0"
}
```

**6. Environment Variables**
```bash
# For sensitive data (API keys, etc.), add in Amplify Console:
# App Settings → Environment Variables
# Never commit sensitive data to your repository
```

## 📚 Learning Resources

- **Next.js Documentation**: [nextjs.org/docs](https://nextjs.org/docs)
- **Tailwind CSS**: [tailwindcss.com/docs](https://tailwindcss.com/docs)
- **TypeScript**: [typescriptlang.org/docs](https://typescriptlang.org/docs)
- **React**: [react.dev](https://react.dev)

## 🤝 Contributing

Feel free to fork this project and customize it for your needs! If you find bugs or have suggestions for improvements, please create an issue or submit a pull request.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

**Happy coding! 🚀**

*Need help? Check the troubleshooting section above or create an issue in the repository.*
