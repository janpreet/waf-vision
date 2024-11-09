# WAF Vision 🛡️

A real-time Web Application Firewall (WAF) visualization tool for DevOps and Platform Engineers to demonstrate WAF request processing mechanics in action. Perfect for infrastructure discussions, security demonstrations, and developer onboarding.

## Why I Built This

As a Platform/DevOps Engineer, I often need to remind myself and explain WAF mechanics to different teams. While AWS WAF, Cloudflare, and other solutions are powerful, their inner workings can be opaque. I built WAF Vision to demonstrate WAF behavior in a clear, visual way that helps us understand what's happening behind the scenes when we implement WAF rules in our infrastructure.

## Core Functionality

- 🔍 Real-time HTTP request inspection
- 🌐 Client IP detection and geolocation
- 🕒 WAF rule processing pipeline visualization
- 📊 Rule violation metrics and analytics
- 🛡️ Simulated security rule evaluation
- 🔄 Infrastructure-as-Code ready

## Tech Stack

- Frontend: Vanilla JS & HTML
- Styling: Tailwind CSS v2.2.19
- External API: ipify for IP detection
- Hosting: GitHub Pages
