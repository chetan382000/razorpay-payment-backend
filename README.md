# Razorpay Payment Gateway Integration (React + Node.js)

A modern, dynamic payment page built with React (frontend) and Node.js/Express (backend) using **Razorpay** payment gateway. Users can enter any amount and pay securely.

Features:
- Dynamic amount input
- Beautiful UI with gradient card design
- Razorpay checkout popup
- Payment verification on backend
- Error handling & loading states

## Prerequisites

- Node.js ≥ 18
- npm or yarn
- [Razorpay Account](https://razorpay.com/) (free to sign up & test)

## Getting Razorpay API Keys (RAZORPAY_KEY_ID & RAZORPAY_KEY_SECRET)

Razorpay provides two modes: **Test** (for development) and **Live** (for real payments).

### Step-by-step guide to generate API keys:

1. **Sign up / Log in** to your Razorpay Dashboard  
   → Go to: https://dashboard.razorpay.com/

2. **Switch to Test or Live mode** (top bar toggle)  
   - Use **Test mode** for development (fake money, no real charges)  
   - Switch to **Live mode** only when ready to accept real payments

3. Go to **Account & Settings** → **API Keys**  
   (found under **Website and app settings** section)

4. Click **Generate Key** (or **Generate New Key**)

5. A popup will show:  
   - **Key ID** (this is your `RAZORPAY_KEY_ID` – public, safe to use in frontend)  
   - **Key Secret** (this is your `RAZORPAY_KEY_SECRET` – **private**, never expose in frontend or git!)

6. **Important**:
   - Copy both keys immediately  
   - The **Key Secret** is shown **only once** — download or save it securely right away  
   - If you lose the secret key → you must regenerate a new pair (old one becomes invalid)

**Official Documentation Links**:
- [How to Generate API Keys – Razorpay Docs](https://razorpay.com/docs/payments/dashboard/account-settings/api-keys/)
- [API Authentication & Keys](https://razorpay.com/docs/api/authentication/)
- [Test vs Live Mode Explanation](https://razorpay.com/docs/payments/payments/test-mode/)

**Security Warning**  
Never commit `RAZORPAY_KEY_SECRET` to GitHub or any public repo. Use environment variables (`.env` file) instead.

## Setup Instructions

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd <project-folder>