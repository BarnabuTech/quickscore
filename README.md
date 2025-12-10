# QuickScore

**AI-Powered Instant Loan Assessment Platform**

QuickScore is a modern fintech application that revolutionizes the loan application process by leveraging artificial intelligence to provide instant credit assessments. Built with Next.js and powered by Google Gemini AI, the platform enables borrowers to get loan decisions in minutes instead of days.

## 🎯 Key Features

### For Borrowers (Individual & Business)
- **AI Identity Verification**: Real-time liveness detection and ID document verification using Gemini Vision API
- **Smart Financial Analysis**: Automatic analysis of M-Pesa transactions and bank statements
- **Instant Credit Assessment**: AI-powered credit scoring with personalized loan recommendations
- **Seamless Onboarding**: Step-by-step guided application process with progress tracking
- **Multiple Dashboards**: Separate interfaces for individual borrowers, business borrowers, and lenders

### For Lenders
- **Application Management**: Review and manage loan applications with AI recommendations
- **Risk Assessment**: Automated flagging of high-risk applications with detailed reasons
- **Smart Insights**: AI-generated approval/rejection recommendations with confidence scores
- **Real-time Analytics**: Track application trends and decision metrics

## 🚀 Technology Stack

- **Frontend**: Next.js 15, React 18, TypeScript
- **UI Components**: shadcn/ui, Tailwind CSS
- **AI/ML**: Google Gemini 1.5 Pro (via Genkit AI)
- **Data Visualization**: Recharts
- **Form Management**: React Hook Form, Zod validation
- **Authentication**: Simplified role-based routing (prototype mode)

## 🤖 AI Capabilities

### Identity Verification
- Liveness detection to prevent spoofing
- ID document forgery detection
- Face matching between live photo and ID
- Confidence scoring for each verification step

### Financial Analysis
- M-Pesa transaction pattern analysis
- Income stability assessment
- Spending behavior insights
- Debt-to-income ratio calculation

### Credit Assessment
- Weighted scoring algorithm (Identity 30%, Income 25%, Spending 20%, Savings 15%, Debt 10%)
- Risk level determination (Low/Medium/High)
- Personalized loan amount recommendations
- Interest rate calculation based on creditworthiness

## 📁 Project Structure

```
src/
├── ai/                        # AI services and flows
│   ├── services/             # Core AI processing logic
│   │   ├── identity-verification.ts
│   │   ├── financial-analysis.ts
│   │   └── credit-assessment.ts
│   └── flows/                # Genkit AI flows
├── app/                      # Next.js app directory
│   ├── api/                  # API routes
│   │   └── ai/              # AI processing endpoints
│   ├── borrower/            # Individual borrower flows
│   ├── business-borrower/   # Business borrower flows
│   ├── lender/              # Lender interface
│   └── auth/                # Authentication pages
├── components/              # React components
│   ├── borrower/           # Borrower-specific components
│   ├── lender/             # Lender-specific components
│   ├── shared/             # Shared components
│   └── ui/                 # shadcn/ui components
└── lib/                    # Utility functions and data
```

## 🛠️ Getting Started

### Prerequisites
- Node.js 18+ 
- npm or yarn
- Google AI API key (for Gemini)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/mikesplore/quickscore.git
cd quickscore
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
```bash
cp .env.example .env.local
```
Add your Google AI API key to `.env.local`:
```
GOOGLE_GENAI_API_KEY=your_api_key_here
```

4. Run the development server:
```bash
npm run dev
```

5. Open [http://localhost:3000](http://localhost:3000) in your browser.

## 🎨 User Flows

### Individual Borrower Onboarding
1. **Identity Verification**: Liveness check + ID upload
2. **Personal Details**: Basic information collection
3. **Financial Connection**: M-Pesa or bank account linking
4. **AI Assessment**: Instant credit score and loan offers

### Business Borrower Onboarding
1. **Business Information**: Company details and registration
2. **Representative Verification**: Owner/director identity check
3. **Business Financials**: Revenue and expense analysis
4. **Document Upload**: Business certificates and statements
5. **AI Assessment**: Business credit score and financing options

### Lender Workflow
1. **Dashboard Overview**: Application metrics and trends
2. **Application Queue**: Review pending applications with AI insights
3. **Applicant Profiles**: Detailed view with AI recommendations
4. **Decision Making**: Approve, flag, or reject with explanations

## 🔐 Security & Privacy

- **No Credential Storage**: Never stores passwords or PINs
- **Read-Only Access**: Only reads transaction data, cannot perform transactions
- **Data Encryption**: All sensitive data encrypted in transit
- **AI Processing**: Identity verification happens server-side with secure API calls

## 📊 AI Assessment Metrics

The platform analyzes multiple factors to generate credit scores:

- **Identity Score** (30%): Liveness detection, document authenticity, face matching
- **Income Score** (25%): Stability, consistency, source verification
- **Spending Score** (20%): Patterns, categories, responsibility
- **Savings Score** (15%): Average balance, trends, emergency fund
- **Debt Score** (10%): Existing obligations, payment history, utilization

## 🚧 Development Status

This is a prototype/MVP demonstrating AI-powered loan assessment capabilities. Key features implemented:

✅ Complete onboarding flows (individual & business)
✅ AI-powered identity verification
✅ Financial data analysis
✅ Credit assessment engine
✅ Dashboard interfaces for all user types
✅ Application management for lenders
✅ Real-time processing indicators

## 📝 License

This project is part of a demonstration/portfolio and is not intended for production use without proper financial regulations compliance and security audits.

## 👨‍💻 Author

**Mike Wachira**
- GitHub: [@mikesplore](https://github.com/mikesplore)

## 🙏 Acknowledgments

- Google Gemini AI for vision and language models
- shadcn/ui for beautiful UI components
- Next.js team for the amazing framework
