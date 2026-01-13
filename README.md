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

## Platform Considerations

### WhatsApp Integration

WhatsApp is being considered as the primary chat platform due to its widespread adoption (2+ billion users).

**Integration Options:**
- **WhatsApp Business API (Meta Cloud API)** - Official solution requiring Meta business verification
- **Third-party platforms** - Services like Twilio, Wassenger, or BotPenguin that wrap the WhatsApp API

**Limitations:**
- The official WhatsApp Business API is primarily designed for 1:1 business-to-customer conversations
- Group chat support is limited in the official API (some third-party providers like Wassenger offer better group support)
- Requires business verification through Meta
- Promotional/marketing messages are prohibited (trip planning assistance should be acceptable)

**Pricing:**
- First 1,000 conversations per month are free
- Pay-per-conversation model after that

### Alternative Platforms

| Platform | Group Chat Support | Bot API | Verification Required |
|----------|-------------------|---------|----------------------|
| WhatsApp | Limited (via third-party) | Business API | Yes |
| Telegram | Native | Free Bot API | No |
| Discord | Native | Free Bot API | No |
| Slack | Native | Free Bot API | No |

**Telegram** may be a simpler alternative for prototyping due to its free, well-documented Bot API with native group chat support and no business verification requirement.

### Decision

Platform choice is still under consideration. The ideal solution should support:
- Group chat participation
- Direct messaging for consent collection
- Easy integration with AI/LLM backends
