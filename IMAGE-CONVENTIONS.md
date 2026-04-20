# PrintPlayHouse — Image Conventions

> Consistent, SEO-friendly image naming and optimization standards for the PrintPlayHouse image repository.

---

## 1. Folder Structure

Each product gets its own folder, named with the product's URL slug.

```
{product-slug}/
├── product-front.jpg
├── product-detail-closeup.jpg
├── lifestyle-secondary.jpg
└── ugc-social-media.jpg
```

**Example — Keeper Hoodie:**

```
keeper-hoodie/
├── product-front.jpg
├── product-detail-closeup.jpg
├── lifestyle-secondary.jpg
└── ugc-social-media.jpg
```

---

## 2. File Naming Rules

| Rule | Detail |
|---|---|
| **Lowercase only** | `keeper-hoodie-front.jpg` ✅ `KeeperHoodie_Front.jpg` ❌ |
| **Hyphens, not underscores** | `product-front.jpg` ✅ `product_front.jpg` ❌ |
| **No spaces** | Never use spaces in filenames |
| **Descriptive, keyword-rich** | Include product slug when used outside its folder |
| **No version numbers in filenames** | Use Git history for versioning |

---

## 3. Shot Types

Every product should have all four shot types. New shot types may be added as needed.

| Filename | Shot Type | Purpose | Background |
|---|---|---|---|
| `product-front.jpg` | Clean product shot | Primary ecommerce image, thumbnails | White or cream (`#FDF6EC`) |
| `product-detail-closeup.jpg` | Macro / detail | Show print quality, texture, hardware | Neutral, blurred |
| `lifestyle-secondary.jpg` | Lifestyle | Show fit, movement, context | Real-world environment |
| `ugc-social-media.jpg` | UGC-style | Social proof, Instagram/TikTok | Candid, natural |

---

## 4. Image Specifications

| Spec | Requirement |
|---|---|
| **Format** | JPEG for photos, PNG for any graphic/flat-lay with transparency |
| **Color space** | sRGB |
| **Resolution** | 72 DPI (web) |
| **Product shot dimensions** | 1000 × 1000 px (1:1 square) |
| **Lifestyle shot dimensions** | 1200 × 1500 px (4:5 portrait) or 1200 × 800 px (3:2 landscape) |
| **Max file size** | 300KB for product shots, 500KB for lifestyle |
| **Quality** | JPEG quality 80–85 (balance of sharpness and size) |

> **WebP:** Where the platform supports it, serve WebP versions. Keep the original JPEG as the source of truth in this repo.

---

## 5. Alt Text Standards

Alt text is written in `PRODUCT-COPY.md` for each product. The formula is:

```
PrintPlayHouse {Product Name} — {shot description}
```

**Examples:**

| Shot | Alt Text |
|---|---|
| `product-front.jpg` | `PrintPlayHouse Keeper Hoodie — front product shot showing full graphic print` |
| `product-detail-closeup.jpg` | `PrintPlayHouse Keeper Hoodie — close-up of bold graphic print detail` |
| `lifestyle-secondary.jpg` | `PrintPlayHouse Keeper Hoodie — lifestyle photo, model wearing relaxed fit outdoors` |
| `ugc-social-media.jpg` | `PrintPlayHouse Keeper Hoodie — UGC social media shot, styled and worn by customer` |

**Rules:**
- Always start with the brand name
- Describe what is actually in the image
- Include the product name
- No keyword stuffing — write for a screen reader, not a search engine
- Maximum 125 characters

---

## 6. Versioning & Updates

- Images are version-controlled via Git
- To replace an image, commit the new file with the same filename — Git history preserves the old version
- Never rename image files after they have been published (breaks live URLs)
- If a completely new image replaces an old one for SEO reasons, add a redirect from the old URL in the platform

---

## 7. CDN Usage

Images in this repository are served as stable URLs via GitHub's raw content CDN:

```
https://raw.githubusercontent.com/naoufac/printplay-house-images/main/{product-slug}/{filename}
```

**Example:**
```
https://raw.githubusercontent.com/naoufac/printplay-house-images/main/keeper-hoodie/product-front.jpg
```

Use these URLs in:
- Product page image `src` attributes
- Structured data (`Product` schema `image` field)
- Email templates
- Social media link previews (Open Graph `og:image`)

---

## 8. Adding a New Product

1. Create a folder: `{product-slug}/`
2. Add all four required images (see §3)
3. Name files exactly as specified (see §2)
4. Write alt text in `PRODUCT-COPY.md`
5. Add the product to the table in `README.md`
6. Open a PR with the new images

---

*Last updated: April 2026*
