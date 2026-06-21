# הקמת חיבור Claude ↔ Obsidian (אייפד)

מסמך זה מסביר איך להעביר את חבילת ה‑Vault שבתיקייה `obsidian-vault/`
לריפו הפרטי שלך ולחבר הכול באייפד.

## 1. צור ריפו פרטי
ב‑GitHub (אפליקציה או דפדפן): New repository → שם `obsidian-vault` →
סמן **Private** → Create.

## 2. העבר את חבילת ה‑Vault לריפו הפרטי
התוכן המוכן נמצא כאן בתיקייה `obsidian-vault/`. שתי דרכים להעביר:

- **דרך Working Copy באייפד:** Clone של הריפו הפרטי, ואז העתק לתוכו את הקבצים
  מתיקיית `obsidian-vault/` (אפשר להוריד אותם מ‑GitHub כ‑ZIP).
- **או:** הורד את התיקייה, ובאפליקציית GitHub/דפדפן העלה את הקבצים לריפו הפרטי.

## 3. חבר את Claude לריפו הפרטי
פתח **סשן Claude Code חדש** ב‑claude.ai/code (או באפליקציה) שמכוון לריפו
`obsidian-vault`. בסשן כזה יש ל‑Claude גישת קריאה/כתיבה מלאה ל‑Vault.

## 4. סנכרן לאייפד
1. **Working Copy** → Clone של `obsidian-vault`.
2. Working Copy → "Setup Folder Sync" → תיקייה ב‑Files.
3. **Obsidian** → "Open folder as vault" → אותה תיקייה.
4. עבודה שוטפת: **Pull** לקבלת שינויי Claude, **Commit + Push** לשליחת שלך.

## מבנה ה‑Vault
ראה `obsidian-vault/README.md` להסבר מלא על התיקיות והתבניות.
