# PITSAFE AFRICA — WaterOps

**Bilingual mine-water and dewatering operations prototype.**

PITSAFE AFRICA is an early-stage operational recordkeeping tool for mining contractors and mine-site teams. This prototype demonstrates how a team could record:

- Pump and water-infrastructure assets
- Manual water-level, flow and pressure readings
- Field inspection observations
- Maintenance actions and follow-up status
- Issues and incidents for review
- JSON and CSV exports

## Current version: browser prototype

The current `index.html` is a **local browser demo**, not a production cloud application.

- Records are stored in the browser's local storage on the device being used.
- Records are not shared between employees or devices.
- There is no login, organization/team administration, cloud synchronization, backup service, or role-based access in this prototype.
- It does not connect to sensors, SCADA, telemetry, mine systems, or automatic alerts.
- It does not control pumps or replace mine-approved safety procedures or emergency systems.

## Run the prototype

Open `index.html` in a modern web browser. For more reliable testing, serve this repository as a static website.

## Planned development

1. Add secure authentication and organization-based cloud data.
2. Add employee accounts, roles, and shared records.
3. Complete French and English interface coverage.
4. Add audit history, reporting, and controlled exports.
5. Test security, tenant isolation, backups, and mobile installation before any operational deployment.

## Safety and data handling

Use only data that you are authorized to record. Follow the mine's approved access, permit, HSE, and emergency procedures. Only competent and authorized personnel may perform specialist inspections or make safety-critical interpretations. This prototype is an operational recordkeeping aid; it is not an engineering design, statutory inspection certificate, geotechnical interpretation, safety clearance, or emergency alert service.

**PITSAFE AFRICA — Know the condition. Monitor the risk. Protect operations.**
