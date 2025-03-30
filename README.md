# 🗓 Life Calendar

A Python visualization tool that helps you reflect on your life in weeks. This project renders a grid representing 90 years of life, with each square representing a week. The past weeks are shown in black, and the future ones remain white.

<p align="center">
  <img src="image.png" alt="Life Calendar Preview" width="500"/>
</p>

## ✨ Features

- 90-year life calendar (4680 weeks total).
- Automatically calculates past vs. future weeks based on your birth date.
- Clean, minimalist grid using rounded square cells.
- Built-in font for consistent aesthetics.
- Easy customization (colors, dimensions, labels).

## 📦 Requirements

- Python 3.6 or higher
- `matplotlib`

Install the required dependency:

```bash
pip install matplotlib
```

## 🧠 How It Works

Each cell in the 52×90 grid represents one week. The script:

1. Converts your birth date to a `datetime` object.
2. Iterates over all weeks up to 90 years.
3. Checks whether each week is in the past.
4. Draws filled (black) or empty (white) rounded rectangles accordingly.

## 🚀 Usage

1. Clone or download this repository.
2. Edit the `BIRTH_DATE` variable in the notebook or script.
3. Run the script to generate your life calendar.

```python
BIRTH_DATE = '1990-01-01'  # YYYY-MM-DD format

draw_life_calendar(
    birth_date_str=BIRTH_DATE,
    dpi=200
)
```

> **Note**: The required font (`BalsamiqSans-Regular.ttf`) is already included in the `fonts/` directory.

## 📁 Project Structure

```bash
lifecalendar/
├── image.png                        # Sample output image
├── life_calendar.ipynb             # Jupyter notebook version
├── fonts/
│   └── BalsamiqSans-Regular.ttf    # Custom font used in the visualization
└── README.md
```

## 🛠 Customization

You can easily tweak the following:

- **Font size or family**: Update the `font_path` or sizes inside the function.
- **Grid dimensions**: Change `num_years` in `generate_dates()`.
- **Colors**: Change `facecolor` and `edgecolor` in the `FancyBboxPatch`.
- **Output format**: Export as image/PDF using `plt.savefig()`.

## 📝 License

This project is licensed under the MIT License. Feel free to use, modify, and distribute it as you wish.
