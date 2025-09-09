# World Script Data Analysis

A collection of datasets and tools for analyzing writing systems (scripts) from around the world.  
Includes information about Unicode ranges, writing directions, years of origin, and whether the scripts are still in use today.

## 📂 Projects

### 1. [Unicode Scripts](./characterScript.js)
A JavaScript dataset of world writing systems, with metadata such as Unicode ranges, script direction, and references.

### 2. [Analyzer](./characterCount.js)
A tool that uses the dataset to analyze text and detect which script(s) are present.

## 🚀 Possible Use Cases
- Detect the script of any given character or text
- Study the distribution of living vs extinct scripts
- Build educational or linguistic research tools

# 3. [Unicode Scripts Dataset](./characterScript.js)

This repository contains a JavaScript dataset that describes a wide variety of writing systems used throughout history and in modern times. Each script is represented as an object with metadata, including its Unicode ranges, writing direction, and historical details.

## Dataset Structure

The dataset is an array of objects (`SCRIPTS`), where each object has the following properties:

- **`name`**: The name of the script (e.g., `"Latin"`, `"Cyrillic"`, `"Arabic"`).
- **`ranges`**: An array of Unicode code point ranges (start and end values) that define which characters belong to the script.
- **`direction`**: The writing direction of the script:
  - `ltr` → left-to-right  
  - `rtl` → right-to-left  
  - `ttb` → top-to-bottom
- **`year`**: Approximate year when the script was created.
- **`living`**: A boolean indicating whether the script is still in active use (`true`) or extinct (`false`).
- **`link`**: A reference link (usually a Wikipedia article) for more details about the script.

## Example Entry

```js
{
  name: "Latin",
  ranges: [[65, 91], [97, 123], ...],
  direction: "ltr",
  year: -700,
  living: true,
  link: "https://en.wikipedia.org/wiki/Latin_script"
}

