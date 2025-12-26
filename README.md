================================================================================
        AI-DRIVEN PHOTO RESTORATION SYSTEM WITH OPENCV
================================================================================

A complete toolkit for restoring and processing old photos using computer 
vision techniques powered by OpenCV and AI models.

================================================================================
FEATURES
================================================================================

1. PHOTO REPAIR (OpenCV Inpainting)
   - Automatic crack and damage detection
   - Manual red-marking support for precise control
   - Face-aware processing to preserve facial details
   - Works 100% offline with no large downloads

2. AI BACKGROUND REMOVAL
   - rembg + U2-Net pretrained model (best quality)
   - OpenCV GrabCut fallback (no external dependencies)
   - Export as transparent PNG or custom background colors
   - Optimized models for portraits and general images

================================================================================
REQUIREMENTS
================================================================================

Core Dependencies (Required):
- Python 3.x
- numpy==1.26.5
- opencv-python==4.8.1.78
- matplotlib==3.8.2
- Pillow>=9.0.0

Optional Dependencies (for AI features):
- rembg>=2.0.50
- onnxruntime>=1.15.0

Note: Optional dependencies enable advanced background removal with AI models.
      The system will work with core dependencies alone using OpenCV methods.

================================================================================
INSTALLATION
================================================================================

1. Install Required Dependencies:
   pip install numpy==1.26.5 opencv-python==4.8.1.78 matplotlib==3.8.2 Pillow

2. Install Optional Dependencies (Recommended for AI features):
   pip install rembg onnxruntime

3. Or install all at once:
   pip install -r requirements.txt

================================================================================
PROJECT STRUCTURE
================================================================================

AI-DRIVEN-PHOTO-RESTORATION-SYSTEM-WITH-OPENCV-/
├── Main Project Execution.ipynb   # Main Jupyter notebook with all code
├── requirements.txt                # Python dependencies
├── DATA/                          # Input images directory
├── masks/                         # Generated masks directory
├── Output Images/                 # Processed output directory
└── README.txt                     # This file

================================================================================
QUICK START GUIDE
================================================================================

1. Open the Jupyter Notebook:
   jupyter notebook "Main Project Execution.ipynb"

2. Update the INPUT_IMAGE_NAME variable in Cell 3 with your image filename
   (Place your image in the DATA/ folder)

3. Run the cells in order:
   - Cell 1: Environment Check
   - Cell 2: Project Initialization
   - Cell 3: Configuration (Set your image name here)
   - Cell 4: Helper Functions
   - Cell 5: Photo Repair/Restoration
   - Cell 6: Run photo repair
   - Cell 7: Background Removal (Optional)

4. Check the "Output Images/" folder for results

================================================================================
USAGE EXAMPLES
================================================================================

PHOTO RESTORATION:
- Place damaged/old photo in DATA/ folder
- Set INPUT_IMAGE_NAME = "your_photo.jpg"
- Run Cell 5 (Photo Repair) to restore the image
- The system will detect cracks and damages automatically
- Or manually mark damages in red for precise control

BACKGROUND REMOVAL:
- Place photo in DATA/ folder
- Set INPUT_IMAGE_NAME = "your_photo.jpg"
- Run Cell 7 (Background Removal)
- Choose between AI method (rembg) or OpenCV GrabCut
- Export as transparent PNG or with custom background

================================================================================
TECHNICAL DETAILS
================================================================================

Photo Repair Methods:
- OpenCV inpainting algorithms (Telea, Navier-Stokes)
- Automatic edge detection for crack identification
- Morphological operations for damage detection
- Face detection to preserve facial features

Background Removal Methods:
- AI-based: U2-Net model via rembg library
- Classical: OpenCV GrabCut algorithm
- Supports custom background colors
- PNG export with transparency

================================================================================
TROUBLESHOOTING
================================================================================

Q: ModuleNotFoundError for rembg
A: Install optional dependencies: pip install rembg onnxruntime
   Or use OpenCV GrabCut method instead

Q: Images not loading
A: Ensure images are placed in the DATA/ folder
   Check that INPUT_IMAGE_NAME matches the actual filename

Q: Poor restoration quality
A: Try manual red-marking for precise damage control
   Adjust inpainting parameters in the code

Q: Background removal not accurate
A: Use AI method (rembg) for better results
   Or adjust GrabCut parameters for specific images

================================================================================
OUTPUTS
================================================================================

All processed images are saved in the "Output Images/" directory with
descriptive filenames indicating the operation performed.

Generated masks are saved in the "masks/" directory for reference and
debugging purposes.

================================================================================
LICENSE & CREDITS
================================================================================

This project uses:
- OpenCV (Apache 2.0 License)
- NumPy (BSD License)
- Pillow (PIL License)
- rembg (MIT License)
- U2-Net model (Apache 2.0 License)

================================================================================
CONTACT & SUPPORT
================================================================================

For issues, questions, or contributions, please refer to the project
repository or contact the maintainer.

================================================================================
VERSION HISTORY
================================================================================

v1.0 - Initial release with photo repair and background removal features

================================================================================
