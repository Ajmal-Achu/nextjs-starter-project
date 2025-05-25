# KS Islamic Center App - Detailed Implementation Plan

## Information Gathered
- The app is a Next.js project with an empty src/app directory except for globals.css.
- The app requires multiple pages and features including splash, onboarding, authentication, home feed, explore, post, learn, teach, messages, profile, admin dashboard, settings, and notifications.
- RTL support for Arabic language is mandatory.
- Role-based access control: guest, student, teacher, volunteer, admin.
- Guest mode restrictions on interactions.
- Posts must include downloadable materials (PDF/DOC).
- Private chats limited to mutual followers.
- Use Tailwind CSS and Google Fonts for styling.
- Use lucid-react icons only if specified (not requested here).
- Create main app entry points layout.tsx and page.tsx.

## Plan

### 1. Main App Entry Points
- `src/app/layout.tsx`: Setup global layout, language toggle, theme toggle, RTL support, and main navigation.
- `src/app/page.tsx`: Splash screen with logo, tagline, loading animation, and optional language selection.

### 2. Authentication Pages
- `src/app/auth/login/page.tsx`: Login form with email, password, social login, links, language toggle.
- `src/app/auth/register/page.tsx`: Registration form with full name, email, password, confirm password, language toggle, auto-login after registration.
- Role application buttons at bottom of login and profile pages.

### 3. Home Feed
- `src/app/home/page.tsx`: TikTok-style vertical scroll of video/image posts with interactions (like, comment, share, download).
- Guest mode disables interactions with banner prompt.

### 4. Explore Page
- `src/app/explore/page.tsx`: Search bar, user cards grid/list with profile picture, name, role badge, follow/unfollow button.
- Profile view with banner, bio, followers, posts, message button (mutual follow).

### 5. Post Tab (User/Creator)
- `src/app/post/page.tsx`: Post request form with title, description, video upload, downloadable file upload, optional thumbnail, submit for approval.
- List of user posts with status and rejection message.

### 6. Learn Tab (Student Only)
- `src/app/learn/page.tsx`: Learning dashboard with welcome message, levels, course cards, tabs for courses, downloads, progress, exams, certificates.

### 7. Teach Tab (Teacher Only)
- `src/app/teach/page.tsx`: Teaching dashboard with my courses, create new course, course builder form, tabs for courses, students, grading, messages.

### 8. Messages Page
- `src/app/messages/page.tsx`: Private 1-on-1 chat interface with text, emojis, image/file upload, scrollable history.
- Chat list view with profile pic, name, last message preview.

### 9. Profile Page
- `src/app/profile/page.tsx`: Profile photo, name, bio, role, edit profile, my posts, followers/following, apply to role buttons and multi-step application form.

### 10. Admin Dashboard
- `src/app/admin/page.tsx`: Application review, post moderation, announcement system, analytics view.

### 11. Settings Page
- `src/app/settings/page.tsx`: Language, theme, notification preferences, terms & privacy, logout.

### 12. Notification System
- Notification tab/dropdown with types: post status, messages, role application status, announcements, comments/likes.

## Dependent Files to be Created/Edited
- Main app entry points: layout.tsx, page.tsx
- Pages under src/app for each feature as above
- Shared components for UI elements (buttons, forms, cards, modals, etc.)
- Hooks for language toggle, RTL support, auth state, role management
- Utilities for API calls, file uploads, notifications
- Tailwind CSS configuration for RTL and theme support

## Follow-up Steps
- Implement main layout and splash page first
- Implement authentication pages and role application
- Implement home feed and explore pages
- Implement post, learn, teach tabs
- Implement messages, profile, admin, settings, notifications
- Test RTL support and role-based access
- Test guest mode restrictions and private chats
- Final styling and responsiveness

---

Please confirm if you approve this detailed plan so I can proceed with implementation.
