# CCTV Crowd Detection System

This is a modern web interface for AI-powered crowd detection using video files or live CCTV streams. Built with **Next.js**, **Tailwind CSS**, and **ShadCN UI components**, the app offers a clean and responsive UI for configuring detection settings and monitoring video input.

## 📁 Project Structure

```
.
├── app/
│   ├── layout.tsx       # Root layout with metadata and global styles
│   └── page.tsx         # Main UI for the crowd detection system
├── styles/
│   └── globals.css      # Tailwind CSS base styles and theme variables
```

> Note: The project assumes usage of ShadCN components (e.g., `@/components/ui/*`, `CrowdDetector`) which should be present in the corresponding directories.

---

## 🧠 Features

- **Video Input Options**:
  - Connect to a CCTV stream via URL (RTSP/HTTP/HLS)
  - Upload a local video file
- **Real-Time Detection** (via `CrowdDetector` component):
  - Adjustable crowd threshold
  - Selectable detection quality
  - Live status feedback
- **System Settings**:
  - Enable/disable alerts
  - Enable/disable recording
  - Compatibility mode for low-resource devices
- **Responsive Design**:
  - Styled using Tailwind CSS and gradients
  - Dark mode-friendly theme

---

## 🚀 Getting Started

### Prerequisites

- Node.js 16+
- npm or yarn
- The following components need to exist:
  - `@/components/ui/*` (from ShadCN UI)
  - `@/components/crowd-detector` (custom or external AI integration)

### Installation

```bash
git clone <your-repo-url>
cd <project-folder>
npm install
```

### Development

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 🧱 Technologies Used

- **Next.js** (App Router)
- **React** with hooks
- **Tailwind CSS** (with custom themes in `globals.css`)
- **ShadCN UI** for component structure
- **Lucide React** for icons
- **Toast system** for alerts

---

## 📌 Important Notes

- Make sure the `CrowdDetector` component exists and supports props like:
  ```tsx
  mode: "video" | "cctv"
  videoUrl?: string
  cctvUrl?: string
  crowdThreshold: number
  detectionQuality: number
  enableAlerts: boolean
  enableRecording: boolean
  ```
- This README assumes you're extending the app to include AI backend or WebRTC/CV integration.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).