# CSS Grid Alignment Cheat Sheet

## The Two Axes

### Block Axis (Vertical)
- Runs **top to bottom** (in English)
- Think: the direction **blocks stack** on a page
- Controlled by `align-*` properties

### Inline Axis (Horizontal)
- Runs **left to right** (in English)
- Think: the direction **text flows** in a line
- Controlled by `justify-*` properties

---

## Property Breakdown

### For Grid Items (individual items)

| Property | Axis | What It Does |
|----------|------|--------------|
| `align-self` | Block (vertical) | Aligns ONE item vertically within its cell |
| `justify-self` | Inline (horizontal) | Aligns ONE item horizontally within its cell |
| `place-self` | Both | Shorthand for both above |

**Example:**
```css
.item {
  align-self: center;      /* Centers vertically in its cell */
  justify-self: end;       /* Aligns to right in its cell */
  /* OR use shorthand: */
  place-self: center end;  /* align / justify */
}
```

---

### For Grid Container (all items)

| Property | Axis | What It Does |
|----------|------|--------------|
| `align-items` | Block (vertical) | Aligns ALL items vertically within their cells |
| `justify-items` | Inline (horizontal) | Aligns ALL items horizontally within their cells |
| `place-items` | Both | Shorthand for both above |

**Example:**
```css
.container {
  align-items: start;      /* All items align to top of cells */
  justify-items: center;   /* All items center horizontally in cells */
  /* OR use shorthand: */
  place-items: start center; /* align / justify */
}
```

---

### For Grid Tracks (the grid itself)

| Property | Axis | What It Does |
|----------|------|--------------|
| `align-content` | Block (vertical) | Aligns the entire grid vertically within the container |
| `justify-content` | Inline (horizontal) | Aligns the entire grid horizontally within the container |
| `place-content` | Both | Shorthand for both above |

**Example:**
```css
.container {
  height: 500px;
  align-content: center;    /* Centers whole grid vertically */
  justify-content: space-between; /* Spreads grid horizontally */
  /* OR use shorthand: */
  place-content: center space-between; /* align / justify */
}
```

---

## Column vs Row

### Columns (Vertical Tracks)
- Run **top to bottom** (along the block axis)
- Defined with `grid-template-columns`
- Items span columns using `grid-column`

### Rows (Horizontal Tracks)
- Run **left to right** (along the inline axis)
- Defined with `grid-template-rows`
- Items span rows using `grid-row`

**Example:**
```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;  /* 3 columns */
  grid-template-rows: 100px auto;      /* 2 rows */
}

.item {
  grid-column: 1 / 3;   /* Span from column line 1 to 3 */
  grid-row: 1 / 2;      /* Span from row line 1 to 2 */
}
```

---

## Quick Memory Tricks

### The Easy Way to Remember:

**ALIGN = BLOCK = VERTICAL** ⬆️⬇️
- `align-items`
- `align-self`
- `align-content`

**JUSTIFY = INLINE = HORIZONTAL** ⬅️➡️
- `justify-items`
- `justify-self`
- `justify-content`

### Items vs Content:
- **`*-items`**: Aligns items INSIDE their cells
- **`*-content`**: Aligns the whole grid (or tracks) within the container

### Common Values:
- `start` - beginning of axis
- `end` - end of axis
- `center` - middle of axis
- `stretch` - fill the space (default for items)
- `space-between` - space between tracks (content only)
- `space-around` - space around tracks (content only)
- `space-evenly` - even space everywhere (content only)

---

## Visual Reference

```
BLOCK AXIS (vertical) ↕️
     ↓
     |  INLINE AXIS (horizontal) ↔️
     |         →
     |  ┌─────┬─────┬─────┐
     |  │  1  │  2  │  3  │  ← Row 1
     ↓  ├─────┼─────┼─────┤
        │  4  │  5  │  6  │  ← Row 2
        └─────┴─────┴─────┘
          ↑     ↑     ↑
       Col 1  Col 2  Col 3
```

- `align-*` controls the ↕️ axis
- `justify-*` controls the ↔️ axis
- Columns run vertically ↕️
- Rows run horizontally ↔️