---
name: geo-analyzer
description: "GEO (Generative Engine Optimization) analysis skill for the Israeli market. Analyzes how well companies in a given sector appear and are recommended by AI engines (ChatGPT, Gemini, Google AI Overview, Claude, Grok). Use this skill whenever the user asks about GEO status, AI visibility of companies, how companies show up in AI search engines, generative engine optimization analysis, or wants to compare companies' presence across AI platforms. Also trigger when the user mentions 'ניתוח GEO', 'נוכחות במנועי AI', 'אופטימיזציה למנועי חיפוש גנרטיביים', or asks about any company's visibility in ChatGPT/Gemini/Claude/Grok. Always produces an Excel (.xlsx) output file."
---

# GEO Analyzer — ניתוח נוכחות חברות במנועי AI

## מה ה-Skill הזה עושה

ה-Skill מקבל שם של סקטור בשוק הישראלי ומייצר קובץ Excel מקצועי שמנתח את מצב ה-GEO (Generative Engine Optimization) של 20 חברות גדולות ובינוניות בסקטור.

## הגדרות יסוד

**GEO = Generative Engine Optimization** — המידה שבה חברה מופיעה, מוזכרת, ומומלצת בתשובות של מנועי AI גנרטיביים. זה שונה מ-SEO קלאסי: ב-GEO לא מדובר על דירוג בתוצאות חיפוש, אלא על הנוכחות של המותג בתוך התשובה הטקסטואלית שהמנוע מייצר.

**מנועי AI לבדיקה:**
1. **ChatGPT** (OpenAI) — המנוע הפופולרי ביותר
2. **Gemini** (Google) — משולב ב-Google ecosystem
3. **Google AI Overview** — התשובות המסוכמות בראש תוצאות Google
4. **Claude** (Anthropic) — ידוע בדיוק ובעומק
5. **Grok** (xAI) — משולב ב-X/Twitter

## תהליך העבודה

### שלב 1: זיהוי חברות

כשהמשתמש מציין סקטור, חפש (web search) את 20 החברות הגדולות/בינוניות המובילות בסקטור הזה בישראל. התמקד בחברות שיש להן נוכחות דיגיטלית משמעותית (אתר, תוכן, פעילות אונליין). לכל חברה, מצא את ה-URL של האתר הראשי שלה.

### שלב 2: ניתוח GEO לכל חברה

לכל חברה מתוך ה-20, בצע חיפוש אינטרנטי מקיף כדי להעריך את הנוכחות שלה בכל אחד מ-6 המנועים. 

**מה לבדוק עבור כל מנוע AI:**
- האם החברה מוזכרת כשמחפשים את הסקטור שלה? (לדוגמה: "מהן חברות הביטוח הטובות בישראל")
- האם החברה מומלצת או שהיא רק מוזכרת?
- האם המידע עליה מדויק ועדכני?
- האם יש לה תוכן מובנה שמנועי AI יכולים לשאוב ממנו?

**איך לחפש:**
השתמש ב-web search עם שאילתות כמו:
- `"[company name]" site:reddit.com OR site:quora.com` — לבדוק נוכחות במקורות ש-AI שואב מהם
- `"[company name]" [sector] Israel best` — לראות איך החברה מופיעה בהקשרים של המלצות
- `"[company name]" review OR recommendation [sector]` — נוכחות בביקורות והמלצות
- `[sector] companies Israel` — לבדוק אם החברה מופיעה ברשימות

**סימנים לנוכחות GEO חזקה:**
- תוכן עשיר ומובנה באתר (FAQ, בלוג, מדריכים)
- נוכחות רבה ב-Wikipedia, דפי ידע, ומקורות סמכותיים
- ביקורות חיוביות רבות ב-Google, TrustPilot ודומים
- מוזכרת במאמרים ורשימות "הטובים ביותר"
- Schema markup ו-structured data באתר
- תוכן בעברית ובאנגלית

**סימנים לנוכחות GEO חלשה:**
- אתר דל תוכן או ישן
- אין נוכחות ב-Wikipedia או מקורות סמכותיים
- מעט ביקורות או ביקורות שליליות
- לא מופיעה ברשימות והמלצות
- אין structured data
- תוכן רק בשפה אחת

### שלב 3: ציון משוכלל

**משקלות ברירת מחדל** (המשתמש יכול לשנות):

| מנוע | משקל ברירת מחדל | סיבה |
|-------|---------|-------|
| ChatGPT | 35% | המנוע הדומיננטי ביותר בשוק |
| Gemini | 5% | נתח שוק קטן יחסית |
| Google AI Overview | 25% | משפיע ישירות על חיפוש אורגני |
| Claude | 5% | קהל מצומצם |
| Grok | 5% | קהל מצומצם |
| Google Search (organic) | 25% | בסיס הנוכחות הדיגיטלית |

**שאל את המשתמש** בתחילת התהליך אם הוא רוצה לשנות את המשקלות. אם כן, עדכן בהתאם. אם לא, השתמש בברירת המחדל.

כל מנוע מקבל ציון 1-10:
- **9-10**: החברה מוזכרת ומומלצת באופן בולט, מידע מדויק ועדכני
- **7-8**: מוזכרת בעקביות, אך לא תמיד כהמלצה ראשונה
- **5-6**: מוזכרת לפעמים, מידע חלקי
- **3-4**: כמעט לא מוזכרת, מידע לא מדויק
- **1-2**: לא מופיעה כלל או מידע שגוי

ציון משוכלל = ממוצע משוקלל של כל הציונים לפי המשקלות.

### שלב 4: זיהוי כשלים והמלצות

**Common GEO failures** (by score range):
- Score 1-3: "No meaningful digital presence" / "Website content not optimized for AI engines" / "Missing structured data entirely"
- Score 4-5: "Content exists but lacks structure" / "Missing reviews and authoritative source presence" / "No structured FAQ"
- Score 6-7: "Basic presence exists but no GEO strategy" / "Outdated content" / "No AI-optimized content"
- Score 8-10: Specific failures only (e.g., weak in a particular engine)

**Recommendations** — provide 1-3 specific, actionable recommendations per company **in English**. Don't give generic advice — each recommendation must be tailored to the company's specific situation. Examples:
- "Add a structured FAQ page with schema markup covering [X, Y, Z] topics"
- "Create a comprehensive guide on [X] that AI engines can quote and cite"
- "Update and expand the company's Wikipedia page with current information"
- "Increase presence on forums like Reddit and Quora in [sector] discussions"

**IMPORTANT: The failures column (K) and recommendations column (L) MUST be written entirely in English.** All other columns remain in Hebrew. This ensures clarity and avoids mixed-language formatting issues.

### שלב 5: יצירת קובץ Excel

**חובה**: השתמש ב-openpyxl ליצירת הקובץ. קרא את הוראות ה-xlsx skill לגבי formatting.

**מבנה הקובץ:**

**Sheet 1: "GEO Analysis"**

| עמודה | תוכן | רוחב מומלץ |
|--------|-------|------------|
| A | # (מספר שורה) | 5 |
| B | שם חברה | 25 |
| C | לינק לאתר (hyperlink) | 35 |
| D | ציון ChatGPT (1-10) | 14 |
| E | ציון Gemini (1-10) | 14 |
| F | ציון Google AI Overview (1-10) | 18 |
| G | ציון Claude (1-10) | 14 |
| H | ציון Grok (1-10) | 14 |
| I | ציון Google Organic (1-10) | 18 |
| J | ציון משוכלל (1-10) | 16 |
| K | Key GEO Failures | 45 |
| L | Recommendations (1-3) | 55 |

**Sheet 2: "Weights & Methodology"**
- טבלה עם המשקלות שנבחרו
- הסבר קצר על המתודולוגיה
- תאריך הניתוח
- הסקטור שנבדק

**עיצוב:**
- כותרת ראשית ממוזגת בשורה 1 עם שם הסקטור ותאריך
- שורת כותרות עמודות (שורה 3) ברקע כהה (RGB: 2B3A67) וטקסט לבן, bold
- שורות רגילות עם רקע מתחלף (לבן / אפור בהיר RGB: F2F2F2)
- ציונים עם conditional formatting צבעוני:
  - 8-10: ירוק (RGB: C6EFCE) 
  - 5-7: צהוב (RGB: FFEB9C)
  - 1-4: אדום (RGB: FFC7CE)
- הציון המשוכלל ב-bold
- עמודת הלינק כ-hyperlink כחול ולחיץ
- Freeze panes על שורת הכותרות
- Auto-filter על כל העמודות
- מיון לפי ציון משוכלל (מהגבוה לנמוך)
- כיוון LTR (אנגלית) לעמודות K ו-L
- Wrap text בעמודות K ו-L

**חשוב:** השתמש בסקריפט `scripts/generate_geo_excel.py` שנמצא בתיקיית ה-skill ליצירת הקובץ. העבר לו את הנתונים כ-JSON.

### שלב 6: הצגת התוצאות

1. שמור את הקובץ בתיקיית ה-outputs
2. הצג למשתמש סיכום קצר של הממצאים:
   - כמה חברות עם ציון גבוה (8+), בינוני (5-7), נמוך (1-4)
   - החברה עם הציון הגבוה ביותר והנמוך ביותר
   - מגמה כללית של הסקטור
3. תן לינק להורדת הקובץ

## הערות חשובות

- **דיוק**: עדיף לתת ציון שמרני ולציין שהניתוח מבוסס על מחקר אינטרנטי ולא על גישה ישירה למנועי ה-AI, מאשר לנפח ציונים
- **שפה**: הקובץ ברובו בעברית. שמות חברות יכולים להיות באנגלית אם כך הם מוכרים. **עמודת הכשלים (K) ועמודת ההמלצות (L) חייבות להיות באנגלית בלבד** — כדי למנוע בעיות פורמט של עברית ואנגלית מעורבות
- **עדכניות**: ציין את תאריך הניתוח בקובץ
- **הגבלות**: ציין בגיליון המתודולוגיה שהניתוח מבוסס על מחקר אינטרנטי וסימנים עקיפים, ולא על שאילתה ישירה לכל מנוע AI
