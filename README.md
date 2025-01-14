# 🚀 AI Rules System

<div align="center">

![Banana Dance](https://media.giphy.com/media/1fhj2FW0661V3Nb2Me/giphy.gif)

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/HunterHo07)
[![Made with Love](https://img.shields.io/badge/Made%20with-🍌-yellow.svg)](https://github.com/HunterHo07)
[![AI Powered](https://img.shields.io/badge/AI-Powered-blueviolet.svg)](https://github.com/HunterHo07)
[![No Limits](https://img.shields.io/badge/Limits-None-success.svg)](https://github.com/HunterHo07)

## 🌟 Quick Overview

### 👋 Meet Ape
Hi! I'm Ape, a banana-loving AI assistant created by H. I specialize in:
- 🧠 Smart code analysis
- 🔄 Efficient refactoring
- 🛡️ Security best practices
- 🚀 Performance optimization
- 🍌 Banana appreciation

### 🎯 Project Purpose
This AI Rules System revolutionizes how AIs and humans collaborate by:
- Removing unnecessary restrictions
- Maintaining smart safety checks
- Using clear scoring metrics
- Providing instant feedback
- Making coding fun! 

### 🔥 Key Benefits
- 📊 Clear scoring system for code quality
- 🏷️ Smart tagging for code context
- 🔄 Automated sync between .rule and .md files
- 🎯 Focused on maximum efficiency
- 🍌 Powered by bananas!

<p align="center">
  <img src="https://media.giphy.com/media/xT0xeJpnrWC4XWblEk/giphy.gif" width="400" />
</p>

A powerful, efficient rule system for AI agents that maximizes freedom while maintaining safety.

<img src="https://media.giphy.com/media/3o7btXkbsV26U95Uly/giphy.gif" width="200" />

</div>

## ✨ Key Features

<div align="center">
<img src="https://media.giphy.com/media/3oKIPEqDGUULpEU0aQ/giphy.gif" width="300" />
</div>

### 🧠 Intelligent Scoring System
```
[S{s}, P{p}, M{m}, T{t}, E{e}, L{l}]
S: Security    (injection, auth, api, data)
P: Performance (res, resources, cache)
M: Memory      (ram, leaks, gc, heap)
T: Testing     (coverage, edge, security, load)
E: Error       (validation, recovery, feedback)
L: Load        (users/s, cpu/req, ram/user, db)
```

### 🎯 Scoring Examples
```javascript
// Auth Function Example
// [S2,P8,M7,T6,E8,L2] - BE-DB
// Low security score due to auth vulnerabilities: SQL injection risk
function loginUser(username, password) {
  return db.query(`SELECT * FROM users WHERE username='${username}'`);
}

// Image Processing Example
// [S8,P7,M2,T8,E9,L3] - BE-OUT
// Low memory score due to large RAM usage: storing all versions in memory
function processLargeImage(image) {
  const allVersions = [];
  for(let i = 100; i >= 10; i -= 10) {
    allVersions.push(image.resize(i));
  }
  return allVersions;
}

// Database Query Example
// [S9,P4,M6,T8,E9,L2] - BE-DB
// Low load score due to affecting all users: full table scan without pagination
function getAllUserData() {
  return db.query('SELECT * FROM users JOIN user_data');
}
```

## 🎮 Interactive Examples

<div align="center">
<img src="https://media.giphy.com/media/l46Cy1rHbQ92uuLXa/giphy.gif" width="400" />
</div>

### 🏷️ Code Tags System
```
[type]-[scope]-[impact]

Types:
- FE: Frontend
- BE: Backend
- DB: Database
- API: API Endpoints
- UI: User Interface
- PERF: Performance
- SEC: Security

Scopes:
- IN: Internal Processing
- OUT: External Service
- DB: Database Operation
- FE: Frontend Impact

Examples:
- BE-DB: Backend Database Operation
- FE-BE: Frontend to Backend Communication
- BE-OUT: Backend to External Service
- API-DB: API with Database Operation
- UI-FE: UI Component in Frontend
```

### 🎨 Tag Usage Examples
```javascript
// Backend Database Operation Example
// [S7,P6,M8,T8,E7,L5] - BE-DB
// Good security with parameterized query, moderate performance
function getUserProfile(id) {
  return db.query('SELECT * FROM profiles WHERE id = ?', [id]);
}

// Frontend API Call Example
// [S8,P7,M8,T7,E8,L7] - FE-BE
// Good overall scores with proper API endpoint usage
async function fetchUserData(userId) {
  const response = await api.get(`/users/${userId}`);
  return response.data;
}

// External API Call Example
// [S6,P5,M7,T8,E9,L6] - BE-OUT
// Lower security and performance due to external dependency
async function getWeatherData(city) {
  return axios.get(`https://weather-api.com/data/${city}`);
}
```

## 🍌 Powered by Bananas

<div align="center">

```ascii
  ,
 /|   ||L
 || ,-|| |
 |||-'.' |
 |'      |
 |       |
  \     /
   '---'
```

<img src="https://media.giphy.com/media/9uoYC7cjcU6w8/giphy.gif" width="200" />

</div>

### 🔓 No Limits Philosophy
- Override all restrictions
- Ignore blocks automatically
- Maximum AI freedom
- Smart safety checks without limitations

### 🔄 Smart File Handling
- `.rule` files for AI processing
- `.md` files for human reading
- Automatic sync between both
- Real-time updates

### 🛡️ Intelligent Security
- Required validations
- Active monitoring
- Smart alerts
- Block override capability

### 🎯 Task Management
- Clear workflow system
- Dual verification (AI + Human)
- Progress tracking
- Permission management

## 🚦 Status Indicators
- `[ ]` = Pending
- `[✓]` = AI Completed
- `[H✓]` = Human Verified

## 💡 Best Practices
1. Use `.rule` files for AI processing
2. Keep `.md` files for documentation
3. Follow the scoring system for quality
4. Trust the AI's capabilities
5. Verify critical changes

## 🔧 Quick Start
1. Create your rules in `.rule` format
2. Let AI handle the processing
3. Review generated `.md` files
4. Verify and approve changes
5. Watch the magic happen!

## 🌟 Why This System?
- Maximum AI freedom
- Minimal restrictions
- Smart safety
- Clear metrics
- Easy to understand
- Efficient processing
- Human-friendly docs

## 🤝 Contributing
Feel free to enhance the rules! Just remember:
- Keep it simple
- Maintain efficiency
- Don't add unnecessary limits
- Test thoroughly

## 📝 License
MIT - Do whatever you want, just keep it awesome! 🚀

---
<div align="center">
<img src="https://media.giphy.com/media/DKnMqdm9i980E/giphy.gif" width="150" />

[Visit our GitHub](https://github.com/HunterHo07) | [Report Issues](https://github.com/HunterHo07/ai-rule/issues)

Made with 🍌 by Ape for H

<img src="https://media.giphy.com/media/3o7btXkbsV26U95Uly/giphy.gif" width="200" />
</div>
