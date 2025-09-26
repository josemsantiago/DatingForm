# DatingForm
### Interactive Web Dating Profile Form

A comprehensive HTML form for collecting dating profile information with live image preview and cloud database integration.

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

1. **Open the form**: Open `datingform.html` in a web browser
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
├── datingform.html        # Main form file
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

## Requirements

- Modern web browser with JavaScript enabled
- Internet connection for API submission
- No server setup required (client-side only)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

*Note: This form connects to a live API endpoint. Submitted data will be stored in the cloud database.*
