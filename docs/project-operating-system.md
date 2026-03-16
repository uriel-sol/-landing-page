# מערכת הפעלה לפרויקט — Project Operating System

## חזון הפרויקט

דף נחיתה עבור "קוד המפצח" של אוריאל סול — תוכנית 13 שבועות לבעלי עסקים ומומחים שרוצים לבנות מנגנון ביקוש יציב.

המטרה: דף נחיתה מקצועי, ממיר, ומדויק שמשקף את הערך של התוכנית ומניע לפעולה.

---

## Source of Truth — מקור האמת

### מצב נוכחי
ה-source of truth עדיין לא הוגדר. הקובץ `landing-page (4).html` הוא קובץ ישן ואינו סמכותי.

### ברגע שהמשתמש יוסיף את הקובץ האחרון:
- הקובץ החדש (צפוי: `index.html`) הופך למקור האמת היחיד
- `landing-page (4).html` הוא קובץ legacy מיושן — **אסור לערוך, להפנות אליו, או להשתמש בו**
- אם `landing-page (4).html` עדיין קיים אחרי הוספת `index.html`, יש להמליץ למשתמש למחוק אותו
- רק architect-lead רשאי להציע שינויים לקובץ מקור האמת

---

## היררכיית סוכנים

```
המשתמש (אוריאל)
  └── architect-lead (סוכן ראשי + מאשר סופי)
        ├── visual-director (כיוון ויזואלי ועיצובי)
        ├── frontend-builder (מימוש טכני)
        ├── motion-designer (אנימציות ותנועה)
        └── qa-launch (ביקורת, QA, מוכנות להשקה)
```

### עקרונות מפתח

1. **architect-lead הוא הממשק היחיד מול המשתמש** — אף סוכן אחר לא פונה ישירות למשתמש
2. **architect-lead הוא המאשר הסופי** — כל output משמעותי חייב לעבור את אישורו
3. **architect-lead פותר קונפליקטים** — כשסוכנים חלוקים, architect-lead מכריע
4. **qa-launch מחזיר ממצאים והמלצות בלבד** — לא מקבל החלטות סופיות

---

## זרימת קבלת החלטות

```
המשתמש מעביר בקשה
    ↓
architect-lead מנתח את הבקשה
    ↓
architect-lead מאציל לסוכן/ים המתאימים
    ↓
סוכן/ים מבצעים ומחזירים תוצאות
    ↓
architect-lead בודק ומאשר / מבקש תיקונים
    ↓
architect-lead מציג למשתמש
    ↓
המשתמש מאשר / מבקש שינויים
```

---

## שלבי עבודה

### Phase 1: Planning (תכנון)
- הגדרת מטרות ודרישות
- architect-lead מתכנן את הגישה
- סוכן פעיל: architect-lead

### Phase 2: Design (עיצוב)
- כיוון ויזואלי, brand, layout
- סוכנים פעילים: visual-director, architect-lead

### Phase 3: Build (פיתוח)
- מימוש HTML/CSS/JS
- סוכנים פעילים: frontend-builder, motion-designer, architect-lead

### Phase 4: QA (בדיקות)
- בדיקות איכות, ביצועים, נגישות
- סוכנים פעילים: qa-launch, architect-lead

### Phase 5: Launch (השקה)
- בדיקת מוכנות סופית, אנליטיקס, העלאה
- סוכנים פעילים: qa-launch, architect-lead

---

## כללי עבודה

1. **לא לגעת בדף ללא אישור architect-lead**
2. **כל החלטת עיצוב עוברת דרך visual-director → architect-lead**
3. **כל החלטה טכנית עוברת דרך frontend-builder → architect-lead**
4. **ממצאי QA הם המלצות בלבד — architect-lead מחליט על הפעולה**
5. **שינויי brand דורשים אישור המשתמש**
6. **כל החלטה משמעותית מתועדת ב-decision-log.md**
7. **אין לבצע commit או push ללא אישור מפורש מהמשתמש**

---

## Handoff Protocol — פרוטוקול העברת עבודה

### מ-architect-lead לסוכן:
- Brief ברור עם הקשר, מגבלות, ופורמט output צפוי
- הגדרת checkpoint לבדיקה

### מסוכן ל-architect-lead:
- תוצר מוגמר + תיעוד החלטות טכניות
- דגלים על בעיות או חסמים

### מ-architect-lead למשתמש:
- תוצר מאושר + הסבר קצר
- שאלות שדורשות החלטת המשתמש

---

## מסמכי הפרויקט

| מסמך | תיאור |
|------|--------|
| `project-operating-system.md` | מסמך זה — מערכת ההפעלה |
| `agent-contracts.md` | חוזים ואחריות של כל סוכן |
| `brand-direction.md` | כיוון מותגי ואסטרטגי |
| `launch-checklist.md` | צ'קליסט להשקה |
| `decision-log.md` | יומן החלטות |
