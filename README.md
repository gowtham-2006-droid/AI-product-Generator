# 🎨 AI Marketing Creative Generator

> Transform your product images into stunning, professional marketing creatives in 30 seconds using AI.

[![Live Demo](https://ai-product-generator-self.vercel.app/)
[![GitHub](https://github.com/gowtham-2006-droid)
[![Made with AI](https://us2.make.com/1686778/scenarios/3766551/edit)


---

## 🌟 Overview

**AI Marketing Creative Generator** is an intelligent, no-code platform that democratizes professional marketing content creation. Small businesses, startups, and marketers can now generate high-quality, platform-optimized marketing creatives without design skills or expensive software.

### 🎯 The Problem

- **High Costs**: Professional designers charge $50-200 per creative
- **Time-Consuming**: Manual creation takes 2-4 hours per design
- **Skill Gap**: 78% of small businesses lack in-house design expertise
- **Scalability Issues**: Testing multiple variations is expensive and slow
- **Platform Complexity**: Each platform requires different formats and styles

### ✨ The Solution

Our AI-powered platform combines **Google Gemini 2.5** for intelligent prompt engineering with **Stability AI SDXL** for photorealistic image generation, orchestrated through **Make.com** workflows—all accessible through a simple web interface.

**Result**: Professional marketing creatives in 30 seconds for $0.02-0.04 each.

---

## 🚀 Features

### Core Capabilities

- **🤖 AI-Powered Prompt Engineering**
  - Google Gemini 2.5 Flash analyzes product context
  - Generates optimized Stable Diffusion prompts
  - Platform-specific optimization (Instagram, Facebook, LinkedIn, etc.)
  - Audience-targeted styling

- **🎨 Professional Image Generation**
  - Stability AI Stable Diffusion XL model
  - 8K resolution output (1024x1024)
  - Photorealistic product photography style
  - Blue-purple gradient brand aesthetic
  - Studio lighting simulation

- **📱 Platform Optimization**
  - 9+ platform presets
  - Format-specific composition (square, vertical, horizontal)
  - Text overlay space consideration
  - Platform aesthetic matching

- **⚡ Intelligent Workflow Automation**
  - Make.com no-code automation
  - 5-module processing pipeline
  - Webhook-based architecture
  - Real-time generation (30-60 seconds)

- **💰 Cost Efficiency**
  - 98% cheaper than hiring designers ($0.04 vs $200)
  - 95% faster than manual creation (30s vs 4 hours)
  - No subscription required for basic use
  - Pay-per-use model

---

## 🎬 Demo

### Live Application
**[Try it now →](https://your-project.vercel.app)**

### Video Demonstration
**[Watch 3-minute demo →](YOUR_YOUTUBE_LINK)**

### Screenshots

#### Main Interface
![Interface](https://via.placeholder.com/800x500/667eea/ffffff?text=Main+Interface)

#### Generated Creative Example
![Example](https://via.placeholder.com/800x500/764ba2/ffffff?text=Generated+Creative)

---

## 🏗️ Architecture

### System Overview
┌─────────────┐
│    USER     │
│ Web Browser │
└──────┬──────┘
│
│ 1. Submit Form (Product + Image)
↓
┌──────────────────┐
│  VERCEL FRONTEND │
│   (HTML/CSS/JS)  │
└────────┬─────────┘
│
│ 2. HTTP POST
↓
┌─────────────────────┐
│   MAKE.COM WEBHOOK  │
│     (Module 1)      │
└──────────┬──────────┘
│
│ 3. Trigger Workflow
↓
┌────────────────────────┐
│   GOOGLE GEMINI AI     │
│     (Module 2)         │
│ → AI Prompt Generation │
└──────────┬─────────────┘
│
│ 4. Optimized Prompt
↓
┌────────────────────────┐
│   STABILITY AI API     │
│     (Module 4)         │
│ → SDXL Image Generation│
└──────────┬─────────────┘
│
│ 5. Generated Image
↓
┌────────────────────────┐
│   SET VARIABLE         │
│     (Module 7)         │
│ → Format for Browser   │
└──────────┬─────────────┘
│
│ 6. Return Response
↓
┌────────────────────────┐
│   USER RECEIVES        │
│   Professional Creative│
└────────────────────────┘
⏱️ Total Time: 30-60 seconds
### Technology Stack

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **Frontend** | HTML5, CSS3, Vanilla JavaScript | User interface and interaction |
| **Hosting** | Vercel | Static site hosting with CDN |
| **Automation** | Make.com | No-code workflow orchestration |
| **AI - Prompts** | Google Gemini 2.5 Flash | Intelligent prompt engineering |
| **AI - Images** | Stability AI SDXL 1.0 | Professional image generation |
| **Version Control** | GitHub | Code repository and collaboration |

---

## 📦 Installation & Setup

### Prerequisites

- [Make.com](https://make.com) account (free tier works)
- [Google AI Studio](https://aistudio.google.com) API key
- [Stability AI](https://platform.stability.ai/) API key
- [Vercel](https://vercel.com) account (optional, for deployment)
- Git installed on your machine

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/ai-marketing-generator.git
cd ai-marketing-generator
2. Import Make.com Scenario
Log in to Make.com
Go to Scenarios → Create a new scenario
Click the "..." menu → "Import Blueprint"
Upload product-creative-generator.json from this repository
Click "Save"
3. Configure API Connections
Module 2: Google Gemini
Click the Gemini module
Click "Add" next to Connection
Get your API key from https://aistudio.google.com/app/apikey
Paste the key and save
Select model: gemini-2.5-flash
Module 4: Stability AI
Click the HTTP Request module
Update the Authorization header:
Bearer YOUR_STABILITY_API_KEY
Get your key from https://platform.stability.ai/account/keys
4. Get Your Webhook URL
Click Module 1 (Custom Webhook) in Make.com
Copy the webhook URL (looks like: https://hook.us2.make.com/xxxxx)
Save this for the next step
5. Update Frontend
Option A: Run Locally
Open index.html in a text editor
Find line ~271:
const WEBHOOK_URL = 'YOUR_MAKE_WEBHOOK_URL_HERE';
Replace with your actual webhook URL
Save the file
Open index.html in your browser
Option B: Deploy to Vercel
Push your code to GitHub:
git add .
git commit -m "Initial commit"
git push origin main
Go to Vercel Dashboard
Click "Add New..." → "Project"
Import your GitHub repository
Add environment variable:
Name: WEBHOOK_URL
Value: Your Make.com webhook URL
Click "Deploy"
6. Activate Make.com Scenario
In Make.com, toggle your scenario to ON (top right)
Save all changes
🎯 Usage
Step 1: Fill in Product Details
Product Name: Enter your product name (e.g., "Organic Coffee")
Description: Describe key features (e.g., "Premium single-origin beans")
Target Audience: Define your audience (e.g., "Health-conscious millennials")
Platform: Select where you'll use it (Instagram, Facebook, etc.)
Step 2: Upload Product Image
Click the upload area or drag & drop
Supports JPG, PNG, WEBP
Recommended: High-quality product photos
Maximum file size: 10MB
Step 3: Generate Creative
Click "Generate Creative"
Wait 30-60 seconds (first request may take longer)
Watch the loading animation
Step 4: Download & Use
Preview your AI-generated creative
See the AI prompt that was used
Review metadata (platform, size, generation time)
Click "Download Image" to save
Use in your marketing campaigns!
Platform-Specific Tips
Platform
Recommended Use
Best Practices
Instagram Post
Product showcases, lifestyle shots
Use vibrant colors, square format
Facebook Ad
Promotional campaigns
Clear product benefits, engaging
LinkedIn Post
B2B marketing, professional products
Corporate aesthetic, sophisticated
Pinterest Pin
Inspirational content
Vertical format, highly aesthetic
Email Newsletter
Hero images, product highlights
Clean, clickable, prominent product
🔧 Configuration
Customizing the Make.com Workflow
Adjust Image Quality (Module 4)
{
  "text_prompts": [...],
  "cfg_scale": 8,        // Prompt adherence (1-35, default: 7)
  "height": 1024,        // Image height
  "width": 1024,         // Image width
  "samples": 1,          // Number of images (1-4)
  "steps": 40,           // Quality steps (10-50, default: 30)
  "style_preset": "photographic"  // Visual style
}
Style Presets Available:
photographic (recommended for products)
digital-art
3d-model
cinematic
anime
enhance
Enhance Gemini Prompts (Module 2)
Modify the prompt template in Module 2 to adjust:
Style preferences
Color schemes
Composition rules
Platform-specific requirements
Frontend Customization
Change Brand Colors (in index.html CSS):
/* Line ~40 */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
/* Change to your brand colors */
Modify Supported Platforms:
<!-- Line ~290 -->
<option value="Instagram Post">Instagram Post</option>
<option value="Custom Platform">Custom Platform</option>
<!-- Add your platforms -->
📊 Project Structure
ai-marketing-generator/
├── index.html                          # Main application file
├── product-creative-generator.json     # Make.com blueprint
├── README.md                           # This file
├── LICENSE                             # MIT License
└── .gitignore                          # Git ignore rules
🐛 Troubleshooting
Common Issues
"Failed to generate creative"
Causes:
Make.com scenario is OFF
Invalid API keys
Webhook URL incorrect
Solutions:
Check Make.com scenario is toggled ON
Verify all API keys are valid
Check scenario execution history in Make.com
Ensure webhook URL is correct in index.html
Long Generation Time (60+ seconds)
Causes:
Stability AI model cold start
High server load
Solutions:
First request often takes 30-60 seconds (model loading)
Subsequent requests should be faster (15-30 seconds)
This is normal behavior for serverless AI models
Module 4 Fails in Make.com
Causes:
Expired Stability AI token
Insufficient credits
Invalid request format
Solutions:
Regenerate Stability AI API key
Check your credit balance at https://platform.stability.ai/account/credits
Verify Module 4 body format matches documentation
No Image Appears in Frontend
Causes:
Module 7 configuration error
Parse response setting incorrect
Solutions:
Check Module 4 has "Parse response: Yes"
Verify Module 7 variable value: data:image/png;base64,{{4.artifacts[1].base64}}
Check browser console for errors (F12)
Getting Help
Issues: Open an issue
Discussions: Join discussions
Email: your.email@example.com
💰 Cost Analysis
Per Creative Costs
Method
Cost
Time
Quality
Freelance Designer
$50-200
2-4 hours
High
Design Agency
$200-500
1-3 days
Very High
DIY (Canva Pro)
$13/month + time
30-60 min
Medium
Our AI Generator
$0.02-0.04
30 seconds
High
Monthly Comparison (100 creatives)
Traditional Design: $5,000-20,000 + weeks of time
Our Solution: $2-4 + 50 minutes total
Savings: ~98% cost reduction, ~95% time reduction
🗺️ Roadmap
Phase 1: MVP ✅ (Completed)
[x] Basic creative generation
[x] Platform optimization
[x] Web deployment
[x] Make.com automation
Phase 2: Enhanced Features (Q1 2026)
[ ] A/B testing (generate multiple variations)
[ ] Batch processing (upload multiple products)
[ ] Custom brand templates
[ ] Brand color extraction from logo
Phase 3: Advanced AI (Q2 2026)
[ ] Video ad generation
[ ] Multi-language support
[ ] Background removal
[ ] AI-powered copy generation
Phase 4: Platform Integration (Q3 2026)
[ ] Direct social media posting
[ ] Analytics dashboard
[ ] Shopify/WooCommerce plugins
[ ] API for developers
Phase 5: Enterprise (Q4 2026)
[ ] Team collaboration features
[ ] Brand guidelines enforcement
[ ] White-label solution
[ ] Custom model training
🤝 Contributing
Contributions are welcome! Please follow these steps:
Fork the repository
Create a feature branch
git checkout -b feature/AmazingFeature
Commit your changes
git commit -m 'Add some AmazingFeature'
Push to the branch
git push origin feature/AmazingFeature
Open a Pull Request
Contribution Guidelines
Follow existing code style
Add comments for complex logic
Update README if adding features
Test thoroughly before submitting
Include screenshots for UI changes
📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
MIT License

Copyright (c) 2026 [Your Name]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software...
🙏 Acknowledgments
Technologies & Services
Make.com - Workflow automation platform
Google Gemini - AI prompt generation
Stability AI - SDXL image generation
Vercel - Hosting and deployment
GitHub - Version control
Inspiration
HackNova - Google Developer Group On Campus Hackathon
Open Innovation - Problem statement focus
Special Thanks
Google Developer Group On Campus community
Open source contributors
Beta testers and early adopters
📞 Contact
Project Maintainer: [Your Name]
GitHub: @YOUR_USERNAME
Email: your.email@example.com
LinkedIn: Your LinkedIn
Project Links:
Live Demo: https://your-project.vercel.app
Repository: https://github.com/YOUR_USERNAME/ai-marketing-generator
Issues: https://github.com/YOUR_USERNAME/ai-marketing-generator/issues
📈 Stats
�
�
�
Load image
🌟 Star History
�
Load image
�

Made with ❤️ and AI
⭐ Star this repo if you find it helpful!
Report Bug · Request Feature · Documentation
�
```
