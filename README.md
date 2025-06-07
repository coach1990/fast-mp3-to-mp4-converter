# Fast MP3 to MP4 Converter

![Python Version](https://img.shields.io/badge/python-3.7+-blue.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

A blazing-fast Python application with a graphical user interface (GUI) to efficiently convert multiple MP3 files to MP4 format (with a black screen) using multi-processing.

This tool is designed for content creators, musicians, or anyone who needs to quickly convert audio files into a video format suitable for platforms like YouTube, Instagram, or other video-sharing sites.

---

### Screenshot

*(It's highly recommended to add a screenshot of the application here. Just replace the placeholder below.)*

![Screenshot 2025-06-07 230108](https://github.com/user-attachments/assets/3e23076a-0be6-4c6d-9658-e6450e3b918c)


---

## Key Features

- **High-Speed Conversion:** Uses an 'ultrafast' FFMpeg preset to prioritize speed over file size, making it ideal for quick batch processing.
- **Concurrent Processing:** Takes full advantage of modern multi-core CPUs by processing multiple files in parallel.
- **User-Friendly GUI:** A simple and intuitive interface built with Tkinter for easy file selection and progress tracking.
- **Batch Processing:** Select and convert dozens or even hundreds of files in one go.
- **Real-Time Feedback:** Watch the status of each file update in real-time from "Working" to "Done", "Skipped", or "Error".
- **Intelligent Skipping:** Automatically skips files that have already been converted to avoid redundant work.
- **Cross-Platform:** Built with standard Python libraries to work on Windows, macOS, and Linux.

---

## Installation & Usage

Getting the application up and running is simple.

### Prerequisites

- **Python 3.7+** must be installed on your system.

### Steps

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/fast-mp3-to-mp4-converter.git](https://github.com/your-username/fast-mp3-to-mp4-converter.git)
    cd fast-mp3-to-mp4-converter
    ```
    *(Replace `your-username` with your actual GitHub username)*

2.  **Install the necessary dependencies:**
    This project relies on the `moviepy` library. To avoid common installation issues, it's best to install it using the following command:

    ```bash
    python -m pip install moviepy==1.0.3
    ```
    *(**Note:** On the first run, `moviepy` may need to download the FFMpeg binary, which can cause a one-time delay. Subsequent runs will be instant.)*

3.  **Run the application:**
    ```bash
    python converter.py
    ```

4.  **Using the App:**
    - Click **"1. Select MP3 Files"** to choose the files you want to convert.
    - Click **"2. Start Conversion"** to begin the process.
    - The converted `.mp4` files will be saved in the same directory as the original MP3s.

---

## How It Works

- **Frontend:** The graphical interface is built using Python's standard **Tkinter** library.
- **Backend/Core Logic:**
    - The core conversion is handled by the powerful **`moviepy`** library, which uses **FFMpeg** under the hood.
    - To prevent the GUI from freezing and to maximize performance, the application uses Python's **`concurrent.futures.ProcessPoolExecutor`**. This creates separate processes for each file conversion, allowing them to run in parallel on different CPU cores.

---

## Contributing

Contributions are welcome! If you have ideas for new features, bug fixes, or improvements, feel free to fork the repository and submit a pull request.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

---

## License

This project is distributed under the MIT License. See the `LICENSE` file for more information.
