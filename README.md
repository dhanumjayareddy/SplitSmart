# SplitSmart README and PRD

## Product overview

SplitSmart is a mobile-first expense-sharing app prototype inspired by Splitwise, extended with a behavioral finance layer. The product adds late-payment interest for users who do not pay on time, rewards users who pay before the due date, credits value into an in-app wallet, and runs a points-based loyalty system designed to improve repayment behavior and retention.

The current prototype is delivered as a single interactive HTML mobile app with five major screens: Home, Groups, Add Expense, Rewards, and Profile. It demonstrates end-to-end UX flows for shared expenses, wallet top-up, reward redemption, notification handling, dark mode, and detailed payment breakdowns.

[cite:1]

## Prototype scope

The prototype covers:

- A realistic mobile UI shell with iPhone-style framing.
- Full visual workflow for a user managing shared bills.
- Late payment penalty communication.
- Early payment incentive communication.
- Wallet balance management.
- Reward points earning and redemption.
- Modal-driven detail and action flows.
- Notification and profile-based settings experiences.

This prototype is optimized for product validation, UX review, stakeholder presentations, and front-end concept testing rather than production financial settlement.

[cite:1]

## Core value proposition

SplitSmart is built around a simple shift from passive bill tracking to active payment behavior design.

### Primary differentiators

- **Penalty engine:** Bills can accrue interest after a due date and grace period.
- **Reward engine:** Early payments generate bonus points and cashback.
- **Wallet loop:** Users can add funds and use wallet balance to reduce payment friction.
- **Behavior score:** The app visualizes payment discipline through points, streaks, and a behavior score.
- **Gamified accountability:** Notifications, badges, and redemption incentives encourage timely settlement.

## Feature inventory

### 1. Home dashboard

The Home screen is the operational summary screen for the user.

#### Included elements

- App header with logo and notification/search actions.
- Wallet card with current balance.
- Total SmartPoints indicator.
- Quick actions for adding and withdrawing funds.
- Summary cards for:
  - Total amount the user owes.
  - Total amount owed to the user.
  - Total interest currently due.
- Interest alert banner showing overdue payments and accrued charges.
- Early payment reward banner showing points and cashback opportunities.
- Recent expense list with payment state badges.

#### UX purpose

This screen gives immediate awareness of risk, opportunity, and cash position. The user should be able to identify what needs payment now, what is earning rewards, and how wallet funds or points can help.

[cite:1]

### 2. Groups screen

The Groups screen organizes shared relationships by context.

#### Included elements

- List of active groups.
- Net balance per group.
- Member count.
- Group-type visual identity through emoji/icon tiles.
- Status badges such as overdue, pending, settled, and paid early.
- Entry point for creating a new group.

#### UX purpose

This screen reduces cognitive load by clustering expenses under contexts like roommates, trips, gaming, or office meals. It helps users understand financial exposure at the group level instead of only per transaction.

[cite:1]

### 3. Add Expense flow

The Add Expense screen is the main data-entry workflow.

#### Included elements

- Amount input.
- Description field.
- Category selector.
- Due-date picker.
- Friend selection chips.
- Split mode selector:
  - Equal split.
  - Custom split.
  - Percentage-based split.
- Real-time expense summary preview.
- Visible rule reminders for late interest and early bonus logic.

#### UX purpose

The flow is designed to keep the rules visible at the moment of creation. This is important because penalties and rewards only feel fair if they are transparent before users commit to an expense.

[cite:1]

### 4. Rewards screen

The Rewards screen explains and operationalizes the loyalty system.

#### Included elements

- SmartPoints balance card.
- Estimated redeemable value.
- Tier label and progress bar.
- Rate cards for:
  - Late interest.
  - Early-pay bonus points.
  - Cashback rate.
  - Grace period.
- “How to earn” explainer list.
- Reward redemption marketplace.

#### UX purpose

This screen transforms repayment discipline into a visible benefit structure. It makes the incentive system concrete rather than abstract.

[cite:1]

### 5. Profile and settings

The Profile screen stores identity, status, behavior metrics, and controls.

#### Included elements

- User avatar and profile summary.
- Expense count.
- Total points.
- Payment streak.
- Payment behavior score.
- Settings list for notifications, interest rules, rewards, and security.
- Toggles for:
  - Auto-pay from wallet.
  - Interest alerts.
  - Early-pay reminders.
- Dark mode toggle.

#### UX purpose

The Profile area lets the product feel personal and configurable. It also introduces trust and control, which are important when financial penalties are involved.

[cite:1]

### 6. Modals and micro-interactions

The prototype also includes supporting interactions that shape the feel of the product.

#### Included elements

- Bottom-sheet modals for expense detail, notifications, wallet top-up, group creation, and group detail.
- Toast notifications after user actions.
- Confetti celebration for deposits and reward redemption.
- Dynamic icon rendering.
- Visual state changes for buttons, chips, and tabs.

#### UX purpose

These interactions create a polished, app-like experience and help users understand cause and effect after each action.

[cite:1]

## Rules engine in the prototype

The prototype communicates the following financial behavior rules.

| Rule area | Current prototype rule |
|---|---|
| Late-payment interest | 1.5% per day after due date |
| Grace period | 3 days |
| Early payment reward | +10 points per ₹100 paid early |
| Early payment cashback | 2% cashback |
| Wallet top-up reward | +5 points per ₹100 added |
| Redemption examples | Wallet credit, premium, travel voucher, movie ticket |

[cite:1]

## User flows

## Primary user flow

### Flow 1: User lands on Home and reviews status

1. User opens the app.
2. User sees wallet balance, points, amount owed, amount receivable, and interest due.
3. User notices one or more alert banners:
   - overdue interest alert,
   - early payment bonus opportunity.
4. User taps a recent expense to inspect details.

**Outcome:** The user quickly understands financial priorities.

[cite:1]

### Flow 2: User adds a new shared expense

1. User taps the floating add button.
2. User enters amount and description.
3. User selects category and due date.
4. User picks friends involved in the split.
5. User chooses split type.
6. User reviews the live summary preview.
7. User confirms the expense.
8. The app shows a success toast and returns the user to the main dashboard.

**Outcome:** A new payable item is created with transparent future rules.

[cite:1]

### Flow 3: User adds money to wallet

1. User taps “Add” on the wallet card.
2. A bottom sheet opens.
3. User selects or types an amount.
4. User sees the point reward logic before confirmation.
5. User confirms.
6. Wallet balance updates.
7. SmartPoints increase.
8. Confetti and a reward toast reinforce the action.

**Outcome:** The app encourages wallet preload behavior that can support later payments.

[cite:1]

### Flow 4: User checks overdue expense details

1. User taps an overdue expense from the feed.
2. Bottom-sheet detail opens.
3. User sees:
   - original amount,
   - days overdue,
   - interest rate,
   - accrued interest,
   - current total due.
4. User can send a reminder.
5. User closes the detail sheet.

**Outcome:** The overdue state is explicit and actionable.

[cite:1]

### Flow 5: User redeems rewards

1. User goes to Rewards.
2. User reviews current point balance and tier progress.
3. User selects a redeemable item.
4. If the point balance is sufficient, redemption succeeds.
5. Points decrement.
6. Reward state updates and visual celebration occurs.

**Outcome:** The incentive loop closes and points become meaningful.

[cite:1]

### Flow 6: User configures repayment behavior settings

1. User navigates to Profile.
2. User reviews behavior score and payment streak.
3. User changes toggles like auto-pay or interest alerts.
4. User uses dark mode if preferred.

**Outcome:** The experience becomes personalized and more trustworthy.

[cite:1]

## Detailed PRD

## Product Requirements Document

### Product name

SplitSmart

### Product type

Mobile-first expense sharing and repayment behavior app.

### Problem statement

Traditional expense-sharing apps help record who owes whom, but they often do little to motivate on-time repayment. As a result, users still need reminders, emotional follow-up, and manual reconciliation. SplitSmart addresses this by combining debt visibility with interest penalties, early payment rewards, wallet liquidity, and behavioral gamification.

### Product vision

Make group expense settlement faster, fairer, and more rewarding by aligning user behavior with clear financial incentives.

### Goal

Reduce late repayments and increase repayment completion by introducing transparent financial consequences and meaningful user rewards.

### Target users

- Students and roommates sharing rent and utility expenses.
- Friends splitting travel, dining, and entertainment costs.
- Small informal groups that need lightweight settlement discipline.
- Users who are comfortable with fintech-style wallets and reward systems.

### User personas

#### Persona 1: The organizer

This user typically pays first, tracks who owes them, and gets frustrated by repeated follow-ups. They value transparency, reminders, and consequences for late payers.

#### Persona 2: The disciplined payer

This user likes to settle quickly and would respond positively to cashback, points, and streaks.

#### Persona 3: The forgetful friend

This user does not intend to delay but benefits from reminders, clear due dates, and visible increasing cost.

### Success metrics

#### Behavioral metrics

- Percent of expenses settled before due date.
- Percent of expenses settled during grace period.
- Average days overdue.
- Number of reminder actions triggered.
- Share of users maintaining an on-time streak.

#### Engagement metrics

- Daily active users.
- Wallet top-up frequency.
- Reward redemption rate.
- Notification click-through rate.
- Repeat expense creation rate.

#### Financial metrics

- Total wallet volume added.
- Cashback granted.
- Points issued.
- Points redeemed.
- Effective reduction in unpaid balances.

### Functional requirements

#### FR1. Authentication and identity

- User can have a personal profile.
- User has a display name, avatar, and account identity.
- Future production version should support phone/email sign-in.

#### FR2. Expense creation

- User can create an expense with amount, description, category, due date, and participants.
- User can choose a split type.
- System displays late-payment and early-payment rule visibility before submission.

#### FR3. Balance computation

- System computes what the user owes and what others owe the user.
- System aggregates this at user level and group level.

#### FR4. Interest engine

- System supports a configurable grace period.
- System applies a daily interest rate after grace period expiry.
- System shows accrued interest separately from base amount.
- System updates total due dynamically.

#### FR5. Rewards engine

- System grants points for early payment.
- System grants cashback for early payment.
- System grants points for wallet top-ups.
- System may grant referral and streak bonuses.

#### FR6. Wallet

- User can add funds to wallet.
- Wallet balance updates immediately.
- Future version may support withdrawal, card, UPI, and bank rails.
- Wallet may be used for auto-pay.

#### FR7. Notifications

- User receives alerts for overdue items.
- User receives alerts for upcoming reward opportunities.
- User can receive reminder confirmation after nudging a payer.

#### FR8. Rewards redemption

- User can redeem points when minimum threshold is met.
- Redemption deducts point balance.
- UI reflects redeemed state.

#### FR9. Profile and settings

- User can review behavior score, points, streak, and settings.
- User can toggle auto-pay and reminders.
- User can enable theme changes.

#### FR10. Group management

- User can view groups.
- User can create groups with custom interest settings.
- User can inspect group-level payment history and pending balances.

### Non-functional requirements

#### NFR1. Usability

- Mobile-first design.
- One-handed navigation for common actions.
- Clear visibility of penalties and rewards.
- Low-friction forms.

#### NFR2. Transparency

- Interest logic must be visible before users agree.
- Reward logic must be explicit and auditable.
- Due dates, grace periods, and accrued values must never be hidden.

#### NFR3. Performance

- Main dashboard should load quickly.
- Wallet and rewards updates should feel instant.
- UI transitions should feel native.

#### NFR4. Accessibility

- High contrast text and status cues.
- Touch targets sized for mobile.
- Semantic structure for future production web/mobile adaptation.

#### NFR5. Trust and safety

- Financial penalties must be configurable and consent-based in real deployment.
- Payment actions should require secure authentication in production.
- Wallet operations must be auditable.

### Key business rules

- Interest starts only after the due date plus configured grace period.
- Early-payment rewards only apply before the due date cutoff.
- Cashback must not exceed configured caps in production.
- Point issuance and redemption require anti-abuse controls in production.
- Group-level interest policies may override global defaults where allowed.

### Data model overview

#### Core entities

- User
- Group
- Expense
- ExpenseParticipant
- Wallet
- WalletTransaction
- RewardAccount
- RewardTransaction
- Notification
- InterestPolicy
- Payment

#### Suggested fields

##### User
- user_id
- name
- email_or_phone
- avatar_url
- behavior_score
- streak_count
- points_balance

##### Group
- group_id
- name
- type
- owner_id
- interest_policy_id
- created_at

##### Expense
- expense_id
- group_id
- creator_id
- description
- category
- amount_total
- due_date
- split_type
- status
- created_at

##### ExpenseParticipant
- expense_participant_id
- expense_id
- user_id
- share_amount
- paid_amount
- overdue_interest_amount
- payment_status

##### Wallet
- wallet_id
- user_id
- balance
- auto_pay_enabled

##### RewardTransaction
- reward_txn_id
- user_id
- source_type
- points_delta
- cash_value_delta
- created_at

### Screen requirements

| Screen | Purpose | Primary actions | Supporting information |
|---|---|---|---|
| Home | Summary and prioritization | Review, tap expense, add funds | Wallet, points, alerts, feed |
| Groups | Contextual organization | Open group, create group | Group balance, members, status |
| Add Expense | Create shared obligation | Fill form, submit | Rules preview, due date, split logic |
| Rewards | Incentive management | Learn, redeem | Tier, earning logic, catalog |
| Profile | Identity and controls | Toggle settings, review score | Streak, score, points, theme |

[cite:1]

### Edge cases to address in production

- Partial payments.
- Split edits after some participants have already paid.
- Disputes over unfair interest application.
- Currency and locale differences.
- Failed wallet top-up.
- Negative wallet balance prevention.
- Redemption abuse.
- Group members leaving or being removed mid-cycle.
- Expense deletion after reminders have already been sent.
- Multiple reminder spam prevention.

### Assumptions in current prototype

- All values are illustrative.
- Wallet movement is simulated.
- Notifications are mock interactions.
- There is no backend persistence.
- There is no real payment gateway integration.
- Interest and reward calculations are currently represented as product logic demonstrations rather than audited financial calculations.

[cite:1]

## Recommended next product steps

### UX and design next steps

- Add onboarding flow explaining interest, grace period, and rewards.
- Add participant-level payment timeline.
- Add detailed transaction history for wallet and points.
- Add dispute and approval flow for penalties.
- Add better split customization UI for uneven shares.

### Product next steps

- Define configurable interest policies by group and jurisdiction.
- Build consent flow for joining a group with penalties enabled.
- Add payment rails such as UPI, bank transfer, card, and wallet autopay.
- Add analytics for payment behavior and reward efficiency.
- Add fraud and abuse controls for points/cashback.

### Engineering next steps

- Separate UI state from financial calculation engine.
- Create API contracts for users, expenses, wallet, and rewards.
- Add database schema and event-based ledgering for wallet and points.
- Implement scheduled jobs for due-date checks and interest accrual.
- Add test coverage for all financial rules.

## Handoff notes

This prototype is strong for:

- design review,
- founder/demo presentations,
- PRD discussion,
- MVP planning,
- front-end concept validation.

Before production launch, the most important areas to harden are:

- legal and policy compliance for interest charging,
- secure payment execution,
- dispute handling,
- auditability of wallet and rewards,
- fairness and consent in group settings.

[cite:1]
