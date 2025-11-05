#  Dataset Image Cleaning Script

This repository provides a Python script for **detecting and removing corrupted images** from dataset (or any dataset organized into folders of images). This helps ensure your machine learning data is clean before model training.

---

## ✅ Features

* Scans all images in the dataset
* Detects broken/corrupted/unreadable images
* Automatically **deletes** corrupted files
* Prints a summary of removed files

---

## 📂 Dataset Structure

Your dataset should be organized like this:

```
plantvillage dataset/
    color/
        Class_1/
        Class_2/
        Class_3/
        ...
```

If your dataset folder name is different, update the path in the script.

---

## 🛠️ Requirements

Make sure you have Python installed along with the Pillow library:

```bash
pip install Pillow

## 📝 What This Script Does

| Step | Action                                               |
| ---- | ---------------------------------------------------- |
| 1    | Walks through all folders in the dataset             |
| 2    | Tries to open each image using Pillow                |
| 3    | If the image is unreadable, it's marked as corrupted |
| 4    | Corrupted images are **automatically deleted**       |
| 5    | A summary is printed at the end                      |

---

## 🧪 Example Output

```
Corrupted file removed: plantvillage dataset/color/class1/img_0452.jpg
Corrupted file removed: plantvillage dataset/color/class4/img_1200.png

Cleaning complete. 12 corrupted images were removed.
```

---

## ⚠️ Notes

* This script **permanently deletes** corrupted files.
* If you want to *only list* corrupted images instead of deleting them, remove the line:

  ```python
  os.remove(path)
  ```

---

## 📄 License

This project is free to use for research, academic, and personal projects.

---

## 🤝 Contributing

Pull requests and improvements are welcome!
