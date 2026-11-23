# Aladdin365 Email Signature Generator

A small website where any Aladdin365 employee can type their details, see their signature,
and copy it into Gmail, Outlook or Apple Mail.

## Project structure

```
aladdin365-email-signature/
├── index.html              The generator page (form, live preview, copy buttons, instructions)
├── README.md               This file
└── assets/
    ├── logo.png            Aladdin365 logo (links to aladdin365.com)
    ├── itme-section.png    India ITME 2026 media partner panel (links to ITME 2026)
    ├── tagline.png         "CONNECTING THE TEXTILE & APPAREL INDUSTRY | Connect. Discover. Learn. Grow"
    ├── icon-facebook.png
    ├── icon-instagram.png
    └── icon-linkedin.png
```

## How it works

- The page uses a little JavaScript only to build the signature from the form.
  The signature itself is plain HTML tables with inline styles and contains no JavaScript.
- When the site is online (on Vercel), image links in the copied signature automatically use
  the site's own public address, for example
  `https://aladdin365-email-signature.vercel.app/assets/logo.png`.
- Long names or designations are made slightly smaller so they always fit in their column.

## Colours

The images are taken from the design exactly as it appears on screen (the design file is CMYK,
U.S. Web Coated SWOP, converted with its colour profile). Colours used in the HTML:

| Element | Colour |
|---|---|
| Employee details text | #383A3C |
| Cyan divider line | #49C0E8 |
| ITME panel background | #E1F4FD |
| Page background | #FFFFFF |

## Changing links later

Social media, website and ITME links are listed near the top of the `<script>` section of
`index.html` under `LINKS`.

## Notes

- Gmail cannot load custom fonts. People without Montserrat installed will see employee details in Arial.
  All other parts are images and look exactly like the design.
- The signature is 1000 px wide, matching the design. Phone email apps shrink it to fit.
- If someone's email app blocks images, they see descriptive text instead.
