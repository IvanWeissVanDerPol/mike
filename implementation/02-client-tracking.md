# 📊 CLIENT TRACKING SYSTEM - COMPLETE TEMPLATE

**Purpose:** Track every client, session, payment, and referral  
**How to Use:** Copy this into Excel, Google Sheets, or Notion  
**Update Frequency:** After EVERY session (same day)

---

## 📋 SPREADSHEET STRUCTURE

### **SHEET 1: CLIENT MASTER LIST**

Copy this table structure into Excel/Google Sheets:

| Column A | Column B | Column C | Column D | Column E | Column F | Column G | Column H | Column I |
|----------|----------|----------|----------|----------|----------|----------|----------|----------|
| **Client ID** | **Name** | **Tier** | **Phone** | **Source** | **First Contact** | **First Session** | **Total Sessions** | **Status** |
| C001 | Ana García | 1 (VIP) | 0981-XXX-XXX | Direct friend | 2026-01-20 | 2026-01-25 | 3 | Active |
| C002 | Luis Ramírez | 2 (Friend) | 0985-XXX-XXX | Direct friend | 2026-01-21 | 2026-01-28 | 1 | Active |
| C003 | María López | 3 (Referral) | 0971-XXX-XXX | Referred by Ana | 2026-01-25 | 2026-02-02 | 2 | Active |

**Column Definitions:**

- **Client ID:** Unique identifier (C001, C002, etc.)
- **Name:** First and last name
- **Tier:** 1 = VIP Friend (Gs. 60K), 2 = Good Friend (Gs. 80K), 3 = Referral (Gs. 100K)
- **Phone:** WhatsApp number
- **Source:** How did you meet? (Direct friend, Referred by X, Family, etc.)
- **First Contact:** Date you first messaged them
- **First Session:** Date of their first massage
- **Total Sessions:** Running count (update after each session)
- **Status:** Active, Paused, Inactive, Waiting List

---

### **SHEET 2: SESSION LOG (Transaction History)**

| Column A | Column B | Column C | Column D | Column E | Column F | Column G | Column H | Column I |
|----------|----------|----------|----------|----------|----------|----------|----------|----------|
| **Session ID** | **Date** | **Client ID** | **Client Name** | **Service** | **Duration** | **Price** | **Paid?** | **Notes** |
| S001 | 2026-01-25 | C001 | Ana García | Massage + Gun | 60 min | Gs. 60,000 | ✅ Cash | Lower back tension, worked glutes + hamstrings |
| S002 | 2026-01-27 | C002 | Luis Ramírez | Massage only | 45 min | Gs. 80,000 | ✅ Cash | Neck/shoulder tension, office worker |
| S003 | 2026-01-28 | C001 | Ana García | Stretching focus | 50 min | Gs. 60,000 | ✅ Cash | Pre-running session, hip flexors |

**Column Definitions:**

- **Session ID:** Unique identifier (S001, S002, etc.)
- **Date:** When session happened
- **Client ID:** Links to Client Master List
- **Client Name:** For easy reference
- **Service:** What you did (Massage + Gun, Stretching, Relaxation, etc.)
- **Duration:** How long (plan 45-60 min, track actual)
- **Price:** What you charged
- **Paid?:** ✅ Cash, ✅ Transfer, ⏳ Pending, ❌ Unpaid
- **Notes:** What you worked on, client feedback, anything to remember

---

### **SHEET 3: INCOME TRACKER (Weekly Summary)**

| Week | Dates | Sessions | Gross Income | Costs | Net Income | Cumulative |
|------|-------|----------|--------------|-------|------------|------------|
| Week 1 | Jan 20-26 | 3 | Gs. 200,000 | Gs. 420,000* | -Gs. 220,000 | -Gs. 220,000 |
| Week 2 | Jan 27-Feb 2 | 4 | Gs. 280,000 | Gs. 30,000 | Gs. 250,000 | Gs. 30,000 |
| Week 3 | Feb 3-9 | 5 | Gs. 380,000 | Gs. 40,000 | Gs. 340,000 | Gs. 370,000 |
| Week 4 | Feb 10-16 | 6 | Gs. 480,000 | Gs. 50,000 | Gs. 430,000 | Gs. 800,000 |

*Week 1 includes initial investment (Gs. 390K-520K)

**How to Fill:**
- Count sessions from Session Log
- Sum all prices from Session Log
- Add costs: oils, towels, Uber if applicable
- Calculate: Net = Gross - Costs
- Track cumulative savings

---

### **SHEET 4: EXPENSE TRACKER**

| Date | Category | Item | Quantity | Cost | Supplier | Notes |
|------|----------|------|----------|------|----------|-------|
| 2026-01-20 | Oils | Coconut oil 1L | 3 bottles | Gs. 375,000 | Casa Grütter | Bulk purchase |
| 2026-01-20 | Linens | Bath towels | 8 | Gs. 100,000 | Casa Nissei | White, cotton |
| 2026-01-20 | Hygiene | Hand sanitizer 1L | 1 | Gs. 20,000 | Farmacenter | |
| 2026-01-20 | Equipment | Carrying bag | 1 | Gs. 50,000 | Fortis | Black duffel |
| 2026-02-15 | Oils | Coconut oil 1L | 2 | Gs. 250,000 | Casa Grütter | Monthly refill |

**Categories:**
- **Oils:** All massage oils
- **Linens:** Towels, sheets, pillow covers
- **Hygiene:** Sanitizer, wipes, cleaning supplies
- **Equipment:** Bags, upgrades, massage gun accessories
- **Transport:** Uber costs (if charging client separately, don't include)
- **Marketing:** Business cards, printing (later, if needed)
- **Other:** Anything else

---

### **SHEET 5: REFERRAL TRACKER**

| Referrer ID | Referrer Name | Referred ID | Referred Name | Status | Conversion Date | Bonus Given? |
|-------------|---------------|-------------|---------------|--------|-----------------|--------------|
| C001 | Ana García | C003 | María López | Converted | 2026-02-02 | ✅ Free 15 min |
| C001 | Ana García | C007 | Pedro Silva | Pending | - | - |
| C005 | Carlos Méndez | C008 | Sofía Torres | Converted | 2026-02-10 | ✅ 20% off next |

**Why Track This?**
- Reward your best referrers (free 15 min upgrade, discount, etc.)
- See which clients bring the most business
- Build your network systematically

**Conversion = Referred person booked and completed first session**

---

### **SHEET 6: AVAILABILITY CALENDAR**

**Purpose:** Block out when you're available vs. booked

Create a simple weekly view:

| Time Slot | Monday | Tuesday | Wednesday | Thursday | Friday | Saturday | Sunday |
|-----------|--------|---------|-----------|----------|--------|----------|--------|
| 8:00-9:30 | AVAILABLE | AVAILABLE | AVAILABLE | AVAILABLE | AVAILABLE | AVAILABLE | AVAILABLE |
| 10:00-11:30 | AVAILABLE | **BOOKED: Ana** | AVAILABLE | AVAILABLE | **BOOKED: Luis** | AVAILABLE | AVAILABLE |
| 14:00-15:30 | AVAILABLE | AVAILABLE | **BOOKED: María** | AVAILABLE | AVAILABLE | AVAILABLE | AVAILABLE |
| 16:00-17:30 | AVAILABLE | AVAILABLE | AVAILABLE | **BOOKED: Pedro** | AVAILABLE | AVAILABLE | AVAILABLE |
| 18:00-19:30 | AVAILABLE | AVAILABLE | AVAILABLE | AVAILABLE | AVAILABLE | AVAILABLE | AVAILABLE |

**How to Use:**
1. Mark your UNAVAILABLE times (classes, personal commitments)
2. When client books, change AVAILABLE → **BOOKED: [Name]**
3. Update weekly
4. Never double-book!

---

## 📱 SIMPLIFIED VERSION (If You Don't Like Spreadsheets)

### **OPTION: Use a Notebook**

**Page 1: Client List**
```
VIP FRIENDS (Gs. 60K):
[ ] Ana García - 0981-XXX - Sessions: 3
[ ] Luis Ramírez - 0985-XXX - Sessions: 1

GOOD FRIENDS (Gs. 80K):
[ ] Carlos Méndez - 0971-XXX - Sessions: 2

REFERRALS (Gs. 100K):
[ ] María López (Ana's friend) - Sessions: 1
```

**Page 2: Weekly Income**
```
WEEK 1 (Jan 20-26):
- Mon: -
- Tue: -
- Wed: Ana (Gs. 60K) ✅
- Thu: Luis (Gs. 80K) ✅
- Fri: Ana (Gs. 60K) ✅
- Sat: -
- Sun: -
TOTAL: Gs. 200K (3 sessions)
```

**Page 3: Expenses**
```
Jan 20: Oils Gs. 375K, Towels Gs. 100K, Hygiene Gs. 20K, Bag Gs. 50K
TOTAL STARTUP: Gs. 545K

Feb 15: Refill oils Gs. 250K
```

---

## 🎯 KEY METRICS TO TRACK

### **Daily:**
- [ ] Sessions completed today
- [ ] Cash collected today
- [ ] Next day's bookings confirmed

### **Weekly:**
- [ ] Total sessions this week
- [ ] Total income this week
- [ ] Average price per session
- [ ] How many new clients this week?
- [ ] How many repeat clients?

### **Monthly:**
- [ ] Total sessions this month
- [ ] Total income this month
- [ ] Total expenses this month
- [ ] Net profit this month
- [ ] Cumulative savings to date
- [ ] Client retention rate (% of clients who booked 2+ times)
- [ ] Average sessions per client

---

## 📊 SAMPLE ANALYSIS (After Month 1)

**Data:**
- Total sessions: 16
- Total income: Gs. 1,120,000
- Total expenses: Gs. 600,000 (includes startup)
- Net profit: Gs. 520,000
- Unique clients: 12
- Repeat clients: 4 (33% retention)

**Insights:**
- ✅ Average Gs. 70K per session (between Tier 1 and Tier 2 pricing)
- ✅ 4 sessions/week average (on track for Month 2 goal of 5/week)
- ⚠️ 33% retention is low - need to follow up with clients after first session
- 💡 Action: Send "How are you feeling?" message 3-5 days after session

---

## 🚨 CRITICAL: PROTECT THIS DATA

**Privacy Rules:**
- ✅ Keep spreadsheet password-protected (if digital)
- ✅ Never share client names/numbers publicly
- ✅ If someone asks "Who are your clients?" → "I can't share that, it's confidential"
- ✅ Delete WhatsApp chat history after booking (or archive)
- ❌ Don't post client testimonials with names (unless they explicitly agree)
- ❌ Don't show this spreadsheet to anyone except maybe family

**Why?** 
- Professional confidentiality (even as a student)
- Legal protection (no paper trail of "physiotherapy business")
- Client trust (they're helping you, respect their privacy)

---

## ✅ SETUP CHECKLIST

**Choose Your Tool:**
- [ ] Google Sheets (free, accessible anywhere) ← **RECOMMENDED**
- [ ] Microsoft Excel (if you have it)
- [ ] Notion (if you like apps)
- [ ] Paper notebook (if you prefer analog)

**Create Your Sheets:**
- [ ] Sheet 1: Client Master List
- [ ] Sheet 2: Session Log
- [ ] Sheet 3: Income Tracker
- [ ] Sheet 4: Expense Tracker
- [ ] Sheet 5: Referral Tracker (optional)
- [ ] Sheet 6: Availability Calendar (optional)

**Add First Entries:**
- [ ] Add your 20 friends to Client Master List (even before they book)
- [ ] Log your startup expenses in Expense Tracker
- [ ] Set up Week 1 in Income Tracker

---

## 📈 GROWTH MILESTONES TO TRACK

Mark these achievements as you hit them:

- [ ] **First session completed!** (Celebrate!)
- [ ] **First Gs. 100,000 earned** (cumulative)
- [ ] **First repeat client** (someone books session #2)
- [ ] **First referral** (someone's friend books)
- [ ] **10 sessions completed** (You're getting experienced!)
- [ ] **First Gs. 500,000 earned**
- [ ] **First Gs. 1,000,000 earned** (Millionaire!)
- [ ] **20 sessions completed**
- [ ] **50 sessions completed** (Expert-level practice)
- [ ] **First Gs. 5,000,000 saved** (20% toward post-license launch!)

---

**🎯 NEXT STEPS:**

1. **Today:** Set up your tracking system (Google Sheets or notebook)
2. **Day 3:** Add your 20 friends to Client Master List
3. **After shopping:** Log expenses in Expense Tracker
4. **After first session:** Log in Session Log + update Income Tracker
5. **Every Sunday:** Review weekly totals and plan next week

---

**Next file:** `03-session-guide.md` → Learn exactly what to do during each massage session
