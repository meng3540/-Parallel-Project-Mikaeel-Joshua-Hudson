from ultralytics import YOLO

# Load a YOLO11n PyTorch model
model = YOLO("yolo11n.pt")

# Run inference
results = model(source = 0, stream = True)
results.print()  # Print results to console
results.show()  # Display results in a window
