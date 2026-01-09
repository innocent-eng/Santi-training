# Computer Basics Training App 💻

A comprehensive, full-featured training application for teaching computer basics, Windows shortcuts, and Microsoft Office applications. Built with React and designed for easy deployment on Google Colab.

## 🌟 Features

### Authentication System
- **User Login/Signup**: Secure authentication with role-based access
- **Admin Role**: Full content management capabilities
- **User Role**: Access to all learning materials with progress tracking

### Content Categories
1. **Computer Basics** - Fundamental computer concepts
2. **Windows Shortcuts** - Essential keyboard shortcuts
3. **MS Word** - Word processing skills
4. **Excel** - Spreadsheet mastery
5. **PowerPoint** - Presentation creation

### Admin Features (✏️ Content Management)
- **Add Lessons**: Create new lessons with rich content
- **Edit Lessons**: Modify existing content anytime
- **Delete Lessons**: Remove outdated or unnecessary lessons
- **Rich Media Support**:
  - Text content with multi-paragraph support
  - Image URLs - Display images from any hosting service
  - Video URLs - Embed YouTube videos for tutorials
  - Quiz creation with multiple-choice questions

### User Features

#### Progress Tracking ✅
- Mark lessons as complete
- Visual progress bars on each category
- Overall progress tracker at the top
- Checkmarks show completed lessons
- Track quiz performance

#### Quiz System 📝
- Optional quizzes for each lesson
- Multiple-choice questions (4 options)
- Instant feedback on answers
- Pass/fail scoring (70% threshold)
- Badge awards for passed quizzes
- Unlimited retake attempts
- Progress saved automatically

#### Data Management 💾
- **Export**: Download all lessons and progress as JSON
- **Import**: Restore from previously saved files
- Perfect for backups or sharing content
- All data persists in browser storage

## 🚀 How to Deploy on Google Colab

### Method 1: Direct HTML Deployment

```python
# 1. Upload the computer_training_app.html file to Colab

# 2. Run this code to display the app:
from IPython.display import HTML, display

# Read the HTML file
with open('computer_training_app.html', 'r', encoding='utf-8') as f:
    html_content = f.read()

# Display the app
display(HTML(html_content))
```

### Method 2: Using Google Colab's HTTP Server

```python
# 1. Upload the HTML file to Colab

# 2. Create a simple server:
from IPython.display import IFrame
import os

# Save the file in the current directory
# Then display it
display(IFrame(src='computer_training_app.html', width=1200, height=800))
```

### Method 3: External Hosting (Recommended for Production)

```python
# Upload to Google Drive or any web hosting service
# Then embed in Colab:
from IPython.display import IFrame

# Replace with your hosted URL
url = "https://your-domain.com/computer_training_app.html"
display(IFrame(src=url, width=1200, height=800))
```

## 📖 User Guide

### Getting Started

1. **First Time Setup**:
   - Open the app
   - Click "Sign Up" 
   - Create an admin account (select "Admin" role)
   - Login with your credentials

2. **Default Admin Account** (pre-configured):
   - Username: `admin`
   - Password: `admin123`
   - **Important**: Change these credentials after first login!

### For Administrators

#### Adding a Lesson

1. Click the green "➕ Add New Lesson" button
2. Fill in the lesson details:
   - **Title**: Give your lesson a clear name
   - **Content**: Write the lesson text (supports multiple paragraphs)
   - **Image URL** (optional): 
     - Upload image to Google Drive, Imgur, or Dropbox
     - Get shareable/direct link
     - Paste in the Image URL field
   - **Video URL** (optional):
     - Go to YouTube video
     - Click "Share" → "Embed"
     - Copy URL (format: `https://www.youtube.com/embed/VIDEO_ID`)
     - Paste in the Video URL field

3. **Adding a Quiz** (optional):
   - Check "Add Quiz"
   - Click "➕ Add Question"
   - Enter question text
   - Fill in 4 answer options
   - Mark the correct answer with radio button
   - Add more questions as needed

4. Click "Add Lesson"

#### Editing a Lesson

1. Click the ✏️ edit icon next to any lesson
2. Modify the content
3. Click "Save Changes"

#### Deleting a Lesson

1. Click the 🗑️ delete icon next to any lesson
2. Confirm deletion

### For Users

#### Taking Lessons

1. Select a category from the sidebar
2. Click on any lesson to view content
3. Read through the content, view images/videos
4. Use "Previous" and "Next" buttons to navigate
5. Click "✓ Mark as Complete" when finished

#### Taking Quizzes

1. Scroll down to the quiz section (if available)
2. Select your answers for each question
3. Click "Submit Quiz"
4. View your results:
   - Green = Correct answer
   - Red = Incorrect answer
5. Pass threshold: 70% or higher
6. Click "🔄 Retake Quiz" to try again

#### Tracking Progress

- **Overall Progress**: View at the top of the screen
- **Category Progress**: Shown on each category tab
- **Lesson Status**: Checkmarks indicate completion
- **Quiz Badges**: 🏆 appears when you pass a quiz

### Data Management

#### Exporting Your Data

1. Click "💾 Export" button in the header
2. A JSON file will download
3. Keep this file safe as backup

#### Importing Data

1. Click "📤 Import" button
2. Select your previously exported JSON file
3. All lessons and progress will be restored

## 🎨 Features Highlights

### Beautiful UI
- Modern gradient design
- Smooth animations
- Responsive layout
- Color-coded progress indicators

### Smart Progress Tracking
- Per-user progress tracking
- Category-level completion rates
- Overall progress percentage
- Quiz performance history

### Flexible Content
- Support for text, images, and videos
- Markdown-style formatting
- No file size limits (external hosting)
- Works with any image/video hosting service

## 🔒 Security Notes

1. **Change Default Password**: Always change the default admin credentials
2. **Data Storage**: All data stored in browser localStorage
3. **Export Regularly**: Keep backups of your content
4. **Shared Computers**: Always logout after use

## 📱 Browser Compatibility

Works on:
- Chrome/Edge (recommended)
- Firefox
- Safari
- Opera
- Any modern browser with JavaScript enabled

## 💡 Tips for Best Experience

### For Admins:
1. Create a logical lesson sequence (beginner to advanced)
2. Use clear, descriptive titles
3. Break complex topics into multiple lessons
4. Add quizzes to reinforce learning
5. Use images and videos to enhance understanding
6. Export data regularly as backup

### For Users:
1. Complete lessons in order
2. Don't skip quizzes - they help retention
3. Review failed quizzes to learn from mistakes
4. Use Previous/Next buttons for easy navigation
5. Track your progress to stay motivated

## 🎯 Content Creation Tips

### Writing Good Lessons

```
Title: Introduction to Computer Hardware

Content:
A computer is made up of several key components.

The main parts include:
- CPU (Central Processing Unit): The brain of the computer
- RAM (Random Access Memory): Temporary storage for active programs
- Hard Drive: Long-term storage for files and programs
- Motherboard: Connects all components together

Each component plays a vital role in the computer's operation.

Image URL: https://example.com/images/computer-parts.jpg
Video URL: https://www.youtube.com/embed/ExxFxD4OSZ0
```

### Creating Effective Quizzes

- Ask clear, unambiguous questions
- Provide 4 realistic options
- Make sure one answer is clearly correct
- Cover key concepts from the lesson
- 3-5 questions per lesson is ideal

### Image Hosting Options

1. **Google Drive**:
   - Upload image
   - Right-click → Get link
   - Change sharing to "Anyone with the link"
   - Use direct link format

2. **Imgur**:
   - Upload image
   - Copy direct link
   - Paste in Image URL field

3. **Dropbox**:
   - Upload image
   - Create shareable link
   - Modify link for direct access

### Video Embedding

**YouTube Steps**:
1. Find your video on YouTube
2. Click "Share" button below video
3. Click "Embed"
4. Copy the src URL from the iframe code
5. Format: `https://www.youtube.com/embed/VIDEO_ID`

Example:
```
Original: https://www.youtube.com/watch?v=dQw4w9WgXcQ
Embed: https://www.youtube.com/embed/dQw4w9WgXcQ
```

## 🐛 Troubleshooting

### Images Not Showing
- Check if URL is accessible
- Ensure it's a direct image link
- Try a different hosting service
- Check image format (JPG, PNG, GIF, WebP)

### Videos Not Playing
- Verify it's a YouTube embed URL
- Check if video is public
- Ensure correct format: `/embed/VIDEO_ID`
- Test the URL in a new browser tab

### Data Not Saving
- Check browser localStorage is enabled
- Clear browser cache and try again
- Export data as backup
- Try a different browser

### Quiz Not Submitting
- Ensure all questions are answered
- Check JavaScript is enabled
- Refresh page and try again

## 📊 Data Structure (for developers)

The exported JSON contains:
```json
{
  "categories": {
    "category-id": {
      "name": "Category Name",
      "lessons": [
        {
          "id": 123456789,
          "title": "Lesson Title",
          "content": "Lesson content...",
          "imageUrl": "https://...",
          "videoUrl": "https://...",
          "quiz": {
            "questions": [
              {
                "question": "Question text",
                "options": ["A", "B", "C", "D"],
                "correctAnswer": 0
              }
            ]
          }
        }
      ]
    }
  },
  "progress": {
    "username-category-lessonid": {
      "completed": true,
      "completedAt": "2025-01-09T...",
      "quizPassed": true,
      "quizScore": 100,
      "quizAttempts": 2
    }
  },
  "users": [
    {
      "username": "admin",
      "password": "admin123",
      "role": "admin"
    }
  ]
}
```

## 🎓 Sample Content Ideas

### Computer Basics
- Parts of a Computer
- Operating System Basics
- File Management
- Internet Safety
- Email Etiquette

### Windows Shortcuts
- Essential Keyboard Shortcuts
- Window Management
- File Explorer Tips
- Copy, Cut, Paste Mastery
- Screen Capture Techniques

### MS Word
- Document Formatting
- Styles and Templates
- Tables and Lists
- Headers and Footers
- Track Changes

### Excel
- Basic Formulas
- Cell Formatting
- Charts and Graphs
- PivotTables
- Data Validation

### PowerPoint
- Slide Design Principles
- Animations and Transitions
- Master Slides
- Presenter View
- Exporting Presentations

## 🤝 Support

For issues or questions:
1. Check the Troubleshooting section
2. Review the User Guide
3. Export your data before making major changes
4. Test features in a new browser if problems persist

## 📜 License

This project is open-source and free to use for educational purposes.

## 🎉 Happy Learning!

Make the most of this powerful training platform. Whether you're an admin creating content or a user learning new skills, this app provides everything you need for a comprehensive computer training experience!

---

**Version**: 1.0.0  
**Last Updated**: January 2026  
**Compatibility**: All modern browsers, Google Colab ready
