import cv2
from ultralytics import YOLO
import torch

# Load the YOLO model
model = YOLO("yolo11n.pt")  # pretrained YOLO11n model
model.to("cuda")
# Open webcam
cap = cv2.VideoCapture(0)

if not cap.isOpened():
    print("Error: Could not open webcam.")
    exit()

while True:
    # Capture frame-by-frame
    ret, frame = cap.read()
    if not ret:
        print("Error: Failed to capture frame.")
        break

    # Run inference on the frame
    results = model(frame)

    # Annotate the frame with results
    annotated_frame = results[0].plot()

    # Display the annotated frame
    cv2.imshow("YOLO Webcam Stream", annotated_frame)

    # Break the loop if 'q' is pressed
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

# Release the video capture object and close the display window
cap.release()
cv2.destroyAllWindows()
