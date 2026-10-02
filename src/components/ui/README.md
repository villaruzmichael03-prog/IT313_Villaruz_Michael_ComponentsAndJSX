# Student Roster Card Renderer

## The Problem

The IT313 registrar gave a list of four enrolled students. This Expo (React Native) app renders each student as a reusable card showing their name, course, and units. The "Full Load" label appears only when `isFullLoad` is true. The header shows the total number of students.

## Component Structure

- **StudentCard**: A functional component that receives name, course, units, and isFullLoad as props. It displays the student's information and uses `{isFullLoad && ...}` to conditionally show the Full Load label. It also has a present state that can be changed by tapping the card.

- **StudentRoster**: The parent component. It contains the students array, displays the student count, has a Reverse Order button, and uses `.map()` with `key={student.id}` to render each StudentCard.

- **app/index.tsx**: The entry file that displays StudentRoster.

## Key Experiment

Using the array index as the key made the checkmark stay in the same position after reversing the list. With `key={student.id}`, the checkmark follows the correct student.

## How to Run

1. `npm install`
2. `npx expo start`
3. Scan the QR code with Expo Go.
