
# Vulnerability Checker

![Vulnerability Checker](https://img.shields.io/badge/security-checker-blue?style=flat-square)

## Overview

The **Vulnerability Checker** is a lightweight web-based tool designed to scan JavaScript, HTML, and CSS files for common vulnerabilities such as:

- Cross-Site Scripting (XSS)
- Cross-Site Request Forgery (CSRF)
- Insecure code patterns (`eval`, `document.write`, etc.)
- Default session cookie names
- Lack of brute-force protection

This project aims to help developers identify potential security flaws in their code to improve the overall security of their web applications.

---

## Features

- **Pattern Matching**: Detects insecure patterns like `eval`, `child_process.exec`, and more.
- **XSS Detection**: Identifies inline script tags, event handlers like `onerror`, and `javascript:` URLs.
- **CSRF Vulnerability Checks**: Highlights forms without CSRF protection tokens.
- **Brute-Force Prevention**: Warns about insufficient login attempt tracking.
- **Session Cookie Validation**: Flags default cookie names that might be vulnerable.

---

## Usage

### 1. Clone or Download the Project
Clone the repository or download the files directly to your local machine.

```bash
git clone https://github.com/your-username/vulnerability-checker.git
```

### 2. Open the HTML File
Simply open the `index.html` file in your preferred web browser. The application requires no additional setup or backend.

### 3. Upload a File
- Click the **"Choose File"** button.
- Select a `.js`, `.html`, or `.css` file from your local system.
- The tool will automatically scan the file and display the results.

---

## File Analysis Example

### Input:
A JavaScript file containing the following code:
```javascript
eval("alert('test')");
document.write("<h1>Test</h1>");
```

### Output:
```plaintext
Insecure pattern found: /eval\(/
Insecure pattern found: /document\.write\(/
```

---

## How It Works

1. **File Upload**: The user uploads a file to be analyzed.
2. **Content Parsing**: The content is read and checked against a list of predefined regular expressions.
3. **Vulnerability Report**: Displays detected issues in a user-friendly format.

### Vulnerabilities Detected
| Vulnerability      | Description                                 |
|--------------------|---------------------------------------------|
| **Insecure Patterns** | Usage of dangerous methods like `eval`.    |
| **XSS**            | Potential cross-site scripting attacks.    |
| **CSRF**           | Forms without adequate CSRF tokens.        |
| **Brute Force**    | Insufficient login attempt protections.    |
| **Cookies**        | Use of default session cookie names.       |

---

## Technologies Used

- **HTML**: For the structure and layout.
- **CSS**: For responsive and user-friendly styling.
- **JavaScript**: For file reading, analysis, and DOM manipulation.

---

## Future Enhancements

- Add support for additional file types.
- Expand detection patterns for advanced security issues.
- Provide recommendations for resolving vulnerabilities.
- Integrate with backend APIs for more detailed scanning.

---

## Contribution

Contributions are welcome! Please feel free to submit a pull request or open an issue if you have suggestions for improvements.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

### Author

Developed with ❤️ by [Your Name](https://github.com/your-username). 
