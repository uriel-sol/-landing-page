# יומן החלטות — Decision Log

תיעוד של כל החלטה משמעותית בפרויקט.
מנוהל על ידי architect-lead.

---

## פורמט

| תאריך | החלטה | מי החליט | נימוק |
|--------|--------|----------|-------|
| YYYY-MM-DD | תיאור ההחלטה | architect-lead / המשתמש | למה |

---

## החלטות

| תאריך | החלטה | מי החליט | נימוק |
|--------|--------|----------|-------|
| 2026-03-14 | הקמת Project Operating System — מבנה תיקיות, סוכנים, ומסמכים | המשתמש + architect-lead | ארגון הפרויקט לפני המשך עבודה על עיצוב ופיתוח |
| 2026-03-14 | architect-lead מוגדר כסוכן ראשי ומאשר סופי | המשתמש | שליטה מרכזית ומסודרת בפרויקט |
| 2026-03-14 | qa-launch מוגדר כסוכן review בלבד — ממצאים והמלצות, לא החלטות סופיות | המשתמש | הפרדה ברורה בין review לבין אישור |
| 2026-03-14 | סוכנים בשפה אנגלית, מסמכים בעברית | המשתמש | תאימות טכנית + נגישות למשתמש |
| 2026-03-14 | brand-direction.md הוא מסמך אסטרטגי, לא ניתוח של HTML קיים | המשתמש | המסמך מגדיר כיוון עתידי, לא מתעד מצב קיים |
| 2026-03-14 | החלפת קופי מלאה ב-index.html | המשתמש + architect-lead | קופי סופי נעול — שלב 1.1 הושלם |
| 2026-03-14 | קונספט ויזואלי: "חדר העבודה האסטרטגי" | המשתמש | Dark Glassmorphism, Mobile-First, High-Ticket premium feel |
| 2026-03-14 | ביטול Mouse Tracking — Mobile-First | המשתמש | כל אפקט חייב לעבוד ללא עכבר; תאורה מבוססת גלילה במקום |
| 2026-03-14 | אייקונים 3D ריאליסטיים במקום אימוג'ים | המשתמש | תואם לקונספט פרימיום; אימוג'ים בקופי הם placeholders בלבד |
| 2026-03-14 | Scrollytelling עם קווי חיווט SVG | המשתמש | משדר תהליך ומנגנון — מתאים לקונספט הבנייה |
| 2026-03-19 | הסרת authority logos מ-HTML (לא רק הסתרה) | architect-lead | בזבוז bandwidth במובייל (8 בקשות רשת), בעיות clipping בדסקטופ |
| 2026-03-19 | הוספת prefers-reduced-motion global block | architect-lead | חובת WCAG AA — דווח ע"י 3 מתוך 4 סוכנים |
| 2026-03-19 | Transform card — class-based glow (scroll-focus) במקום inline styles | architect-lead | מניעת specificity conflicts עם CSS transitions ו-hover states |
| 2026-03-19 | Steps wire — scaleX במקום width animation | architect-lead | ביצועים — width גורם ל-layout reflow בכל frame, scaleX הוא GPU-composited |
| 2026-03-19 | Consent checkbox validation ב-JS (שני הטפסים) | architect-lead | באג קריטי — HTML required attribute נעקף ע"י e.preventDefault() |
| 2026-03-19 | Navbar justify-content:space-between | architect-lead | RTL layout — center לא מתאים לדף עברי |
| 2026-03-19 | הסרת console.log מ-submitLead | architect-lead | חשף webhook URL ו-lead data — סיכון אבטחה |
| 2026-03-19 | Fallback redirect אחרי submit (לא תלוי ב-GTM) | architect-lead | אם GTM חסום ע"י ad blocker, המשתמש נתקע על "שולח..." |
| 2026-03-19 | Scroll popup guard — לא מציג כשבאנר הסכמה פתוח | architect-lead | מניעת שני דיאלוגים מתנגשים על אותו z-index |
| 2026-03-19 | GSAP scripts defer + ScrollTrigger.refresh on load | architect-lead | ביצועי FCP — scripts ב-head חוסמים parsing |
| 2026-03-19 | SVG scrollytelling — window.load במקום setTimeout(500) | architect-lead | מיקום מדויק יותר — ממתין לטעינת כל המשאבים |
| 2026-03-19 | Font-weight normalization — 760→800, 650→700 | architect-lead | תאימות cross-browser — ערכים לא סטנדרטיים לא נתמכים בכל הדפדפנים |
