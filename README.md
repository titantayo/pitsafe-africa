# PITSAFE AFRICA — Mine Water & Dewatering Intelligence

Bilingual English/French prototype for mine-water and dewatering operations.

## Current prototype capabilities

- Pump and infrastructure register (browser demo data)
- Manual water-level records (browser demo data)
- Field inspection and maintenance records (browser demo data)
- Site alert form for leaks, unexpected water ingress, ground-condition observations, sump overflow, pump failure, power loss and instrument faults
- Organization-scoped cloud alert storage in Supabase for authenticated users with a valid PITSAFE profile
- PITSAFE INTELLIGENCE AI assistant interface and authenticated Edge Function

## Important integration status

This repository is an early-stage prototype, not a production mine operations system.

- The general pump, reading, inspection and maintenance forms still use browser-local storage. They are not yet synchronized across team members.
- Site alerts are connected to the Supabase `site_alerts` table, but require a signed-in user with a row in `public.profiles` assigned to the PITSAFE organization.
- The AI Edge Function is deployed with JWT verification and checks the signed-in user's organization before reading operational records. It analyses pumps, readings, inspections, maintenance and site alerts.
- AI requests remain inactive until an OpenAI API key is configured as the server-side Supabase Edge Function secret `OPENAI_API_KEY`. Never place this key in browser code or GitHub.
- Owner account provisioning and employee invitations are not yet configured.
- No SMS, email, push, siren, control-room integration, sensor/SCADA ingestion or guaranteed emergency notification is implemented.
- No physical underground hazard is automatically detected. Site alerts are manually entered observations.

## Emergency and safety boundary

If people may be in danger, immediately use the mine's approved emergency communication channel, notify the control room/supervisor, and follow the mine's emergency and evacuation procedures. Do not wait for this application. The software is not a certified alarm, safety instrumented system, geotechnical monitoring system, engineering design, statutory inspection certificate, or substitute for competent site personnel.

## Next engineering work

1. Provision the first owner account securely and create employee invitation flow.
2. Move pumps, readings, inspections and maintenance from browser storage into organization-scoped Supabase tables.
3. Configure the AI provider secret server-side and test the AI with authorized accounts.
4. Implement notification delivery with verified recipients, delivery logs, retries and acknowledgement workflows.
5. Integrate approved field sensors/telemetry only after hardware, communications, alarm thresholds and mine procedures are specified and validated.
6. Test tenant isolation, mobile behavior, backup/restore and operational failure modes before any mine-site pilot.

**PITSAFE AFRICA — Know the condition. Monitor the risk. Protect operations.**
