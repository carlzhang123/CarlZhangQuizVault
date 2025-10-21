# CarlZhangQuizVault

A lightweight, mobile-friendly quiz application designed for seamless question practice, featuring dynamic question loading, type filtering (single/multiple choice, true/false), direct question navigation, and real-time progress tracking. Built with HTML, Tailwind CSS, and vanilla JavaScript, it supports offline use and responsive design—optimized for both mobile and desktop experiences. Ideal for organizing and practicing various types of quiz content with intuitive UI/UX.

## Features

### 1. Core Functionality



* **Dynamic Question Loading**: Load questions one by one, no full-page refresh for smooth interaction.

* **Flexible Question Navigation**:


  * Switch between "Previous Question" and "Next Question" with one tap/click.

  * Direct jump to a specific question via the jump modal (supports input validation).

* **Question Type Filtering**: Filter questions by type (Single Choice / Multiple Choice / True/False) to focus on specific practice needs.

* **Progress Tracking**: Real-time progress bar shows current practice progress, with clear question count display (e.g., "Question 5 / 453").

* **Answer Display**: Toggle "Show Answer" to view correct answers, with visual highlighting (green for correct, red for incorrect user selections).

### 2. Responsive Design



* **Mobile Optimization**: Buttons auto-switch to icon-only mode on small screens (≤640px) to save space; touch-friendly tap areas (≥45px) for easy operation.

* **Desktop Adaptation**: Full text + icon buttons for clear usability; expanded progress bar and layout for better readability.

* **Cross-Device Compatibility**: Works seamlessly on smartphones, tablets, laptops, and desktops (supports Chrome, Safari, Firefox, Edge).

### 3. Offline Support



* No backend dependencies—all question data is stored locally in JavaScript.

* Works without internet connection after initial page load.

## Tech Stack



* **Frontend**: HTML5 (semantic structure), Tailwind CSS v3 (responsive styling), Vanilla JavaScript (interactivity logic).

* **UI/UX**: Font Awesome icons (intuitive visual cues), smooth transitions (hover/click effects), clear visual hierarchy.

## Quick Start

### 1. Clone the Repository



```
git clone https://github.com/your-username/CarlZhangQuizVault.git

cd CarlZhangQuizVault
```

### 2. Run the Application



* No build steps required—directly open `index.html` in your browser.

* For best experience: Use Chrome (mobile/desktop) or Safari (iOS devices).

### 3. Customize Question Data



1. Open `index.html` and locate the `questions` array (in the `<script>` tag marked "Question Data").

2. Add/modify questions following the existing format:



```
{
  "id": 1,
  "content": "Your question content here?",
  "type": "Single", // 可选: "单选题" / "多选题" / "判断题"
  "optionA": "Option A",
  "optionB": "Option B",
  "optionC": "Option C",
  "optionD": "Option D",
  "answer": "A" // 多选题答案用大写字母拼接，如 "AB"
}
```



1. Save the file and refresh the browser to see changes.

## Usage Guide



| Function               | Operation                                                    |
| ---------------------- | ------------------------------------------------------------ |
| Filter Question Types  | Click "Filter" button → Select desired type (e.g., "Multiple Choice"). |
| Jump to Question       | Click "Jump" button → Enter question number → Click "Confirm". |
| Show Correct Answer    | Click "Show Answer" button (correct answers highlighted in green). |
| Reset Current Question | Click "Reset" button (clears user selection and hides answer). |
| Navigate Questions     | Use "Previous"/"Next" buttons, or swipe left/right (mobile) / arrow keys (desktop). |

## License

MIT License - Feel free to use, modify, and distribute this project for personal or commercial use. See the [LICENSE](LICENSE) file for details.

## Contributing



1. Fork the repository.

2. Create a feature branch (`git checkout -b feature/your-feature`).

3. Commit your changes (`git commit -m 'Add new feature'`).

4. Push to the branch (`git push origin feature/your-feature`).

5. Open a Pull Request.

## Screenshots

### Mobile View

![mobile_view](https://raw.githubusercontent.com/carlzhang123/CarlZhangQuizVault/refs/heads/main/img/mobile_view.png)

### Desktop View

![desktop_view](https://raw.githubusercontent.com/carlzhang123/CarlZhangQuizVault/refs/heads/main/img/desktop_view.png)

### Question Filtering

![question_filter](https://raw.githubusercontent.com/carlzhang123/CarlZhangQuizVault/refs/heads/main/img/question_filter.png)

### Answer Display

![answer_display](https://raw.githubusercontent.com/carlzhang123/CarlZhangQuizVault/refs/heads/main/img/answer_display.png)

## Known Issues



* **Question Data Size**: For very large question banks (>1000 questions), initial page load time may increase. Consider implementing pagination for extremely large datasets.