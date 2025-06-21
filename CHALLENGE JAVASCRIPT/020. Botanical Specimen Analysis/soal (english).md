# 🌿 Botanical Specimen Analysis - Function Documentation

## 📌 Challenge Description

**Difficulty:** Easy

Create a function named `analyzePlantSpecimen` that analyzes a plant specimen and returns a formatted string containing various data points about the plant.

---

## 🔧 Function Declaration

```javascript
function analyzePlantSpecimen(plantName, numberOfLeaves, plantHeight)
```

---

## 🧾 Parameters

| Parameter      | Type   | Description                             |
| -------------- | ------ | --------------------------------------- |
| plantName      | String | The name of the plant specimen.         |
| numberOfLeaves | Number | The number of leaves on the plant.      |
| plantHeight    | Number | The height of the plant in centimeters. |

---

## 🔬 Analysis Rules

1. **Leaf Area (cm²):**

   * Each leaf is rectangular with a width of `1.5 cm`.
   * Formula: `singleLeafArea = plantHeight * 1.5`
   * Total leaf area: `totalLeafArea = singleLeafArea * numberOfLeaves`

2. **Height Conversion:**

   * Convert `plantHeight` from cm to inches: `heightInInches = plantHeight / 2.54`
   * Round to one decimal place.

3. **Height Classification:**

   * "short" if `< 30 cm`
   * "medium" if `30–100 cm`
   * "tall" if `> 100 cm`

4. **Color Code:**

   * Use the first letter of `plantName`, repeated 3 times.
   * Example: `"Fern"` → `"FFF"`

---

## 🧩 Sample Function Code

```javascript
function analyzePlantSpecimen(plantName, numberOfLeaves, plantHeight) {
  const leafWidth = 1.5;
  const singleLeafArea = plantHeight * leafWidth;
  const totalLeafArea = singleLeafArea * numberOfLeaves;
  const heightInInches = (plantHeight / 2.54).toFixed(1);

  let heightCategory = "";
  if (plantHeight < 30) {
    heightCategory = "short";
  } else if (plantHeight <= 100) {
    heightCategory = "medium";
  } else {
    heightCategory = "tall";
  }

  const colorCode = plantName[0].toUpperCase().repeat(3);

  return `Plant: ${plantName}\n` +
         `Leaves: ${numberOfLeaves}\n` +
         `Height: ${plantHeight} cm (${heightInInches} in)\n` +
         `Category: ${heightCategory}\n` +
         `Total Leaf Area: ${totalLeafArea.toFixed(2)} cm²\n` +
         `Color Code: ${colorCode}`;
}
```

---

## 💡 Example Usage

```javascript
console.log(analyzePlantSpecimen("Fern", 10, 45));
```

### ✅ Output

```
Plant: Fern
Leaves: 10
Height: 45 cm (17.7 in)
Category: medium
Total Leaf Area: 675.00 cm²
Color Code: FFF
```

---

## 🧪 Additional Examples

```javascript
console.log(analyzePlantSpecimen("Bamboo", 20, 150));
```

```
Plant: Bamboo
Leaves: 20
Height: 150 cm (59.1 in)
Category: tall
Total Leaf Area: 4500.00 cm²
Color Code: BBB
```

```javascript
console.log(analyzePlantSpecimen("Moss", 5, 12));
```

```
Plant: Moss
Leaves: 5
Height: 12 cm (4.7 in)
Category: short
Total Leaf Area: 90.00 cm²
Color Code: MMM
```

---

## 📎 Notes

* This function is great for practicing basic math operations, string formatting, and conditional logic in JavaScript.
* It helps demonstrate how multiple outputs can be logically organized and formatted for readability.

---

Happy analyzing your botanical specimens! 🌱
