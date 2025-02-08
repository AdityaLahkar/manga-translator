1. Basic Pipeline for One Panel
    1. Extract Text (OCR)
        Use Tesseract OCR or PaddleOCR to detect and extract Chinese text from speech bubbles.
    2. Erase Text from Bubbles
        Use OpenCV inpainting or AI-based inpainting (LaMa) to remove the original text.
    3. Translate Text
        Use Google Translate API, DeepL API, or a custom model for translation.
    4. Context Management
        Store translations in a dictionary (JSON/DB) to ensure consistency across panels.
    5. Reinsert Translated Text
        Use Pillow or OpenCV to write the English text back into the speech bubbles.
    6. Output Translated Panel
        Save the edited panel as a new image/PDF.

2. Scaling for Multiple Panels (with Context Tracking)
    * Store translations in a database so that the same terms, names, and phrases remain consistent.
    * Implement a review/edit option before reinserting text for manual correction.


* Tech Stack
    * OCR: PaddleOCR / Tesseract OCR
    * Text Removal: OpenCV / LaMa AI inpainting
    * Translation: Google Translate API / DeepL API
    * Storage for Context: SQLite / JSON / Local DB
    * Image Processing: Pillow / OpenCV
    * UI (Optional): Tkinter / Flask / React (if making a web tool)