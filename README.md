#  GoHighLevel CRM Pipeline & Automation
### Built with GoHighLevel · CRM · Sales Pipeline · Funnel · Automation · Booking Calendar

![Status](https://img.shields.io/badge/Status-Live%20%E2%9C%85-brightgreen?style=for-the-badge)
![GoHighLevel](https://img.shields.io/badge/GoHighLevel-2E86AB?style=for-the-badge&logoColor=white)
![Pipeline](https://img.shields.io/badge/Pipeline-4%20Stages-orange?style=for-the-badge)
![Automation](https://img.shields.io/badge/Automation-4%20Steps-5C6BC0?style=for-the-badge)
![Funnel](https://img.shields.io/badge/Funnel-3%20Steps-FF4A00?style=for-the-badge)
![Calendar](https://img.shields.io/badge/Booking%20Calendar-Live-34A853?style=for-the-badge)

---

##  Project Overview

A fully functional **GoHighLevel CRM, pipeline and automation system** built for a nutrition coaching business — completed as a capstone assignment for the **GHL Automation & CRM Fundamentals** course.

The system takes a cold visitor from first landing page visit all the way through to a booked consultation and pipeline stage update — **entirely automatically**, with zero manual intervention after the form is submitted.

**8 tasks completed end-to-end:**
- ✅ **10 contacts imported** with custom tag for smart filtering
- ✅ **Smart List created** — dynamic, auto-updating filtered contact view
- ✅ **3 custom fields built** — Fitness Goal, Budget, Lead Source
- ✅ **4-stage sales pipeline** — New Lead → Contacted → Proposal Sent → Closed
- ✅ **3-step lead funnel** — Offer → Appointment → Thank You
- ✅ **Opt-in form + booking calendar** connected to pipeline
- ✅ **4-step automation workflow** — trigger → welcome email → pipeline entry → stage move
- ✅ **Live test confirmed** — form submission fired automation end-to-end

> *"A cold visitor submits a form. Within seconds: welcome email delivered, opportunity created in the CRM, lead moved to Contacted — zero manual work."*

---

##  System Architecture

```
Cold Visitor
      │
      ▼
3-Step Funnel (GloriaN Nutrition Coaching Lead Funnel)
      │
      ├──► Step 1: Offer / Landing Page (opt-in form)
      ├──► Step 2: Appointment (booking calendar)
      └──► Step 3: Thank You Page
      │
      ▼
Form Submitted → AUTOMATION TRIGGERS
      │
      ├──► Action 1: Send Welcome Email (personalised)
      ├──► Action 2: Create Opportunity in CRM Pipeline
      └──► Action 3: Move Lead to 'Contacted' Stage
      │
      ▼
Gloria_N Sales Pipeline (CRM)
      │
      ├──► Stage 1: New Lead
      ├──► Stage 2: Contacted ← auto-moved here by automation
      ├──► Stage 3: Proposal Sent
      └──► Stage 4: Closed
```

---

##  Task 1 — Contacts & CRM Setup

**10 contacts manually added** to GoHighLevel with 4 fields each:

| Field | Detail |
|---|---|
| First Name + Last Name | Full contact name |
| Email Address | Primary contact email |
| Phone Number | Nigerian format |
| Tag | `glorian` — unique identifier for filtering |

**Why the `glorian` tag?**
The sub-account is shared with 20+ classmates. The tag uniquely identifies contacts among hundreds in the shared account — enabling instant filtering and preventing confusion.

---

##  Task 2 — Smart List

**Smart List Name:** `Gloria Njorteah Leads`

A Smart List is a saved, dynamic filter in GHL that automatically updates whenever new contacts match the set criteria — no manual updates required.

| Feature | Detail |
|---|---|
| **Dynamic** | Automatically shows new contacts matching `glorian` tag |
| **Isolated** | Filters only my 10 contacts from 50+ in the shared account |
| **Reusable** | Can be used as audience for email campaigns and automations |
| **Named** | Clearly labelled for easy identification |

---

##  Task 3 — Custom Fields

**3 custom dropdown fields** created in GHL Settings → Custom Fields (Object: Contact):

### Field 1 — Gloria Njorteah_Fitness Goal
**Type:** Dropdown
**Options:** Weight Loss · Muscle Gain · General Fitness · Marathon Training · Nutrition
**Purpose:** Segments leads by health objective for targeted follow-up messaging

### Field 2 — Gloria N_Monthly Budget
**Type:** Dropdown
**Options:** Under £100 · £100–£200 · £200–£400 · £400+
**Purpose:** Qualifies leads by investment level — prioritises high-value prospects

### Field 3 — Gloria N_How Did You Hear About Us
**Type:** Dropdown
**Options:** Instagram · Facebook · Google · Referral · Other
**Purpose:** Tracks marketing channel ROI to identify best-performing lead sources

---

##  Task 4 — Sales Pipeline

**Pipeline Name:** `Gloria_N Sales Pipeline`

A 4-stage pipeline tracking the full lead journey from opt-in to closed client:

| Stage | # | Trigger | What Happens |
|---|---|---|---|
| 🆕 **New Lead** | 1 | Lead submits form | Enters CRM automatically |
| 📞 **Contacted** | 2 | Automation fires | Welcome email sent, stage auto-updated |
| 📄 **Proposal Sent** | 3 | Manual or automated | Pricing or offer shared with lead |
| 🏆 **Closed** | 4 | Deal agreed | Lead converts to paying client |

> Leads automatically move from **New Lead → Contacted** via the automation workflow — no manual stage updates needed.

---

##  Task 5 — 3-Step Lead Funnel

**Funnel Name:** `GloriaN_Nutrition Coaching Lead Funnel`
Built using a prebuilt template — customised for nutrition coaching.

| Step | Page Type | Purpose | Contains |
|---|---|---|---|
| **Step 1** | Offer / Landing Page | Captures lead's interest | Nutrition offer + opt-in form |
| **Step 2** | Appointment | Directs lead to book | 30-min free consultation calendar |
| **Step 3** | Thank You | Confirms submission | Next steps + expectation setting |

> This proven 3-step funnel converts a cold visitor into a booked consultation **automatically**.

---

##  Task 6 — Form & Booking Calendar

### 6a — Opt-in Form
**Form Name:** `GloriaN Nutrition Coaching — Free Consultation Form`

| Field | Type |
|---|---|
| First Name | Text |
| Last Name | Text |
| Phone | Phone (required) |
| Email | Email (required) |
| How Did You Hear About Us | Custom dropdown |
| Fitness Goal | Custom dropdown |

**Form URL:** `api.leadconnectorhq.com/widget/form/9zjI9...`

---

### 6b — Booking Calendar
**Calendar Name:** `Gloria_N Nutrition Consultation`

| Setting | Value |
|---|---|
| Type | Personal Booking |
| Host | Gloria Njorteah |
| Duration | 30 Minutes |
| Availability | Weekdays 8:00 AM – 5:00 PM |
| Timezone | Europe/London (GMT) |

**Booking URL:** `api.leadconnectorhq.com/widget/bookings/glorian-nutrition-consultation`

---

##  Task 7 — Automation Workflow

**Workflow Name:** `Gloria_N Welcome Automation`
**Trigger:** Gloria_N Registration Form Submitted

```
TRIGGER: Form Submitted
      │
      ▼
ACTION 1: Send Welcome Email
Personalised with {{contact.first_name}}, next steps
and calendar booking link — fires instantly
      │
      ▼
ACTION 2: Add to Pipeline
Creates opportunity in Gloria_N Sales Pipeline
at 'New Lead' stage automatically
      │
      ▼
ACTION 3: Move to Contacted
Updates opportunity stage to 'Contacted'
proving automatic pipeline progression
```

---

## ✅ Task 8 — Live Test Results

**Test:** Submitted the GloriaN Nutrition Coaching Registration Form

| Outcome | Result |
|---|---|
| Form submission triggered workflow | ✅ Fired instantly |
| Welcome email delivered to lead's inbox | ✅ Delivered immediately |
| Opportunity created in Gloria_N Sales Pipeline | ✅ Created at New Lead stage |
| Lead moved to Contacted stage automatically | ✅ No manual action needed |

**Pipeline state after test:**

| New Lead | Contacted | Proposal Sent | Closed |
|---|---|---|---|
| 0 | 1 ✅ | 0 | 0 |

> The lead appeared in **Contacted** automatically — proof the end-to-end automation works correctly.

---

##  Assignment Summary

| Task | Deliverable | Status |
|---|---|---|
| Task 1 | 10 contacts added with `glorian` tag | ✅ |
| Task 2 | Smart List — `Gloria Njorteah Leads` | ✅ |
| Task 3 | 3 custom dropdown fields | ✅ |
| Task 4 | 4-stage sales pipeline | ✅ |
| Task 5 | 3-step nutrition coaching funnel | ✅ |
| Task 6 | Opt-in form + 30-min booking calendar | ✅ |
| Task 7 | 4-step automation workflow | ✅ |
| Task 8 | Live test — automation confirmed | ✅ |

---

##  Business Impact

| Area | Manual Process | After GHL Automation |
|---|---|---|
| Lead capture | Manual form collection | Auto-captured via funnel form |
| CRM entry | Manual contact creation | Auto-added to pipeline |
| Welcome communication | Staff sends manually | Personalised email fires instantly |
| Pipeline stage tracking | Manual drag-and-drop | Auto-moved by workflow |
| Appointment booking | Phone/email back-and-forth | Self-serve 30-min calendar |
| Lead segmentation | Impossible at scale | Smart Lists + custom fields |
| Marketing ROI tracking | Unknown | Source field tracks every lead |

---

##  Tech Stack

| Tool | Role |
|---|---|
| **GoHighLevel (GHL)** | All-in-one CRM, automation and funnel platform |
| **GHL Contacts** | Lead database with custom fields and tags |
| **GHL Smart Lists** | Dynamic filtered contact views |
| **GHL Pipeline** | Visual sales pipeline — 4 stages |
| **GHL Funnel Builder** | 3-step lead capture funnel |
| **GHL Forms** | Opt-in form with custom fields |
| **GHL Calendar** | 30-min personal booking widget |
| **GHL Workflows** | 4-step automation — trigger → email → pipeline → stage |

---

##  Repository Contents

```
ghl-crm-pipeline-automation/
│
├── docs/
│   └── Gloria_Njorteah_GHL_Assignment.pptx   # Full assignment presentation
│
├── screenshots/
│   ├── contacts_smart_list.png
│   ├── custom_fields.png
│   ├── sales_pipeline.png
│   ├── funnel_steps.png
│   ├── form_calendar.png
│   ├── automation_workflow.png
│   └── live_test_result.png
│
└── README.md
```

---

##  Future Improvements

| Feature | Description |
|---|---|
| 💳 Payment Integration | Add Stripe checkout step after Proposal Sent stage |
| 📱 SMS Automation | Send SMS follow-up after welcome email |
| 🔄 Re-engagement Sequence | Automated email sequence for leads stuck in Proposal Sent |
| 📊 Reporting Dashboard | GHL reporting for pipeline conversion rates |
| 🤖 AI Appointment Bot | Use GHL AI to handle booking rescheduling |
| 🌍 Multi-location Calendar | Add multiple coaching locations/timezones |

---

##  About the Builder

**Gloria Njorteah** — Strategic Business Analyst & AI Automation Specialist

This project was completed as a capstone assignment for the **GHL Automation & CRM Fundamentals** course — demonstrating end-to-end CRM setup, funnel building, form and calendar creation, and fully automated lead capture and pipeline management in GoHighLevel.

- 🌍 [LinkedIn](https://www.linkedin.com/in/gloria-njorteah)
- 💼 [Upwork](https://www.upwork.com/freelancers/gloinnovate)
- 🐙 [GitHub](https://github.com/Glorious75)

> *Available to build GoHighLevel CRM systems, automation workflows and lead funnels for your business. Let's talk.*

---

*Built with 🚀 using GoHighLevel | GHL Automation & CRM Fundamentals · March 2026*
