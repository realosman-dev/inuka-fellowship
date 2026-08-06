# Week 9 Video Walkthrough — Script & Storyboard
### For recording `Week9_Video_[YourName].mp4` (~3 minutes)

> **Note:** I can't record or export an actual screen-capture video file for
> you — that needs your own screen and voice. Below is a tight script and
> shot list so you can record it in one take using the notebook's outputs.
> Suggested tools: Zoom/Loom/QuickTime/OBS screen recording, 3 minutes.

---

## Shot list (what to have on screen, in order)

1. Section 4 output — Confusion Matrix + ROC curve (Random Forest)
2. Section 6 output — SHAP summary plot
3. Section 6 output — SHAP force/waterfall plot for the single flagged machine
4. (Optional close) Feature importance bar chart

---

## Narration script

**[0:00–0:30] Open — the problem, plainly**

> "Hi, I'm [Your Name]. This is a walkthrough of the equipment failure
> prediction model I built for Week 9. The goal is simple: instead of
> waiting for a machine to break, flag it a few days early so maintenance
> can get ahead of it. I trained two models — Random Forest and XGBoost —
> on sensor data like vibration, temperature, and operating hours."

**[0:30–1:10] Show the confusion matrix / ROC — be honest about tradeoffs**

> "Here's how the model actually performs. [point to confusion matrix]
> Accuracy alone would be misleading here, because failures are rare —
> under 12% of machines. So I focused on recall: of the machines that
> really did fail, how many did we catch? And ROC-AUC, which tells us how
> well the model ranks risky machines above healthy ones regardless of
> where we set the alert threshold."

**[1:10–2:00] SHAP summary — the global view**

> "This is a SHAP summary plot — it's the model's explanation for *all*
> machines at once. Each dot is one machine. Red means a high sensor
> reading, blue means a low one, and position left-to-right shows whether
> that reading pushed the prediction toward 'failure' or 'no failure'.
> You can see vibration at the top — high vibration, shown in red, sits
> almost entirely on the failure side. That matches what maintenance
> teams already know: vibration is usually the earliest warning sign."

**[2:00–2:45] SHAP force/waterfall — one specific case**

> "Now let's zoom into one machine — this is the highest-risk case in my
> test set. Here is a case the model flagged as **High Risk**. You can
> see here that **vibration was the main driver** — it's the longest bar
> pushing the prediction toward failure — with operating hours adding to
> that risk too. This is exactly the kind of explanation I'd hand a
> technician: not just 'this machine is risky,' but 'here's specifically
> why.'"

**[2:45–3:00] Close — trust and limits**

> "One last thing: this is a decision-support tool, not a decision-maker.
> It's going to have false alarms, and it will occasionally miss one — no
> model on data this imbalanced is perfect. It's built to flag the
> machines worth a technician's attention first, not to replace their
> judgment on the floor. Thanks for watching."

---

## Delivery notes
- Keep tone confident and plain-spoken — avoid reading jargon straight off
  the plots; translate it as you go (as scripted above).
- Practice once without recording so the SHAP-plot section flows in under
  a minute.
- Trim silence at the start/end before exporting as `.mp4`.
