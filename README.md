# 🖼️ Image Labeler using Amazon Rekognition

This project uses **AWS Rekognition** to detect and label objects in images stored in an S3 bucket. It fetches images from AWS S3, sends them to Rekognition, and prints detected labels with confidence scores.

<img width="1071" height="741" alt="520591871-a099a93b-732f-4a76-9da2-556fa5caf62b" src="https://github.com/user-attachments/assets/a210300e-9aea-4f78-aeb1-1037af597569" />



---

## 🚀 Features

- Detects objects in images using AWS Rekognition
- Fetches images directly from S3 bucket
- Displays label names with confidence scores
- Processes multiple images in a loop
- Saves processed output images locally

---

## 🧰 AWS Services Used

- Amazon S3 → Stores images
- Amazon Rekognition → Image analysis & label detection  
:contentReference[oaicite:0]{index=0}

---

## 📁 Project Structure


Image-Labeler-using-Amazon-Rekognition/
│
├── image_labeler.py
├── README.md
├── .gitignore
└── output_images/ (generated after running)


---

## ⚙️ Requirements

Install dependencies:

```bash
pip install boto3 pillow
🔐 AWS Setup
Create an IAM user
Attach policies:
AmazonRekognitionFullAccess
AmazonS3FullAccess
Configure AWS CLI:
aws configure
▶️ How to Run
Upload images to your S3 bucket
Update bucket name in code:
bucket = "your-bucket-name"
Run script:
python image_labeler.py
🧾 Sample Output
Processing: clock.png

Detected Labels:
Clock - 99.55%
Wall - 91.20%
Tower - 88.10%
📸 Output Images

Processed images are saved locally with bounding box overlays:

output_clock_png.png
output_IMG_0465_jpg.png
📌 Notes
Only JPG/PNG images are supported (HEIC not supported)
Ensure AWS credentials are configured properly
Make sure images exist in S3 bucket
📚 Learning Outcome
AWS S3 integration
AWS Rekognition API usage
Python AWS SDK (boto3)
Image processing with PIL
