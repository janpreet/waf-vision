# WAF Vision: A Simple Guide 🛡️

## What This Tool Actually Does

This is a simulation tool that helps visualize how web security works. It shows some real information about your connection mixed with simulated security checks.

### What's Real:
- Your browser type
- Current time
- Your actual User Agent (browser information)
- Basic IP detection

### What's Simulated:
- Security checks and results
- Rule violations
- Processing times
- Security alerts

### What's Experimental (May Not Work):
- Privacy/Apple Relay detection
- VPN detection
- Private mode detection

## How WAF Vision Works When You Visit

1. **Initial Contact**
   - Checks your connection details.
   - Detects if you’re using privacy tools like Apple Relay.
   - Gets your IP address.

2. **Security Processing**
   - Runs through each WAF rule (e.g., SQL injection, Apple Relay).
   - Marks passed or failed checks.
   - Records the results for stats.

3. **Display and Updates**
   - Shows gathered data in an easy-to-read format.
   - Highlights which security checks passed or failed.
   - Updates visitor stats based on results.

## How Each Part Works

### 1. IP Detection
```javascript
getUserIP() // Tries to find where you're connecting from
```
- Uses ipify API to get your IP address
- Might show "IP Detection Failed" if the service is unreachable
- Like asking "what's your address?" but for the internet

### 2. Browser Information
```javascript
navigator.userAgent // Gets your real browser details
```
- Shows if you're using Chrome, Safari, Firefox, etc.
- Displays your actual browser information
- Think of it as your browser's ID card

### 3. Request Details
```javascript
generateRequestDetails() // Collects visit information
```
Shows:
- Real time of your visit
- Your actual browser details
- Simulated page requests (randomly picked from a list)
- Simulated request types (GET, POST, etc.)

### 4. Security Rules (WAF Rules)
```javascript
wafRules // Pretend security checkpoints
```
Simulates checking for:
- SQL Injection (database attacks)
- XSS (malicious scripts)
- Rate Limiting (too many requests)
- Geographic Filtering (location checks)
- Input Validation (dangerous content)

Each rule:
- Has an 80% chance of passing
- Shows a simulated processing time
- Displays helpful tips when you hover

### 5. Results Display
```javascript
displayRequestInfo() // Shows what is known about you
displayWAFResults() // Shows simulated security results
```
- Organizes information in easy-to-read panels
- Uses color coding for results
- Provides helpful tooltips on hover

### 6. Statistics Tracking
```javascript
stats // Keeps count of what happened
```
Tracks:
- Number of simulations run
- How many checks "failed"
- How many privacy services detected

## Common Security Terms Explained

- **WAF**: Web Application Firewall - the website’s security guard.
- **IP Address**: Internet address of your connection - like your home address for the web.
- **Apple Relay**: Apple’s tool to hide your real location - similar to forwarding mail.
- **VPN**: Virtual Private Network - a private connection tunnel.
- **User Agent**: Information about your browser type.

## Color Guide

- **Green** = Check passed
- **Red** = Check failed
- **Yellow** = Information alert
- **Gray** = General information

## Features

### Auto-Refresh
```javascript
toggleAutoRefresh() // Runs new simulations automatically
```
- Updates every 3 seconds when turned on
- Shows different results each time
- Can be turned on/off with a button

### Tooltips
- Hover over any item to see more information
- Explains what each check means
- Provides security tips

## Important Notes

1. **This is a Learning Tool**
   - Does not provide actual security
   - All security checks are simulated
   - Used to understand how WAFs work

2. **Privacy Note**
   - Cannot reliably detect all privacy services
   - Privacy detection is experimental
   - No data is stored or shared

3. **Real vs Simulated**
   - Browser info is real
   - Security checks are simulated
   - Results are randomized

---
Built by [Janpreet](https://github.com/janpreet)
*A learning tool for understanding web security*