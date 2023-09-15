# Facedetect+
Machine learning project

Used the Teck stack: Jupyter, Opencv,NumPy

Short description of the project: 
• Developed a project to detect the faces of people using images of any format. In addition, the eyes and body parts can be
detected as well.
• The accuracy of the project to detect the faces is 86%
> In this project we are using Haarcascase classifier.
> Haarcascade_frontalface is a cascade classifier trained for face detection in computer vision and image processing.
> It's part of the Haar Cascade classifiers, a machine learning-based approach used for object detection, specifically faces in this case.

Things needed to know about project or imp libraries information:
cv2.imread() : It is used to read the image
cv2.cvtColor(): method is used to convert an image from one color space to another

Syntax: cv2.cvtColor(src, code[, dst[, dstCn]])

Parameters:
src: It is the image whose color space is to be changed.
code: It is the color space conversion code.
dst: It is the output image of the same size and depth as src image. It is an optional parameter.
dstCn: It is the number of channels in the destination image. If the parameter is 0 then the number of the channels is derived automatically from src and code. It is an optional parameter.

Return Value: It returns an image.

cv2.COLOR_BGR2GRAY is used to convert an image from the BGR (Blue, Green, Red) color space to grayscale

cv2.COLOR_BGR2BGRA  it converts an image from the BGR (Blue, Green, Red) color space to BGRA (Blue, Green, Red, Alpha) color space. 
The alpha channel represents the transparency or opacity of each pixel in the image. It allows you to create images with transparency, often referred to as "RGBA images" (Red, Green, Blue, Alpha), where you can control the visibility of each pixel.

cascade.detectMultiScale : is a function commonly used in the OpenCV library for object detection. It is particularly popular for tasks like face detection, pedestrian detection, and general object detection

Detects objects of different sizes in the input image. The detected objects are returned as a list of rectangles.

Parameters
image:	Matrix of the type CV_8U containing an image where objects are detected.
objects:	Vector of rectangles where each rectangle contains the detected object, the rectangles may be partially outside the original image.
scaleFactor:	Parameter specifying how much the image size is reduced at each image scale.
minNeighbors:	Parameter specifying how many neighbors each candidate rectangle should have to retain it.
flags:	Parameter with the same meaning for an old cascade as in the function cvHaarDetectObjects. It is not used for a new cascade.
minSize:	Minimum possible object size. Objects smaller than that are ignored.
maxSize:	Maximum possible object size. Objects larger than that are ignored. If maxSize == minSize model is evaluated on single scale.

cv2.rectangle() method is used to draw a rectangle on any image.

Syntax: cv2.rectangle(image, start_point, end_point, color, thickness)

Parameters:
image: It is the image on which rectangle is to be drawn.
start_point: It is the starting coordinates of rectangle. The coordinates are represented as tuples of two values i.e. (X coordinate value, Y coordinate value).
end_point: It is the ending coordinates of rectangle. The coordinates are represented as tuples of two values i.e. (X coordinate value, Y coordinate value).
color: It is the color of border line of rectangle to be drawn. For BGR, we pass a tuple. eg: (255, 0, 0) for blue color.
thickness: It is the thickness of the rectangle border line in px. Thickness of -1 px will fill the rectangle shape by the specified color.

Return Value: It returns an image.



Notes:
Color spaces are different types of color modes. Thus, these are used in image processing and signals & system for various purposes.
Popular and also has extensive use, such as RGB, CMYK, Y’UV, YIQ, Y’CbCr, HSV, etc.

Grayscale images are single-channel images where each pixel represents the intensity or brightness of the original image, rather than its color.

> Advantages of using the haarcascade_frontalface classifier for face detection:

Speed: Haar Cascade classifiers are known for their speed and efficiency.
Accuracy: While Haar Cascade classifiers may not be as accurate as some deep learning-based approaches (like Convolutional Neural Networks or CNNs), they still offer a reasonable level of accuracy for many practical applications. 
Robustness: Haar Cascade classifiers are trained on a large dataset of positive and negative images, making them robust to variations in pose, lighting conditions, and facial expressions.
Lightweight: These classifiers have a relatively small memory footprint, making them suitable for deployment on resource-constrained devices

Other similar cascade classifiers are:

LBP (Local Binary Pattern) Cascade: LBP is a texture descriptor that can be used for object detection. Cascade classifiers based on LBP are often used for detecting objects like faces.

HOG (Histogram of Oriented Gradients) Cascade: HOG is a feature descriptor that captures the local gradient information in an image. Cascade classifiers based on HOG are effective for detecting objects with distinctive shapes, such as pedestrians or cars.

AAM (Active Appearance Models) Cascade: Active Appearance Models combine shape and texture information to detect objects. They are often used for face detection and facial feature tracking.

LDF (Linear Discriminant Function) Cascade: Linear Discriminant Function Cascade classifiers use linear decision boundaries to separate objects from non-objects. They are sometimes used in simpler object detection tasks.

RAL (Rapid Adaboost Learning) Cascade: RAL is a cascade classifier designed to accelerate the training process of AdaBoost-based classifiers, making it suitable for real-time applications.

Facial Feature Cascade Classifiers: These classifiers are specialized for detecting specific facial features like eyes, noses, and mouths within the context of face detection. They can be used in conjunction with full-face detection.

Object-specific Cascade Classifiers: Depending on your application, you may come across cascade classifiers designed for specific objects like cars, license plates, or animals.
