# Traffic_Sign_ComputerVision

Traffic Sign Detection – Raspberry Pi / Linux
Real-time German traffic sign detection via YOLO and live camera feed. Built for Raspberry Pi / Linux with libcamera.

⚠️ Dieses Projekt ist für Raspberry Pi / Linux entwickelt. Auf Windows muss libcamera-still durch cv2.VideoCapture() ersetzt werden.

Features

Erkennung von 43 deutschen Verkehrsschildern
Live-Kamera-Feed via libcamera-still (Raspberry Pi Camera Module)
PyQt5 GUI mit 20 FPS Update-Rate
Konfidenz-Anzeige pro erkanntem Schild (Threshold: 50%)
Konsolenausgabe aller Erkennungen mit Konfidenzwert

Voraussetzungen
Hardware

Raspberry Pi mit Camera Module
Linux / Raspberry Pi OS

Software
bashpip install opencv-python numpy ultralytics PyQt5 Pillow

## Modell

Das YOLO-Modell `best.pt` muss unter folgendem Pfad liegen: /home/tary/best.pt

Der Pfad kann in der Datei traffic_signs.py angepasst werden:
pythonMODEL_PATH = "/home/tary/best.pt"
Erkannte Schildklassen
43 Klassen: Tempo 20–120, Überholverbote, Vorfahrtsschilder, Gefahrenzeichen, Richtungsgebote u.v.m.
Usage
bashpython traffic_signs.py
Hinweis für Windows-Nutzer
libcamera-still ist nicht verfügbar. start_camera_capture() und update_frame() müssen auf cv2.VideoCapture(0) umgestellt werden.
