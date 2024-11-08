# IELTS Speaking Assistant 🎤

## 📖 Giới thiệu
**IELTS Speaking Assistant** là một ứng dụng Python hỗ trợ người dùng luyện tập kỹ năng nói IELTS. Ứng dụng cung cấp giao diện tương tác, đọc câu hỏi, nhận diện giọng nói và đánh giá câu trả lời dựa trên AI.

### Các tính năng:
- **Giao diện tương tác**: Được xây dựng bằng `tkinter` giúp dễ sử dụng.
- **Đọc câu hỏi bằng giọng nói**: Sử dụng Google Text-to-Speech (`gTTS`).
- **Nhận diện giọng nói**: Chuyển giọng nói của người dùng thành văn bản.
- **Đếm ngược thời gian thực**: Đếm ngược 45 giây cho mỗi câu trả lời.
- **Đánh giá tự động**: Sử dụng AI Generative của Google để đánh giá và đưa ra điểm số IELTS.

## 🛠️ Cài đặt

### Yêu cầu:
1. **Python 3.8+** đã cài đặt trên máy.
2. **API Key của Google Generative AI**: Lấy API key từ [Google Generative AI Studio](https://aistudio.google.com/app/apikey).

### Cài đặt các thư viện Python
Chạy lệnh sau để cài đặt các thư viện cần thiết:

```bash
pip install gtts SpeechRecognition pyaudio google-generativeai pillow
Lưu ý: Nếu gặp lỗi khi cài đặt pyaudio, hãy thử:

- Trên macOS: brew install portaudio
- Trên Ubuntu/Linux: sudo apt install portaudio19-dev

### 3. **Configuration**
```markdown
## ⚙️ Cấu hình

### 1. Thay thế API Key
Mở file Python chính (`IELTS_Speaking_Assistant.py`) và thay thế API key ở **dòng 18**:

```python
# Thay "Your GenAI key" bằng API key của bạn
genai.configure(api_key="Your GenAI key")
Lấy API key từ Google Generative AI Studio.

2. Thêm file câu hỏi
Đảm bảo rằng file câu hỏi (IELTS_Speaking_Formatted_Final.txt) có định dạng như sau:

vbnet
Copy code
Topic: Sports
Question: Have you ever supported a sports team? Why/Why not?

Topic: Travel
Question: What kind of places do you like to visit?
yaml
Copy code

---

### 4. **Usage Instructions**
## 🚀 Hướng dẫn sử dụng

Chạy ứng dụng bằng Python:

```bash
python IELTS_Speaking_Assistant.py
Quy trình sử dụng:
Nhấn Start để bắt đầu phiên luyện tập.
Ứng dụng sẽ đọc chủ đề và câu hỏi cho bạn.
Bắt đầu đếm ngược 45 giây để bạn trả lời.
Ứng dụng sẽ ghi âm câu trả lời của bạn, chuyển thành văn bản và đánh giá bằng AI.
Hiển thị kết quả đánh giá và điểm số trên màn hình.
Nhấn Next Question để chuyển sang câu hỏi tiếp theo.
yaml
Copy code

---

### 5. **Project Structure**
```
📦 IELTS-Speaking-Assistant
├── IELTS-logo.png # Logo của ứng dụng
├── IELTS_Speaking_Assistant.py # File Python chính
├── IELTS_Speaking_Formatted_Final.txt # File câu hỏi
├── temp.mp3 # File âm thanh tạm thời
├── README.md # Tài liệu hướng dẫn
```