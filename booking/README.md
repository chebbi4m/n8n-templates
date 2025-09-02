# Booking Automation Templates

This folder contains n8n workflow templates for automated booking and reservation management systems.

## Available Templates

### `booking_template.json` - AI Booking Automation (Multi-Channel)

A comprehensive booking system that captures reservations from multiple channels and processes them with AI.

#### **What it does:**
- Captures bookings from 6 different channels: Website, Phone, WhatsApp, Messenger, Instagram, and Email
- Uses AI (OpenAI) to parse and extract booking details from natural language
- Stores all bookings in Google Sheets for easy management
- Sends automated confirmations, reminders, and follow-ups
- Routes responses back to the original channel

#### **Channels Supported:**
1. **Website Booking** - Webhook endpoint for online forms
2. **Phone Booking** - Twilio Voice integration for phone calls
3. **WhatsApp Booking** - Twilio WhatsApp integration
4. **Messenger Booking** - Facebook Messenger webhook
5. **Instagram Booking** - Instagram direct message webhook
6. **Email Booking** - Email webhook for email-based bookings

#### **Workflow Process:**
1. **Capture** - Receives booking requests from any channel
2. **Parse** - AI extracts structured data (name, date, time, guests, channel)
3. **Store** - Saves booking to Google Sheets
4. **Confirm** - Sends AI-generated confirmation message
5. **Remind** - Sends reminder 24 hours before booking
6. **Follow-up** - Sends thank you message 24 hours after booking

#### **Required Credentials:**
- **OpenAI API** - For AI parsing and message generation
- **Google Sheets API** - For storing booking data
- **Twilio API** - For phone and WhatsApp integration

#### **Configuration Required:**
- `YOUR_OPENAI_API` - Your OpenAI API key
- `YOUR_SHEET_ID` - Your Google Sheets ID
- `YOUR_GOOGLE_SHEETS_API` - Google Sheets API credentials
- `YOUR_TWILIO_API` - Twilio API credentials

#### **Google Sheets Setup:**
Create a sheet with columns:
- Column A: Name
- Column B: Date
- Column C: Time
- Column D: Guests
- Column E: Channel

#### **Webhook Endpoints:**
After importing, you'll get these webhook URLs:
- `/booking-web` - Website bookings
- `/booking-messenger` - Messenger bookings
- `/booking-instagram` - Instagram bookings
- `/booking-email` - Email bookings
- `/rebook` - Rebooking requests

#### **AI Features:**
- **Smart Parsing** - Extracts booking details from any format
- **Confirmation Messages** - Personalized confirmation texts
- **Reminder Messages** - Friendly reminder notifications
- **Follow-up Messages** - Thank you messages with rebooking offers

#### **Use Cases:**
- Restaurant reservations
- Hotel bookings
- Service appointments
- Event registrations
- Any business requiring booking management

#### **Benefits:**
- **Multi-channel** - Capture bookings from anywhere
- **AI-powered** - Handles natural language input
- **Automated** - Complete booking lifecycle automation
- **Centralized** - All bookings in one Google Sheet
- **Scalable** - Handles any volume of bookings
