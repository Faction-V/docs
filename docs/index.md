# CAPITOL.ai Overview

Welcome to CAPITOL.ai! This document provides an overview of the three main ways you can integrate and use our services.

## Sections

- [LLM API](/llm-api)
- [User API](/user-api)
- [NPM Library](/npm-library)

## Usage Options

### 1. LLM API

CAPITOL.ai's LLM API allows you to create and manage your own stories with full control. When you create a story using the API, you will receive a WebSocket address, enabling you to stream the results in real-time. 

**Key Features:**

- **Full Control:** Manage your stories independently.
- **WebSocket Streaming:** Stream results directly from the provided WebSocket address.
- **Flexible Actions:** Perform any action on any story you own by tracking the response IDs.

[Learn more about the LLM API](#llm-api)

### 2. User API

The User API is designed to facilitate requests on behalf of a user or an organization. This API allows you to create stories, segment them by user or organization, and later query to retrieve these stories. 

**Key Features:**

- **User Segmentation:** Easily segment stories and reports for different users.
- **ACL Layer:** All requests are proxied through our LLM API with an additional Access Control Layer for user-specific management.
- **Story Management:** Create and retrieve stories tailored to your users' needs.

[Learn more about the User API](#user-api)

### 3. NPM Library

CAPITOL.ai offers a fully integrated, turnkey solution with our NPM library. This allows you to build reports on your website quickly and easily. The library makes it simple to create shareable reports that are editable only by the story's author.

**Key Features:**

- **Turnkey Solution:** Quickly integrate and start building reports on your website.
- **Report Sharing:** Share reports with others while maintaining control over edits.
- **Author-Only Editing:** Ensure that only the story author can make changes.

[Learn more about the NPM Library](#npm-library)
