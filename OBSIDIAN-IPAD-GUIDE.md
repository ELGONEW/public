# 📱 מדריך מלא: Claude + Obsidian באייפד

מדריך שלב‑אחר‑שלב להקמת Vault מסונכרן ב‑Git, שעובד גם באייפד שלך וגם
מאפשר ל‑Claude לעבוד עליו. כל שלב כולל תיאור מילולי של מה אתה אמור לראות
על המסך ("צילום מסך במילים"), כך שלא תלך לאיבוד.

> ⏱️ זמן כולל משוער: 20–30 דקות. צריך לעשות את זה פעם אחת בלבד.

---

## 🧰 מה צריך להתקין מראש

מ‑App Store, התקן את שלוש האפליקציות:
1. **Obsidian** — אפליקציית הפתקים (כבר התקנת ✅).
2. **Working Copy** — לקוח Git לאייפד (חינם לשימוש הבסיסי שנצטרך).
3. **GitHub** — לניהול הריפו (אפשר גם דרך Safari, אבל האפליקציה נוחה).

---

## חלק א' — יצירת ריפו פרטי ב‑GitHub

1. פתח את אפליקציית **GitHub** והתחבר לחשבון `ELGONEW`.
2. בפינה השמאלית‑תחתונה לחץ על אייקון ה‑**+** (או על תמונת הפרופיל → "New").
   *מה תראה:* תפריט עם האפשרות **"New repository"**.
3. בחר **New repository** ומלא:
   - **Repository name:** `obsidian-vault`
   - **Visibility:** בחר **Private** 🔒 (חשוב! הפתקים אישיים)
   - סמן **"Add a README file"**
4. לחץ **Create repository**.
   *מה תראה:* דף הריפו החדש עם קובץ `README.md` בודד.

✅ עכשיו יש לך ריפו פרטי ריק.

---

## חלק ב' — חיבור Working Copy לחשבון GitHub

1. פתח את **Working Copy**.
2. לחץ על אייקון ה‑**+** למעלה → **"Clone repository"**.
   *מה תראה:* מסך שמבקש כתובת ריפו, ולמטה כפתור התחברות ל‑GitHub.
3. לחץ **"Sign in with GitHub"** ואשר את ההרשאות.
   *מה תראה:* רשימת הריפואים שלך, כולל `obsidian-vault` ו‑`public`.

---

## חלק ג' — העברת חבילת ההתחלה לריפו הפרטי

חבילת ה‑Vault שהוכנה נמצאת כרגע בריפו **`public`** (בענף
`claude/obsidian-integration-setup-6unsmz`), בתיקייה `obsidian-vault/`.
צריך להעתיק אותה לריפו הפרטי. הדרך הנוחה באייפד:

1. ב‑Working Copy, **Clone** את הריפו `public`:
   - בחר אותו מהרשימה → בחר את הענף `claude/obsidian-integration-setup-6unsmz`.
2. **Clone** גם את `obsidian-vault` (הפרטי).
3. פתח את `public` ב‑Working Copy, היכנס לתיקייה `obsidian-vault/`,
   ולחץ **Select** → בחר את כל הקבצים והתיקיות שבתוכה.
4. **Copy** → עבור לריפו `obsidian-vault` → **Paste**.
   *מה תראה:* כל מבנה התיקיות (Inbox, Notes, Templates...) מופיע בריפו הפרטי.
5. ב‑`obsidian-vault`: לחץ **Commit** (כתוב הודעה כמו "Initial vault") ואז **Push**.

> 💡 חלופה פשוטה יותר: ב‑GitHub הורד את התיקייה כ‑ZIP, חלץ ב‑Files, וגרור
> לתוך הריפו ב‑Working Copy. אבל לרוב העתק/הדבק בין שני ריפואים נוח יותר.

---

## חלק ד' — סנכרון התיקייה ל‑Files (כדי ש‑Obsidian יראה אותה)

1. ב‑Working Copy, פתח את הריפו `obsidian-vault`.
2. בתפריט (שלוש נקודות בפינה) בחר **"Setup Folder Sync"** או
   **"Share Repository in Files"**.
   *מה תראה:* בקשה לבחור תיקיית יעד באפליקציית **Files**.
3. בחר מיקום (למשל "On My iPad" → תיקייה חדשה בשם `ObsidianVault`).
4. אשר. Working Copy ישמור עכשיו עותק חי של הריפו שם, ויסנכרן שינויים.

---

## חלק ה' — פתיחת ה‑Vault ב‑Obsidian

1. פתח את **Obsidian**.
2. במסך הפתיחה בחר **"Open folder as vault"**.
   *מה תראה:* דפדפן קבצים של iOS.
3. נווט ל‑`Files → On My iPad → ObsidianVault` (התיקייה מחלק ד') ובחר **Open**.
   *מה תראה:* Obsidian נפתח עם `Home.md`, ובסרגל הצד התיקיות Inbox/Notes/וכו'.
4. הפעל את התבניות: **Settings (גלגל שיניים) → Core plugins → הפעל "Templates"**.
5. **Settings → Templates → Template folder location** → בחר `Templates`.
   *מעכשיו:* לחיצה על "Insert template" תציע את Daily Note / Meeting / Project / Note.

✅ ה‑Vault עובד באייפד!

---

## חלק ו' — חיבור Claude לריפו הפרטי

כדי שאני (Claude) אוכל ליצור ולערוך פתקים ב‑Vault:

1. בדפדפן/אפליקציה היכנס ל‑**claude.ai/code**.
2. בבחירת סביבת העבודה / הריפו, בחר את **`obsidian-vault`** (הפרטי).
3. פתח שיחה חדשה — משם תהיה לי גישת קריאה/כתיבה מלאה ל‑Vault, ואוכל לדחוף שינויים.

---

## חלק ז' — זרימת העבודה היומיומית

| מתי | מה לעשות | איפה |
|------|-----------|------|
| לפני שמתחילים לעבוד | **Pull** | Working Copy → repo → Pull |
| אחרי שכתבת/ערכת פתקים | **Commit** ואז **Push** | Working Copy |
| אחרי ש‑Claude עבד על ה‑Vault | **Pull** כדי לראות שינויים | Working Copy |

> ⚠️ **חשוב:** עשה Pull לפני עריכה ו‑Push אחרי עריכה, כדי להימנע
> מהתנגשויות (conflicts). אם בכל זאת נוצר conflict, Working Copy יראה לך
> אותו ויאפשר לבחור גרסה.

---

## 🆘 פתרון תקלות נפוצות

- **Obsidian לא רואה את התיקייה** → ודא שעשית "Setup Folder Sync" בחלק ד',
  ושבחרת את תיקיית הסנכרון (ולא את הריפו ישירות).
- **התבניות לא עובדות** → ודא שהפלאגין "Templates" מופעל ושמוגדרת תיקיית
  `Templates` (חלק ה', שלבים 4–5).
- **שינויים של Claude לא מופיעים** → עשה **Pull** ב‑Working Copy; שינויי Claude
  מגיעים כ‑commits בריפו.
- **התנגשות (merge conflict)** → תמיד עדיף Pull לפני שמתחילים לערוך.

---

## 🔒 הערת אבטחה
לאחר שהעברת בהצלחה את התוכן לריפו הפרטי, כדאי למחוק את תיקיית
`obsidian-vault/` מהריפו הציבורי `public` כדי לא להשאיר אותה גלויה.
אני יכול לעשות זאת עבורך — רק בקש.
