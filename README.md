# Wellesley Crave 🍽️

A comprehensive food tracking and dining hall navigation application built specifically for Wellesley College students. Track your meals, discover your favorite dishes, and get personalized dining recommendations based on your dietary preferences and allergens.

## Features

### 🔐 Secure Authentication
- Google OAuth integration with Wellesley email authentication
- Secure user profile management
- Personalized dashboard experience

### 🍽️ Smart Menu Navigation
- **Real-time Menu Data**: Integration with AVI Food Systems API for up-to-date dining hall menus
- **Multi-Location Support**: Coverage for all major dining halls (Tower, Bates, Bae, Stone D)
- **Meal-Specific Views**: Separate menus for Breakfast, Lunch, and Dinner
- **Time-Aware Interface**: Automatic meal suggestions based on current time

### 🥗 Personalized Food Tracking
- **Comprehensive Food Journal**: Log meals with detailed nutritional information
- **Macro Tracking**: Monitor calories, protein, carbohydrates, and fat intake
- **Custom Notes**: Add personal notes to meal entries
- **Historical Data**: View past food logs with date-specific filtering

### 🔔 Smart Notifications
- **Favorite Dish Alerts**: Get notified when your favorite dishes are available
- **Dining Hall Preferences**: Set your preferred dining hall for quick access
- **Personalized Recommendations**: Menu filtering based on your dietary needs

### 🚫 Allergy & Dietary Management
- **Comprehensive Allergen Database**: Support for 9 major allergens (Peanut, Soy, Dairy, Egg, Wheat, Sesame, Shellfish, Fish, Tree Nut)
- **Dietary Restrictions**: Filter for Vegetarian, Vegan, Gluten Sensitive, Halal, Kosher, and Lactose-Intolerant options
- **Smart Filtering**: Automatically hide incompatible menu items
- **Safety First**: Clear allergen warnings and ingredient information

### 📊 Advanced Analytics
- **Multiple Time Frames**: View nutrition data by day, week, month, or year
- **Interactive Visualizations**: Toggle between bar charts and pie charts for macro breakdowns
- **Dining Pattern Analysis**: Transition network graphs showing dining hall usage patterns
- **Activity Heatmaps**: Monthly logging activity visualization

### ⚙️ Customizable Settings
- **Favorite Dishes Management**: Add/remove favorite dishes with search functionality
- **Dining Hall Preferences**: Set default dining locations
- **Profile Customization**: Manage allergens and dietary restrictions
- **Data Synchronization**: Automatic cloud backup and sync

## Technology Stack

### Frontend
- **Streamlit**: Modern web application framework
- **Plotly**: Interactive data visualizations
- **Pandas**: Data manipulation and analysis

### Backend
- **SQLite**: Local database management
- **GitHub Integration**: Cloud storage and synchronization
- **OAuth2**: Secure authentication flow

### APIs & External Services
- **AVI Food Systems API**: Real-time dining hall menu data
- **Google OAuth**: Secure user authentication
- **GitHub API**: Database backup and synchronization

## Project Structure

```
wellesley-crave/
├── home.py                 # Main application entry point
├── food_journal.py         # Food logging and meal selection
├── metrics.py             # Analytics and data visualization
├── settings.py            # User preferences and configuration
├── auth.py                # Google OAuth authentication
├── user_profile.py        # User profile management
├── userWalkthrough.py     # New user onboarding
├── notification.py        # Favorite dish notifications
├── update_database.py     # Database operations
└── db_sync.py            # GitHub synchronization
```

## Installation & Setup

### Prerequisites
- Python 3.8+
- Streamlit
- Required Python packages (see requirements below)

### Required Packages
```bash
pip install streamlit pandas plotly requests authlib sqlite3
```

### Configuration
1. **Google OAuth Setup**:
   - Create a Google Cloud Project
   - Enable Google OAuth 2.0
   - Configure redirect URIs
   - Add credentials to Streamlit secrets

2. **GitHub Integration**:
   - Create a private repository for database storage
   - Generate a GitHub personal access token
   - Configure repository details in secrets

3. **Streamlit Secrets**:
   ```toml
   [google]
   client_id = "your_google_client_id"
   client_secret = "your_google_client_secret"
   redirect_uri = "your_redirect_uri"

   [github]
   token = "your_github_token"
   repo = "username/repo-name"
   db_path = "wellesley_crave.db"
   ```

## Usage

### Getting Started
1. **Login**: Use your Wellesley email to authenticate via Google OAuth
2. **Setup Profile**: Complete the initial walkthrough to set preferences
3. **Explore Menus**: Browse real-time dining hall menus
4. **Log Meals**: Track your food intake with detailed nutritional data
5. **View Analytics**: Monitor your eating patterns and nutritional trends

### Key Workflows

#### Logging a Meal
1. Navigate to "Select" tab in Food Journal
2. Choose date, dining hall, and meal type
3. Browse available menu items
4. Select desired dishes
5. Review nutritional summary in "Log" tab
6. Add meal notes and save entry

#### Setting Up Notifications
1. Go to Settings
2. Search and add favorite dishes
3. Set preferred dining hall
4. Configure allergen and dietary preferences
5. Receive notifications when favorites are available

#### Viewing Analytics
1. Access Metrics page
2. Choose time frame (Day/Week/Month/Year)
3. Toggle between chart types
4. Explore dining patterns and nutritional trends

## Data Privacy & Security

- **Local Storage**: All personal data stored locally and in private GitHub repository
- **Secure Authentication**: Google OAuth with Wellesley email verification
- **Data Encryption**: Secure transmission of all user data
- **No Third-Party Sharing**: Personal information never shared with external parties

## Contributing

This project was developed as a final project for CS 248 at Wellesley College. The codebase combines original development with adapted components from course materials and external sources, properly attributed throughout the code.

## Authors

Developed by Wellesley College students as part of CS 248 coursework, with guidance from Professor Eni and integration of course-provided authentication components.

## Acknowledgments

- Professor Eni for authentication framework and guidance
- AVI Food Systems for dining hall API access
- Wellesley College Dining Services for menu data
- ChatGPT for debugging assistance and visualization generation

## License

This project is for educational purposes as part of Wellesley College coursework.

---

*Built with ❤️ for the Wellesley College community*
