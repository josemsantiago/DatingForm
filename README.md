# DatingForm
### Interactive Web Dating Profile Form

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/license-MIT-blue)
![Status](https://img.shields.io/badge/status-active-success)

A comprehensive HTML form for collecting dating profile information with live image preview and cloud database integration.

## Screenshots

> **Note:** Form screenshots will be added soon. Open `index.html` in your browser to see the interactive form in action.

## Overview

This web-based dating profile form demonstrates advanced HTML form elements, CSS styling, JavaScript integration, and API connectivity. Users can upload photos, fill out detailed profile information, and submit data to a cloud database.

## Features

### 📷 Image Management
- **File Upload**: Profile picture upload with live preview
- **Image Preview**: Real-time display of selected image before submission
- **Supported Formats**: Standard image formats (JPG, PNG, GIF, etc.)

### 👤 Personal Information
- **Basic Details**: Name, age, date of birth, gender identity
- **Physical Attributes**: Favorite color picker
- **Demographics**: Country selection from dropdown menu
- **Financial**: Salary range slider from "Poor" to "Rich"

### 📞 Contact Information
- **Email**: Required email with built-in validation
- **Phone**: Optional telephone number input
- **Address**: Multi-line address field
- **Preferences**: Contact method selection (email/phone checkboxes)

### 🎨 User Experience
- **Responsive Design**: Works on desktop and mobile devices
- **Visual Styling**: Professional purple/lavender color scheme
- **Interactive Elements**: Hover effects and dynamic form elements
- **Input Validation**: Built-in HTML5 form validation

## Technical Implementation

### Frontend Technologies
- **HTML5**: Semantic form structure with modern input types
- **CSS3**: Custom styling with hover effects and color schemes
- **JavaScript**: External script for image preview functionality

### Form Elements Used
```html
<input type="file">        <!-- Image upload -->
<input type="email">       <!-- Email validation -->
<input type="tel">         <!-- Phone number -->
<input type="date">        <!-- Date picker -->
<input type="color">       <!-- Color picker -->
<input type="range">       <!-- Salary slider -->
<select>                   <!-- Country dropdown -->
<textarea>                 <!-- Address field -->
<input type="checkbox">    <!-- Contact preferences -->
```

### Backend Integration
- **API Endpoint**: `https://us-central1-nucamp-production.cloudfunctions.net/post/formdata`
- **Method**: POST with multipart/form-data encoding
- **Cloud Storage**: Submitted data stored in cloud database
- **Image Processing**: Profile pictures processed and stored

## How to Use

1. **Open the form**: Open `index.html` in a web browser
2. **Upload Photo**: Click "Choose File" to select a profile picture
3. **Fill Details**: Complete all required fields (marked with *)
4. **Preview**: Review your information and image preview
5. **Submit**: Click submit to send data to the database

## Form Fields

### Required Fields (*)
- **Name**: Full name
- **Sex**: Gender selection (Female/Male)
- **Email**: Valid email address
- **Contact Method**: At least one contact preference

### Optional Fields
- **Gender**: Gender identity (separate from sex)
- **Age**: Numeric age input
- **Date of Birth**: Calendar date picker
- **Favorite Color**: Color picker
- **Country**: Dropdown selection (Brazil, France, Japan, Libya, USA)
- **Salary**: Range slider (0-100 scale)
- **Phone**: Telephone number
- **Address**: Full address

## File Structure

```
DatingForm/
├── index.html            # Main form file
└── README.md             # This documentation
```

## External Dependencies

- **Image Preview Script**: `https://url.nucamp.co/datingjs`
- **Cloud Database**: NuCamp production cloud functions
- **Font Stack**: Verdana, Arial, Geneva, Tahoma, sans-serif

## Browser Compatibility

- **Modern Browsers**: Chrome, Firefox, Safari, Edge
- **HTML5 Support**: Required for advanced input types
- **JavaScript**: Must be enabled for image preview
- **File Upload**: Browser must support file input type

## Privacy & Security

- **Data Transmission**: HTTPS encrypted submission
- **Cloud Storage**: Secure cloud database storage
- **No Local Storage**: Data not stored locally in browser
- **Validation**: Server-side validation for security

## Customization

### Styling
- Modify CSS variables in the `<style>` section
- Change color scheme by updating color values
- Adjust form layout with CSS grid/flexbox

### Fields
- Add new form fields by following existing patterns
- Modify dropdown options in `<select>` elements
- Adjust validation rules with HTML5 attributes

## Sample Data Flow

```
User fills form → JavaScript validates → Image preview updates →
Form submits → Data sent to cloud API → Stored in database →
Confirmation returned to user
```

## Use Cases

- **Dating Applications**: Profile creation for dating platforms
- **Social Networks**: User registration forms
- **Survey Systems**: Comprehensive data collection
- **Educational Projects**: Form development learning

## Prerequisites

- **Web Browser**: Modern browser with JavaScript enabled
  - Chrome 90+ (recommended)
  - Firefox 88+
  - Safari 14+
  - Edge 90+
- **Internet Connection**: Required for API submission and external scripts
- **No Server Setup**: Runs entirely client-side

## Troubleshooting

### Common Issues

**Issue:** Image preview not working

**Solution:** Ensure JavaScript is enabled in your browser and you have an active internet connection (the preview script loads from `https://url.nucamp.co/datingjs`).

---

**Issue:** Form submission fails

**Solution:**
1. Check your internet connection
2. Verify all required fields are filled (marked with *)
3. Check browser console (F12) for error messages
4. Ensure email format is valid

---

**Issue:** CORS errors in browser console

**Solution:** This is expected when opening HTML files directly (file:// protocol). For full functionality:
- Use a local server (Python: `python -m http.server 8000`)
- Or deploy to a web host

---

**Issue:** Uploaded image too large

**Solution:** Resize your image before uploading. Most browsers limit file upload sizes. Recommended: under 5MB.

---

**Issue:** Country dropdown empty or not working

**Solution:** Check that the HTML file hasn't been corrupted. The dropdown should contain: Brazil, France, Japan, Libya, USA.

For additional help, please open an issue in the repository issue tracker.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add YourFeature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

### Enhancement Ideas
- Add more form fields (hobbies, interests, etc.)
- Implement client-side validation before submission
- Add multiple image upload support
- Create success/error message display
- Add form progress indicator
- Implement data preview before submission

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact & Support

- **Author**: José Santiago Echevarria
- **Issues**: Please report bugs via the repository issue tracker
- **Educational Context**: Demonstrates HTML5 form elements, CSS styling, and API integration
- **API Endpoint**: Connects to NuCamp cloud functions for data storage

---

**Important:** This form connects to a live API endpoint. Submitted data will be stored in the cloud database. Do not submit sensitive personal information.
