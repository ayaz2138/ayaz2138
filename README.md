import cv2

def access_camera():
    camera = cv2.VideoCapture(0)  # 0 represents the default camera
    while True:
        ret, frame = camera.read()
        cv2.imshow("Camera Feed", frame)
        if cv2.waitKey(1) == ord('q'):  # Press 'q' to exit
            break
    camera.release()
    cv2.destroyAllWindows()

access_camera()
