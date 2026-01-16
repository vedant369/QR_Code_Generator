# QR Code Generator

A simple Python-based QR code generator that creates customizable QR codes from URLs or text input. Built for use in Jupyter Notebooks with inline display capabilities.

## Features

- Generate QR codes from any URL or text
- Customizable appearance (colors, size, border)
- Display QR codes directly in Jupyter Notebook
- Save QR codes as PNG files
- High error correction level for better scanning reliability

## Requirements

- Python 3.x
- qrcode library with PIL support
- Pillow (PIL)
- IPython (for Jupyter Notebook display)

## Installation

Install the required dependencies using pip:

```bash
pip install qrcode[pil] pillow
```

## Usage

### Basic Usage

1. Open the Jupyter Notebook `QR_Code_Generator.ipynb`
2. Run all cells
3. When prompted, enter the URL or text you want to encode
4. The QR code will be displayed in the notebook and saved as `qrcode.png`

### Function Parameters

The `generate_qr()` function accepts the following parameters:

- `url` (str): The URL or text to encode in the QR code
- `box_size` (int, default=10): Size of each box in the QR code grid
- `border` (int, default=4): Width of the border (minimum is 4)
- `fill_color` (str, default="black"): Color of the QR code pattern
- `back_color` (str, default="white"): Background color
- `filename` (str, default="qrcode.png"): Output filename for the saved image

### Example

```python
from QR_Code_Generator import generate_qr

# Generate a basic QR code
generate_qr("https://example.com")

# Generate a customized QR code
generate_qr(
    url="https://example.com",
    box_size=15,
    border=2,
    fill_color="darkblue",
    back_color="lightgray",
    filename="custom_qr.png"
)
```

## Output

The generated QR code will:
- Be displayed inline in the Jupyter Notebook
- Be saved as a PNG file in the current directory
- Use high error correction (ERROR_CORRECT_H) for robust scanning

## License

This project is open source and available for personal and commercial use.

## Contributing

Feel free to submit issues or pull requests for improvements and bug fixes.
