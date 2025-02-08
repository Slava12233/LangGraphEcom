# WordPress AI Agent

סוכן AI המנוהל דרך בוט בטלגרם לביצוע פעולות באתר וורדפרס באמצעות פקודות בשפה טבעית.

## תכונות

- קבלת פקודות בשפה טבעית דרך טלגרם
- פירוש הפקודות באמצעות LangChain ו-OpenAI
- ביצוע פעולות באתר וורדפרס דרך REST API
- תמיכה בפעולות:
  - הורדת מבצעים ממוצרים
  - עדכון מחירי מוצרים
  - קבלת נתוני מכירות

## דרישות מערכת

- Python 3.8 ומעלה
- חשבון טלגרם ובוט (דרך BotFather)
- חשבון OpenAI עם מפתח API
- אתר וורדפרס עם WooCommerce מותקן

## התקנה

1. שכפל את המאגר:
```bash
git clone <repository-url>
cd wordpress-ai-agent
```

2. צור סביבה וירטואלית והפעל אותה:
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

3. התקן את הדרישות:
```bash
pip install -r requirements.txt
```

4. העתק את קובץ `.env.example` ל-`.env`:
```bash
cp .env.example .env
```

5. ערוך את קובץ `.env` והוסף את הפרטים הנדרשים:
- `TELEGRAM_BOT_TOKEN`: אסימון הבוט מ-BotFather
- `WP_URL`: כתובת אתר הוורדפרס שלך
- `WP_USER`: שם משתמש לוורדפרס
- `WP_PASSWORD`: סיסמת אפליקציה לוורדפרס
- `OPENAI_API_KEY`: מפתח API של OpenAI

## הפעלה

הפעל את הבוט:
```bash
python main.py
```

## שימוש

שלח הודעות לבוט בטלגרם עם פקודות בשפה טבעית, לדוגמה:
- "הורד את המבצע על מגני הטלפון"
- "כמה מכרנו מהחולצות השבוע?"
- "עדכן את המחיר של הכובעים"

הבוט יפרש את הפקודות ויבצע את הפעולות המתאימות באתר הוורדפרס.

## אבטחה

- אל תשתף את קובץ `.env` או את הפרטים הרגישים שבו
- השתמש בסיסמת אפליקציה ייעודית לוורדפרס במקום סיסמת המשתמש הראשית
- הגבל את הגישה לבוט בטלגרם למשתמשים מורשים בלבד

## רישיון

MIT License 