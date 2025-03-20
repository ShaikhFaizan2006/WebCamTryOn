# Advanced Virtual Try-On

This application allows you to virtually try on clothing using your webcam. It utilizes computer vision and pose estimation to overlay garments on your body in real-time.

## Features

- Real-time garment overlay on webcam feed
- Pose estimation to track body movements
- Adjustable garment sizing and positioning
- Background removal for garment images
- Debug mode to visualize pose skeleton
- Three modes of operation: standalone with Tkinter UI, command-line, and Streamlit web interface

## Requirements

Install the required dependencies using pip:

```
pip install -r requirements.txt
```

## Usage

### Tkinter UI Mode (Recommended)

Run the application with a graphical user interface:

```
python app.py
```

or explicitly with:

```
python app.py --tkinter
```

The Tkinter UI provides:
- File browser for selecting garment images
- Real-time garment preview
- Sliders for adjusting width, height, and collar position
- Toggle for skeleton display
- Start/Stop controls

### Command-line Mode

Run the application in traditional command-line mode:

```
python app.py --garment path/to/garment.png
```

Optional arguments:
- `--webcam`: Webcam index to use (default: 0)
- `--resolution`: Camera resolution (default: 640x480)

Controls:
- '+'/'-': Adjust garment width
- 'Up'/'Down' arrows: Adjust garment height
- '<'/'>': Adjust collar position
- 'd': Toggle debug mode (skeleton visualization)
- 'c': Toggle control display
- 'f': Toggle performance mode
- 's': Toggle fullscreen mode
- 'q': Quit

### Streamlit Web Interface

Run the application as a Streamlit web app:

```
python app.py --streamlit
```

Or you can run it directly with Streamlit:

```
streamlit run app.py -- --streamlit
```

The web interface provides:
- Garment upload through the UI
- Sliders for adjusting garment fit
- Live webcam view with virtual try-on

## Notes

- For best results, use garment images with transparent backgrounds (PNG format)
- Good lighting improves pose estimation accuracy
- The application works best with the person facing the camera directly 