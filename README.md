Binary to Video Converter

This project encodes any file as a lossless video where each bit is visually represented as a black or white pixel. It also decodes the video back into the original file without data loss.

📌 Features

✅ Lossless Encoding using FFV1 codec (preserves binary accuracy)
✅ Handles Compression Artifacts with brightness thresholding
✅ Supports Any File Format by encoding as binary
✅ Automatic Filename Extraction for seamless decoding
✅ Compatible with OpenCV

📥 Installation

🔹 Dependencies

Make sure you have OpenCV installed:

sudo apt-get install libopencv-dev  # Ubuntu
brew install opencv                # macOS

Or install via C++ package manager if needed.

🔹 Compile the Program

g++ -o binary_to_video binary_to_video.cpp `pkg-config --cflags --libs opencv4`

🚀 Usage

1️⃣ Encode File to Video

Convert a file into a binary video:

./binary_to_video -e myfile.txt

📌 Output: YYYYMMDD_HHMMSS_txt.avi

2️⃣ Decode Video to Original File

Retrieve the original file from a video:

./binary_to_video -d YYYYMMDD_HHMMSS_txt.avi

📌 Output: output.txt

⚙️ How It Works

Reads the file and converts it into a binary string.

Encodes binary as black (1) and white (0) pixels.

Saves frames in a lossless AVI video using the FFV1 codec.

Extracts frames, reconstructs binary, and writes the original file.

🛠️ Supported Formats

This works with any file including:

✅ Text files (.txt, .csv, etc.)

✅ Images (.png, .jpg, .bmp, etc.)

✅ Executables (.exe, .bin)

✅ Archives (.zip, .rar, .tar.gz)

🔥 Future Improvements

Add custom resolutions for different file sizes.

Implement real-time playback of binary decoding.

Improve speed for large files.

📜 License

This project is open-source under the MIT License. Feel free to contribute! 🚀

