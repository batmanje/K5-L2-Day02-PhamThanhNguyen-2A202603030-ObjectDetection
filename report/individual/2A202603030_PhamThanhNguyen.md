# Báo cáo cá nhân — Ngày 2 Object Detection

## 1. Thông tin học viên

- Họ tên: Phạm Thành Nguyên
- MSSV: 2A202603030
- Email: phamthanhnguyen5122000@gmail.com
- Lớp: 2a-lec-e402
- Link repo bài làm: https://github.com/batmanje/K5-L2-Day02-PhamThanhNguyen-2A202603030-ObjectDetection.git
- Link Colab đã chạy: https://colab.research.google.com/drive/1qsbAD6sFeLy9zNJQSiQGVR2eYqOJV4Bv?usp=sharing

## 2. Schema và mini guideline

(https://github.com/batmanje/K5-L2-Day02-PhamThanhNguyen-2A202603030-ObjectDetection/blob/main/GUIDELINE_MINI.md)

## 3. Annotation và self-QC

- Số file nhãn train:50/50
- Kết quả checker và lỗi đã xử lý:
- Danh sách ít nhất 10 ảnh đã rà bằng mắt:
- Lỗi bỏ sót/box/class phát hiện khi rà và cách sửa:
- Commit khóa nhãn ban đầu:

## 4. Gold QC và rework

| Chỉ số | Trước sửa | Sau sửa nếu có |
|---|---:|---:|
| TP | 466 | |
| FP | 577 | |
| FN | 187 | |
| Precision | 0.4468 | |
| Recall | 0.7136 | |
| F1 | 0.5495 | |
| mean_iou_of_matches | 0.8384 | |
| passed | pass | |

Dẫn tới `outputs/annotation_evaluation.json` trong repo. Nếu rework, ghi ảnh, lỗi đã kiểm, quyết định sửa/giữ và lý do. Không suy nguyên nhân chỉ từ FP/FN. Không có rework thì ghi rõ.

## 5. Kết quả YOLO

- Runtime, GPU/CPU, phiên bản Ultralytics và Torch: Python-3.13.18, CPU,  Ultralytics Settings v0.0.8, torch-2.14.1
- Các tham số thay đổi so với notebook nếu có và lý do:
- Đường dẫn best checkpoint trong phiên chạy: /content/Day2-Lab/outputs/yolo26_runs/vehicle_annotation/weights/best.pt 

| Chỉ số trên 10 ảnh eval | Giá trị |
|---|---:|
| Precision | 0.4584933050853634 |
| Recall | 0.23341765280930263 |
| mAP50 | 0.276335557972849 |
| mAP50–95 | 0.2053946444941465 |

Đặt cả 2 folder `assets/eval_predictions/` và `assets/yolo26_runs/` (giải nén từ `day2_colab_outputs.zip`) cạnh báo cáo và dẫn link tương đối. Không chỉ ghi số; chỉ ra ít nhất một ảnh và vật thể cụ thể.

Trả lời bốn câu hỏi cuối notebook:

1. Lớp nào recall thấp nhất? Ảnh nào minh họa? Lớp Bus recall thấp nhất, ảnh drive_058
2. Nếu mAP50 cao nhưng mAP50–95 thấp, cần kiểm điều gì trên box? box có thừa nền không, mép có lệch không, có cắt mất phần xe không, Box có quá to/bao 2 xe hoặc trùng lặp không.
3. Lỗi class nào có thể liên quan guideline? Dữ kiện nào hỗ trợ nhận xét? Lỗi nhầm van với bus, drive_058: ground truth 1 bus + 6 van, model dự đoán 6 bus + 2 van.
4. Vì sao không dùng 10 ảnh eval để train? Vai trò validation của chúng trong notebook là gì? Vì 10 ảnh eval là tập validation duy nhất chưa từng thấy — đưa chúng vào train là rò rỉ dữ liệu (data leakage), 

## 6. Khó khăn và cách xử lý

| Bước/thời điểm | Lỗi quan sát | Cách đã thử | Kết quả/còn thiếu |
|---|---|---|---|
| | | | |

## 7. Tự đánh giá theo rubric

(https://github.com/batmanje/K5-L2-Day02-PhamThanhNguyen-2A202603030-ObjectDetection/blob/main/RUBRIC.md)

## 8. Công cụ AI và tài liệu tham khảo
- CVAT dùng để gán nhãn, Colab dùng train và đánh giá model.
