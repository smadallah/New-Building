# EduMarket Hub — Mobile App Design

## Overview

**EduMarket Hub** is a dual-purpose mobile app that combines an educational platform for tutoring and learning materials with a marketplace for buying and selling educational resources. The app serves teachers, students, and general users with distinct user flows for each role.

---

## Screen List

### Authentication & Onboarding
1. **Splash Screen** — App launch with logo and branding
2. **Sign In / Sign Up** — Email/password authentication with role selection
3. **Role Selection** — Choose between Teacher, Student, or Buyer/Seller
4. **Profile Setup** — Complete profile information based on role

### Core Navigation (Tab Bar)
5. **Home** — Personalized feed based on user role
6. **Explore / Browse** — Discover courses, tutors, and products
7. **Marketplace** — Buy and sell educational resources
8. **My Learning** — Enrolled courses, saved materials, wishlist
9. **Profile** — User account, settings, and preferences

### Educational Hub
10. **Course List** — Browse available courses and tutoring services
11. **Course Detail** — Full course description, instructor info, reviews, and enroll button
12. **Tutor Profile** — Tutor bio, qualifications, availability, and booking
13. **My Courses** — Enrolled courses, progress tracking, and materials
14. **Course Content** — Lessons, videos, PDFs, and assignments
15. **Assignment Submission** — Upload and submit assignments

### Marketplace
16. **Product List** — Browse educational products (books, notes, flashcards, etc.)
17. **Product Detail** — Product description, images, price, seller info, and reviews
18. **Seller Profile** — Seller information, ratings, and product listings
19. **Shopping Cart** — Review items before checkout
20. **Checkout** — Payment and delivery address
21. **Order Confirmation** — Order details and tracking
22. **My Sales** — For sellers: products listed, sales history, and earnings
23. **My Purchases** — Order history and download links

### Additional Screens
24. **Search** — Global search for courses, tutors, and products
25. **Notifications** — Course updates, order status, messages
26. **Messages** — Direct messaging with tutors, sellers, and students
27. **Settings** — App preferences, privacy, notifications, and logout

---

## Primary Content and Functionality

### Home Screen (Role-Based)

**For Students:**
- Recommended courses based on interests
- Upcoming tutoring sessions
- Recent learning materials
- Quick links to explore new content

**For Teachers:**
- Student enrollment notifications
- Course performance analytics
- Pending assignments to grade
- Income summary from marketplace sales

**For Buyers/Sellers:**
- Featured products
- Recent purchases and sales
- Trending educational resources
- Seller dashboard shortcuts

### Explore / Browse Screen
- **Search bar** at the top for quick access
- **Category filters** (Math, Science, Languages, etc.)
- **Sorting options** (Most popular, newest, highest rated)
- **Grid or list view** of courses/products
- **Infinite scroll** for pagination

### Marketplace Screen
- **Product categories** (Study notes, flashcards, books, past papers, etc.)
- **Product cards** with image, title, price, seller rating
- **Filter by price range, rating, and category**
- **Add to cart** functionality
- **Wishlist** for later purchase

### My Learning Screen
- **Enrolled courses** with progress bars
- **Saved materials** and notes
- **Wishlist** for future enrollment
- **Download materials** for offline access

### Profile Screen
- **User avatar and name**
- **Role badge** (Teacher, Student, Seller)
- **Account statistics** (courses enrolled, products sold, ratings)
- **Edit profile** button
- **Settings** and **Logout** options

---

## Key User Flows

### Student Enrolling in a Course
1. Student navigates to Explore → Courses
2. Browses or searches for a course
3. Taps on course card → Course Detail screen
4. Reviews course description, instructor, reviews, and price
5. Taps "Enroll Now" → Checkout (if paid)
6. Confirms enrollment → My Learning updated
7. Accesses course content immediately

### Teacher Publishing a Course
1. Teacher navigates to Profile → "Create Course"
2. Fills in course title, description, category, and price
3. Uploads course materials (videos, PDFs, assignments)
4. Sets course as "Live"
5. Course appears in Explore for students to discover
6. Teacher monitors enrollments and student progress

### Buyer Purchasing Educational Materials
1. Buyer navigates to Marketplace
2. Browses or searches for materials (e.g., "Biology notes")
3. Taps on product card → Product Detail
4. Reviews product description, seller rating, and price
5. Taps "Add to Cart"
6. Proceeds to checkout → Payment
7. Receives download link or digital delivery
8. Material available in "My Purchases"

### Seller Listing a Product
1. Seller navigates to Profile → "Sell Materials"
2. Creates new product listing (title, description, category, price)
3. Uploads product images and files
4. Sets product as "Active"
5. Product appears in Marketplace
6. Seller receives notifications when product is purchased
7. Seller views earnings in dashboard

---

## Color Choices

| Element | Color | Hex | Usage |
|---------|-------|-----|-------|
| **Primary** | Teal/Blue | #0a7ea4 | Buttons, links, highlights |
| **Background** | White (Light) / Dark Gray (Dark) | #ffffff / #151718 | Screen backgrounds |
| **Surface** | Light Gray (Light) / Darker Gray (Dark) | #f5f5f5 / #1e2022 | Cards, inputs |
| **Foreground** | Dark Gray (Light) / Light Gray (Dark) | #11181C / #ECEDEE | Primary text |
| **Muted** | Medium Gray | #687076 / #9BA1A6 | Secondary text |
| **Success** | Green | #22C55E | Confirmations, success states |
| **Warning** | Amber | #F59E0B | Warnings, alerts |
| **Error** | Red | #EF4444 | Errors, destructive actions |
| **Border** | Light Border | #E5E7EB / #334155 | Dividers, borders |

---

## Navigation Structure

### Tab Bar (Bottom Navigation)
- **Home** — Home screen
- **Explore** — Browse courses and products
- **Marketplace** — Buy and sell
- **My Learning** — Saved courses and materials
- **Profile** — User account

### Modal Flows
- **Sign In / Sign Up** — Full-screen modal
- **Checkout** — Modal with payment form
- **Messages** — Stack navigator for chat
- **Notifications** — Drawer or modal

---

## Design Principles

1. **Mobile-First** — All screens optimized for portrait orientation (9:16) and one-handed usage
2. **iOS-Like** — Follows Apple Human Interface Guidelines for consistency
3. **Clear Hierarchy** — Primary actions prominent, secondary actions accessible
4. **Accessibility** — Sufficient color contrast, readable text sizes, touch targets ≥ 44pt
5. **Performance** — Fast load times, lazy loading for lists, cached images
6. **Consistency** — Unified spacing, typography, and component styles across screens

---

## Implementation Notes

- Use **Expo Router** for navigation between screens
- Use **NativeWind (Tailwind CSS)** for styling
- Use **React Query** for data fetching and caching
- Use **AsyncStorage** for local persistence (user preferences, offline content)
- Use **Backend API** for user authentication, course data, and marketplace transactions
- Implement **Push Notifications** for course updates and order status
- Support **Dark Mode** with automatic theme switching

