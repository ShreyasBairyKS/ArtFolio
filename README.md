# ArtFolio 🎨

*The professional network for creatives. Showcase your projects and build your story.*

## About The Project

ArtFolio is an Android mobile application designed for artists, designers, musicians, and all creative professionals. It bridges the gap between a visual-first platform like Instagram and a corporate network like LinkedIn. 

The core problem ArtFolio solves is that creatives need a way to present a curated, professional narrative of their work that is more organized than a social media feed but easier to maintain than a personal website.

---

## ✨ Implemented Features

### 🔐 Authentication & User Management
- **Multi-Role System:** Support for 4 user types (Artist, Audience, Sponsor, Organisation)
- **Google Sign-In:** Seamless authentication with Firebase Auth
- **Guest Mode:** Preview functionality without sign-up (development feature)
- **Profile Management:** Edit bio, profile picture, and personal information
- **Account Deletion:** Secure account deletion with confirmation workflow

### 👤 Rich User Profiles
- **Role-Based Profiles:** Specialized data models for each user type
  - **Artists:** Portfolio URLs, art forms, reels, follower/following lists
  - **Audience:** Liked content, following artists, sponsor applications
  - **Sponsors:** Company name, budget range, sponsored programs
  - **Organisations:** Legal documents, event lists, sponsorship programs
- **Profile README:** Markdown-style bio editor with live preview
- **Follow System:** Follow/unfollow functionality with follower/following counts
- **Profile Sharing:** Share profile links via native share sheet

### 📝 Advanced Post Creation & Management
- **Multiple Post Types:** Image, Video, Reel, Idea, Gallery, Live
- **Visibility Controls:** Public, Private, Sponsors Only, Followers Only
- **Multi-Image Support:** Upload and manage multiple images per post (Gallery feature)
- **Image Editing:** Crop, rotate, and optimize images before upload
- **Rich Metadata:**
  - Title and detailed description
  - Skills tagging (e.g., #OilPainting, #DigitalArt)
  - Location tagging (city, state, country with coordinates)
  - Collaborator tagging
  - Sponsorship details
- **Draft Management:** Save and restore post drafts
- **Edit Posts:** Update existing posts with new images or content
- **Delete Posts:** Remove posts with cascade deletion of images

### 🎨 Comprehensive Engagement System
- **Likes:** Simple like/unlike with real-time counts
- **Comments:** Nested comment threads with user avatars
- **Kudos System:** Professional feedback with 8 types:
  - Great Composition 🎨
  - Inspiring Idea 💡
  - Amazing Colors 🌈
  - Technical Excellence ⚡
  - Creative Concept ✨
  - Beautiful Details 👁️
  - Unique Style 🎭
  - Professional Work ⭐
- **Share Functionality:** Share posts externally with rich previews
- **Save Posts:** Bookmark posts for later viewing with dedicated saved posts screen
- **View Tracking:** Track post views and engagement metrics

### 🔍 Discovery & Explore
- **Explore Page:** Three intelligent discovery modes
  - **Trending:** Posts with highest engagement (last 7 days)
  - **Diverse:** Curated mix of different skills and content types
  - **Latest:** Chronological feed of fresh content
- **Trending Algorithm:** Smart scoring based on:
  - Likes (1 point), Comments (3 points), Shares (5 points)
  - Kudos (4 points), Views (0.1 points)
  - Time decay factor for recency
- **Skill-Based Filtering:** Multi-select skill chips for targeted discovery
- **Popular Skills:** Dynamic skill recommendations based on trending content
- **Search Functionality:** Find users, posts, and content by keywords
- **Post Detail View:** Dedicated screen for individual posts with full engagement

### 💬 Real-Time Messaging
- **Direct Messages:** One-on-one chat with real-time updates
- **Conversations List:** Overview of all conversations with last message preview
- **Message Status:** Read/unread indicators
- **Typing Indicators:** Live typing status
- **New Message:** Start conversations from search results
- **Message Threading:** Organized conversation history

### 🔔 Notification System
- **In-App Notifications:** Comprehensive notification types:
  - Like, Kudos, Comment, Share notifications
  - Follow notifications
  - Collaboration requests
  - Sponsorship updates
  - Organisation updates
  - New messages
- **Notification Center:** Dedicated screen with pagination
- **Action Icons:** Contextual icons for each notification type
- **Deep Linking:** Navigate directly to relevant content

### 🎨 Design & Theming
- **Custom Brand Theme:** Color palette based on ArtFolio logo
  - Coral Red (Primary) #E85D52
  - Teal Green (Secondary) #60C4AE
  - Golden Yellow (Accent) #E2B444
  - Dark Teal #155E5C
  - Warm Neutral #3F3029
- **Dark/Light Mode:** System-aware theme switching with custom dark palette
- **Animated Splash Screen:** Polished app launch with logo animations
- **Google Fonts Integration:** Typography using Poppins and Lato
- **Responsive Design:** Screen size adaptation with flutter_screenutil
- **Custom Icons:** SVG icon support for crisp graphics

### 🛠️ Technical Infrastructure
- **Firebase Backend:**
  - **Firestore:** Real-time database with complex queries and indexes
  - **Firebase Storage:** Image hosting with progress tracking
  - **Firebase Auth:** Secure authentication with Google Sign-In
  - **Firebase App Check:** App security and anti-abuse
- **State Management:** Provider pattern with loading states
- **Image Optimization:**
  - Local caching with crypto-based keys
  - Lazy loading and pagination
  - Memory-efficient image handling
  - Progressive loading with placeholders
- **Error Handling:** Centralized error service with user-friendly messages
- **Validation Service:** Input validation for forms and user data
- **Session Management:** Guest mode and auth state handling
- **Asset Management:** Mock data loader for development

### 📱 Screen Architecture
**22 Fully Implemented Screens:**
1. Splash Screen (animated)
2. Authentication Screen
3. User Type Selection Screen
4. Home Screen (tab navigation)
5. Feed Screen (deprecated, replaced by Explore)
6. Improved Feed Screen
7. Explore Screen (with trending algorithm)
8. Create Post Screen
9. Edit Post Screen (via Create Post)
10. Post Detail Screen
11. Profile Screen (self and other users)
12. Edit Profile Screen
13. Profile README Editor Screen
14. Follow List Screen (followers/following)
15. Search Screen
16. Notifications Screen
17. Conversations Screen
18. Chat Screen (individual conversation)
19. New Message Screen
20. Saved Posts Screen
21. Image Gallery Screen
22. Delete Account Screen

### 🗂️ Data Models
**9 Comprehensive Models:**
- User (with role enum)
- Post (with engagement metrics, trending score)
- Comment
- Kudos (8 types with emojis)
- Message
- AppNotification (9 types)
- ProfileReadme (Markdown support)
- Role Models (Artist, Audience, Sponsor, Organisation)
- PostLocation (with coordinates)

### 🔧 Services & Utilities
**14 Service Classes:**
1. **AuthService:** Firebase authentication management
2. **FirestoreService:** Database CRUD operations (1600+ lines)
3. **StorageService:** Image upload/delete with progress
4. **MessagingService:** Real-time chat functionality
5. **UserService:** User data management
6. **TrendingService:** Discovery algorithms and recommendations
7. **SavedPostsService:** Bookmark functionality
8. **ShareService:** Native sharing integration
9. **ValidationService:** Input validation
10. **ErrorHandlerService:** Centralized error management
11. **ImageCacheService:** Local image caching
12. **FirestoreImageService:** Optimized image loading
13. **AssetLoader:** Mock data loading
14. **SessionState:** App state management
15. **AccountDeletionService:** Secure account removal

### 🎯 Advanced Features
- **Pagination:** Infinite scroll for feeds and lists
- **Pull to Refresh:** Manual data refresh in all feeds
- **Image Compression:** Automatic optimization before upload
- **Batch Operations:** Efficient multi-item updates
- **Optimistic Updates:** Instant UI feedback with rollback
- **Deep Linking:** Navigation from notifications
- **Share Sheet Integration:** Native OS sharing
- **Grid/List View Toggle:** Multiple viewing modes for profiles
- **Tab Navigation:** Bottom navigation with 5 tabs

---

## 🛠️ Tech Stack

* **Platform:** Android
* **Framework:** Flutter 3.35.4
* **Language:** Dart 3.9.2
* **Backend:** Firebase (Authentication, Firestore, Storage, App Check)
* **State Management:** Provider pattern with ValueNotifier
* **UI Libraries:** 
  - flutter_screenutil (responsive design)
  - google_fonts (typography)
  - flutter_svg (vector graphics)
* **Image Processing:** image_picker, image_cropper
* **Storage:** SharedPreferences (local data)
* **Utilities:** http, crypto, path, path_provider
* **Sharing:** share_plus

---

## 📋 Getting Started

### Prerequisites
- Flutter SDK (>=3.22.0)
- Dart SDK (>=3.9.0)
- Android Studio / VS Code
- Firebase account with project setup

### Installation

1.  **Clone the repository**
    ```sh
    git clone https://github.com/R-V-Abhishek/ArtFolio.git
    cd artfolio
    ```

2.  **Install dependencies**
    ```sh
    flutter pub get
    ```

3.  **Configure Firebase** (see `FIREBASE_SETUP_GUIDE.md`)
    - Set up Firebase Storage rules
    - Enable Anonymous Authentication
    - Create Firestore indexes
    - Add `google-services.json` to `android/app/`

4.  **Run the app**
    ```sh
    flutter run
    ```

### Firebase Setup
For detailed Firebase configuration, see **[FIREBASE_SETUP_GUIDE.md](FIREBASE_SETUP_GUIDE.md)**

Key requirements:
- Firebase Storage security rules
- Firestore composite indexes
- Anonymous authentication enabled
- Google Sign-In configured

---

## 📁 Project Structure

```
lib/
├── main.dart                 # App entry point
├── exceptions/              # Custom exceptions
├── models/                  # Data models (9 models)
├── providers/               # State management
├── routes/                  # Navigation and routing
├── screens/                 # UI screens (22 screens)
├── services/                # Business logic (14 services)
├── theme/                   # Theming and styling
└── widgets/                 # Reusable UI components

assets/
├── icons/                   # App icons and logo
├── images/                  # Static images
└── mock_posts.json         # Development mock data

docs/
├── auth_bypass.md          # Guest mode documentation
├── explore_page_implementation.md
└── LITERATURE_SURVEY.md    # Research and references
```

---

## 🚀 Future Enhancements

- Instagram API integration for post import
- Video upload and playback support
- Live streaming functionality
- Sponsorship marketplace
- Organisation event management
- Advanced analytics dashboard
- Push notifications
- Web and iOS versions

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

## 👥 Team

**Developer:** R-V-Abhishek , ShreyasBairyKS, GShreekar
**Repository:** [github.com/R-V-Abhishek/ArtFolio](https://github.com/R-V-Abhishek/ArtFolio)

---

## 📚 Documentation

- [Firebase Setup Guide](FIREBASE_SETUP_GUIDE.md)
- [Auth Bypass Documentation](docs/auth_bypass.md)
- [Explore Page Implementation](docs/explore_page_implementation.md)
- [Literature Survey](docs/LITERATURE_SURVEY.md)

---

**ArtFolio** - *Where creativity meets community* 🎨✨
