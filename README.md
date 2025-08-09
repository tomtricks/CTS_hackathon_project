# Verizon International Plan Selector

A modern React component that provides a hybrid chat + comparison UI for selecting Verizon international travel plans. This component solves the pain point of fragmented plan selection flows by combining an intelligent chatbot assistant with a comprehensive comparison grid.

## ✨ Features

- **🤖 Smart Chatbot Assistant**: Guides users through destination, duration, and priority questions
- **📊 Dynamic Plan Filtering**: Automatically filters plans based on user responses
- **🎯 Comparison Grid**: Side-by-side plan comparison with detailed information
- **✅ Confirmation Flow**: Clean confirmation screen with plan summary
- **📱 Responsive Design**: Works perfectly on desktop and mobile devices
- **🎨 Verizon Branding**: Uses Verizon's red color scheme and modern design patterns

## 🚀 Quick Start

### Option 1: Demo HTML File (Fastest)
1. Open `demo.html` in your web browser
2. The component will load immediately with all dependencies from CDN

### Option 2: React Project Setup
1. Install dependencies:
   ```bash
   npm install
   ```
2. Import and use the component:
   ```jsx
   import InternationalPlanSelector from './InternationalPlanSelector';
   
   function App() {
     return <InternationalPlanSelector />;
   }
   ```

## 🛠 Component Architecture

### Step 1: Chatbot Interface
- **Left Panel**: Welcome message with Verizon branding
- **Right Panel**: Interactive chat with guided questions
- **Questions**: Destination, trip duration, and priorities
- **State Management**: Stores user responses for filtering

### Step 2: Plan Comparison
- **Filtered Results**: Shows only relevant plans based on chat responses
- **Plan Cards**: Display price, data allowance, country coverage, and perks
- **Smart Sorting**: Orders plans by user priority (cost, data, or premium features)
- **Interactive Selection**: Easy plan selection with hover effects

### Step 3: Confirmation
- **Plan Summary**: Shows all selected plan details
- **Pricing Breakdown**: Clear daily rate and feature overview
- **Actions**: Confirm selection or go back to modify

## 📋 Mock Data Structure

The component includes comprehensive mock data with 6 different plans:

```javascript
{
  id: 1,
  name: "Global Pass",
  price: 10,
  data: "500MB/day",
  countries: ["UK", "France", "Germany", "Italy", "Spain"],
  regions: ["Europe"],
  perks: "Unlimited calls & texts",
  duration: "1-7 days",
  priority: "budget"
}
```

## 🎯 Filtering Logic

The component intelligently filters plans based on:

1. **Destination Matching**: Filters by region (Europe, Asia, North America, Global)
2. **Duration Compatibility**: Matches trip length with plan duration limits
3. **Priority Alignment**: 
   - "Lowest cost" → Shows budget plans first
   - "Maximum data" → Prioritizes data-rich plans
   - "Premium features" → Highlights premium plans

## 🎨 Design System

- **Colors**: Verizon red (#DC2626) with gray neutrals
- **Typography**: Modern system fonts with clear hierarchy
- **Spacing**: Consistent padding and margins using Tailwind classes
- **Interactions**: Smooth hover effects and transitions
- **Icons**: Heroicons for consistent iconography

## 📱 Responsive Behavior

- **Desktop**: Full two-panel layout with chat sidebar
- **Tablet**: Stacked layout with optimized card grid
- **Mobile**: Single column with touch-friendly interactions

## 🔧 Customization

### Adding New Plans
Add new plan objects to the `mockPlans` array:

```javascript
{
  id: 7,
  name: "Your Plan Name",
  price: 20,
  data: "2GB/day",
  countries: ["Country1", "Country2"],
  regions: ["Region"],
  perks: "Your perks description",
  duration: "1-14 days",
  priority: "data" // "budget", "data", or "premium"
}
```

### Modifying Questions
Update the `questions` array to change chatbot flow:

```javascript
{
  key: 'newQuestion',
  text: 'Your question text?',
  options: ['Option 1', 'Option 2', 'Option 3']
}
```

### Styling Changes
The component uses Tailwind CSS classes. Key styling areas:

- **Brand Colors**: `bg-red-600`, `text-red-600`, `border-red-300`
- **Layout**: `grid`, `flex`, `space-y-*`, `gap-*`
- **Typography**: `text-*`, `font-*`
- **Interactive States**: `hover:*`, `transition-*`

## 🔄 State Management

The component uses React hooks for state management:

- `currentStep`: Controls the 3-step flow
- `chatAnswers`: Stores user responses from chatbot
- `selectedPlan`: Holds the chosen plan for confirmation
- `filteredPlans`: Contains plans filtered by user preferences
- `chatMessages`: Manages the conversation history
- `currentQuestion`: Tracks chatbot progress

## 🚀 Next Steps

To integrate this component into a production Verizon application:

1. **API Integration**: Replace mock data with real plan API
2. **Authentication**: Add user login and account integration
3. **Payment Flow**: Connect to Verizon's billing system
4. **Analytics**: Add tracking for user interactions and conversions
5. **A/B Testing**: Implement testing for different question flows
6. **Accessibility**: Add ARIA labels and keyboard navigation
7. **Internationalization**: Add multi-language support

## 📝 Files Included

- `InternationalPlanSelector.jsx` - Main React component
- `demo.html` - Standalone demo with CDN dependencies
- `package.json` - Project dependencies and scripts
- `README.md` - This documentation

## 🎉 Demo Flow

1. **Start**: User sees welcome screen with chat panel
2. **Chat**: Answer 3 questions about travel plans
3. **Compare**: View filtered plans in comparison grid
4. **Select**: Choose preferred plan
5. **Confirm**: Review and confirm selection

The entire flow is designed to be completed in under 2 minutes, significantly improving the user experience compared to traditional plan selection interfaces. 