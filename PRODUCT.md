# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Static HTML (single-file index.html), hosted on Vercel. Landing page only; app is a separate deployment.

## Users

**Primary — the barber.** Includes the barber who rents a chair or works on commission inside someone else's shop. They create their own account, build their own booking page, and tell the system which barbershop they work at (name and address). The agenda and the clients are theirs. They lose money to no-shows and empty slots, and they make decisions fast. Not technical; lives on their phone; promotes their work on Instagram; has little time; distrusts complicated systems and inflated promises.

**Secondary — the barbershop owner with a team.** Can use Agendou to manage multiple barbers: per-barber agenda, commissions, "no preference" option for the client, multi-location. Not the current build target.

**End user — the barber's client.** Books via mobile, ideally in seconds, without downloading an app or creating an account.

The landing speaks barber-to-barber: "sua agenda", "seus clientes", "seu WhatsApp", "seu link."

## Product Purpose

Agendou gives every barber a self-booking link (agendou/{nome}) ready to drop in their Instagram bio. The client picks a service, a day, and a slot; confirms with just a name and phone number; no app, no account. The barber stops answering "tem horário?" between cuts, loses fewer clients to no-shows, and always knows what came in and what's still owed.

## Positioning

The barber starts alone, free, independent of the shop owner — no IT setup, no negotiation. The client books in seconds from the bio link, which is the lowest-friction booking experience in the Brazilian barbershop market. WhatsApp confirmation arrives from the barber's own number with real delivery status (not a platform number, not a fake "sent" tick). Built-in subscription club (renda previsível) and Pix to hold the slot are features most competitors charge separately for or don't offer.

## Operating Context

- Barber's primary acquisition channel: Instagram bio link
- All communication with clients happens on WhatsApp — clients won't install another app
- Barbers work solo or in small shops with no IT support; must be instant to set up
- Payment: Pix (and card); no automatic renewal; pay when they want
- App entry point: https://app-barber-agendamentos.vercel.app/cadastro?plano=gratuito|mensal|trimestral|anual

## Capabilities and Constraints

**Confirmed features (do not invent others):**
1. Booking link (agendou/{nome}): custom photo, logo, colors; client picks service → day → slot → confirms with name + phone only
2. Per-booking client link to reschedule or cancel within the barber's defined window; save-to-calendar button
3. WhatsApp confirmation + reminder via official Meta API from the barber's own number; fallback: one-tap manual message with prefilled text
4. Optional/mandatory Pix to hold the slot (signal or full amount) with QR code and deadline — reduces no-shows
5. Day agenda, manual booking, vacation/block-out, working hours with lunch break
6. Financial: income received, amount still owed, period reports, CSV export
7. Clients: per-client history, total spent, churned (45+ days), recurring vs. new
8. Client list import via CSV/Excel — don't start from zero
9. Subscription plans / loyalty club the barber sells to their own clients (e.g. "unlimited cuts for R$ X/month"), usage and billing control — predictable monthly income
10. Team: multiple barbers on one agenda, per-barber commission, "no preference" option, multi-location

**Free tier:** up to 15 clients, no credit card. All features available at every plan tier — the only difference is the client limit.

## Brand Commitments

- Name: Agendou
- App URL pattern: https://app-barber-agendamentos.vercel.app/cadastro?plano=gratuito|mensal|trimestral|anual
- Language: Brazilian Portuguese throughout
- Prices in BRL; payment via Pix (and card)
- Typography: Inter for interface copy; Geist Mono for times, prices, and codes (reinforces the agenda/clock concept)
- Visual base: near-black background #07080a; warm CSS aurora animation (crimson #ff2f3a → coral #ff6b4a → amber #ffb347) with grain and vignette; prefers-reduced-motion respected; everything else neutral (white #fff, gray #9c9c9d); accent/CTA warm (#ff5a3c / #e85a3a) used sparingly
- Components: discreet glass panels, pill buttons, status badges with dot + text (never color alone)
- Voice: direct, Brazilian, barber-to-barber. Short sentences, concrete verbs (agenda, confirma, lembra, recebe). Day-to-day barbershop language without forced slang. Never: "revolucione", "potencialize", "solução completa", "tudo em um só lugar", "leve seu negócio ao próximo nível". Show, don't promise.

## Evidence on Hand

**Confirmed pricing (exact values):**
- Gratuito: R$ 0 — up to 15 clients
- Mensal: R$ 59,90/mês
- Trimestral: R$ 159,90/trimestre
- Anual: R$ 599,90/ano
- All features included in every plan

**What does not exist yet:** no confirmed testimonials, real client counts, star ratings, partner logos, or press. These must never be fabricated.

## Product Principles

1. **Zero friction for the client.** If booking needs an app or an account, the barber loses the client. Frictionlessness is non-negotiable.
2. **The barber owns their own business.** Their link, their WhatsApp, their clients, their money — independent of the shop owner.
3. **WhatsApp is the confirmation layer.** Brazilian barbers and clients live on WhatsApp; work with it, not around it.
4. **Start free, grow into paid.** The free tier must be genuinely useful — it earns trust before asking for money.
5. **Show, don't promise.** Real product screens and real workflows beat claims and inflated metrics.

## Accessibility & Inclusion

No product-specific accessibility requirements confirmed. Standard WCAG AA for the landing page. Mobile-first: most traffic arrives from Instagram on a phone.
