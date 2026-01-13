# Atoshi

A collaborative chat-based assistant that helps groups plan and organize activities together.

## Overview

Atoshi is a chatbot that participates in group conversations, listens to discussions, and contributes meaningful suggestions when appropriate. The initial use case focuses on helping a group of people plan a trip to Japan.

## High-Level Requirements

### Group Chat Interface
- Multiple people can join a shared chat room
- Users discuss topics collaboratively (e.g., planning a trip to Japan)
- The bot participates as a member of the chat, listening and contributing when helpful

### Privacy-First Personal Memory
- The bot connects with each user individually to request consent for storing personal information
- Users who do not give consent will not have their information recorded
- Only consenting users' information is remembered and utilized

### Personalized Assistance
- For users who have given consent, the bot remembers their personal information
- The bot uses this knowledge to provide personalized help in their daily lives
- When planning group activities (like the Japan trip), the bot leverages everyone's preferences and constraints to create better plans

### Trip Planning (Initial Use Case)
- Help a group of 5 people plan a trip to Japan
- Consider each person's preferences, schedules, and requirements
- Provide suggestions for itineraries, accommodations, and activities
