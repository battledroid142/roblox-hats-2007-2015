# Roblox Hats & Accessories Dataset (2007–2015)

An unofficial, public-domain dataset of Roblox catalog items (primarily hats and accessories) released between 2007 and 2015. 

This repository provides the data in two standard formats for easy use in your own projects, tools, or analyses:
* `roblox_items.csv` — The primary dataset (comma-separated values).
* `roblox_items.json` — The same dataset formatted as JSON.

## Data Schema

Here are the fields included for each item in the dataset:

| Field | Type | Notes |
| :--- | :--- | :--- |
| `id` | Integer | The unique Roblox asset ID. |
| `name` | String | The name of the item. |
| `description` | String | The item description. May be empty or contain quotes/newlines. |
| `price` | Integer / String | The price in Robux. **See note below.** |
| `creator` | String | The creator of the item (e.g., "Roblox"). |
| `creator_type` | String | The type of creator (e.g., "User"). |
| `item_type` | String | The type of item (e.g., "Asset"). |
| `asset_type` | Integer | The Roblox asset type ID (e.g., 8 for Hats, 41 for Hair, 42 for Face). |
| `limited` | Boolean | `true` or `false`. |
| `offsale` | Boolean | `true` or `false`. |

### Important Data Notes
* **Price Formatting:** Because some items cannot be bought with Robux, the `price` field is a mixed type. It is usually an integer (e.g., `95`), but for some items, it is the string `"Free/Offsale"`.
* **Booleans:** In the CSV file, `limited` and `offsale` are stored as `True`/`False` (capitalized). In the JSON file, they are standard JSON booleans (`true`/`false`).
* **Missing Data:** Some items have empty descriptions.

## Usage

You don't need to install anything to use this data. You can:
* Download the files directly and open them in Excel, Google Sheets, or your preferred text editor.
* Fetch the raw files directly into your Python, JavaScript, or Lua projects via the GitHub Raw URL.

## Data Quirks

Note: The price column contains integers and the string "Free/Offsale". Please clean this in your code if you are doing numerical analysis.

## Limited

The limited field is not populated in this snapshot and should not be trusted.

## License

This dataset compilation is released into the public domain under **The Unlicense**. You are free to copy, modify, publish, use, or distribute it for any purpose, commercial or non-commercial, without asking for permission.

## Disclaimer

This is an unofficial community dataset. It is not affiliated with, endorsed by, or sponsored by Roblox Corporation. Item names, descriptions, and metadata belong to their respective owners. This data is provided for archival and research purposes.
