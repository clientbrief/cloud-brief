# Cloud Client Brief  
**Scenario ID:** CB-CLOUD-001  
**Industry:** Financial Services (Non-Bank)  
**Company Size:** ~180 employees  
**Geography:** Southeast Asia  
**Cloud Maturity:** Low to Medium  
**Timeline Sensitivity:** High  

---

## 1. Client Background

The client is a mid-sized financial services company operating in the consumer lending and payment aggregation space. The organization has been in operation for more than 8 years and has experienced rapid growth over the last 24 months.

Most of the company’s technology stack was built incrementally to support immediate business needs rather than long-term scalability or architectural consistency.

The engineering team is capable but relatively small, with limited exposure to large-scale cloud-native systems.

---

## 2. Business Context

The company is preparing to launch two new digital products within the next 3 months. These products are expected to increase transaction volume significantly but are not yet projected to generate immediate profit.

Senior management has mandated that:
- Infrastructure costs must remain predictable
- No major operational disruptions are acceptable during launch
- The team should avoid long-term vendor lock-in where possible

At the same time, regulatory scrutiny around data handling and availability has increased.

---

## 3. Current State (Existing Systems)

The current system landscape includes:

- A monolithic backend application running on virtual machines
- Relational database hosted on a self-managed instance
- Manual deployment processes with minimal automation
- Centralized logging is limited and inconsistent
- Backups exist but recovery procedures are not regularly tested

The system has historically handled moderate traffic, with occasional availability issues during peak usage.

---

## 4. Technical Requirements (Known)

The client has identified the following high-level requirements:

- Support a projected 2–3x increase in transaction volume
- Improve baseline system availability
- Ensure basic disaster recovery capability
- Enable faster deployment cycles for product teams
- Maintain data residency within the region

These requirements are considered **directional**, not exhaustive.

---

## 5. Constraints & Limitations

### Financial Constraints
- Infrastructure budget is capped and closely monitored
- No approval for large upfront capital expenditure
- Preference for incremental cost growth tied to usage

### Organizational Constraints
- Engineering team has limited cloud-native experience
- No dedicated SRE or platform team
- Operational ownership remains with the same team building features

### Technical Constraints
- Existing application cannot be fully refactored in the short term
- Some legacy components are poorly documented
- Downtime tolerance during business hours is very low

### Time Constraints
- Initial improvements must be delivered within 6–8 weeks
- Long-term modernization can only be justified after product launch

---

## 6. Compliance & Risk Considerations

The organization operates under financial regulatory oversight, requiring:

- Data encryption at rest and in transit
- Access control and auditability
- Reasonable availability guarantees

Formal certifications are not immediately required, but **failure to demonstrate basic controls may trigger regulatory attention**.

---

## 7. Known Risks

- Cost overruns if scaling behavior is not well understood
- Operational burden shifting too quickly to an inexperienced team
- Partial improvements creating inconsistent system behavior
- Over-engineering solutions beyond the organization’s ability to maintain

---

## 8. Open Questions & Ambiguities

The client has not yet provided clear answers to the following:

- Acceptable recovery time objectives (RTO)
- Acceptable recovery point objectives (RPO)
- Expected traffic patterns (steady vs bursty)
- Long-term commitment to a single cloud provider
- Appetite for managed services vs self-managed control

These ambiguities are expected to influence architectural decisions significantly.

---

## 9. Decision Context Summary

This is **not** a greenfield system.

Any proposed approach must:
- Respect existing system constraints
- Balance reliability improvements against operational simplicity
- Avoid introducing complexity that the current team cannot sustain
- Accept that some risks may remain in the short term

The objective is **reasonable improvement**, not architectural perfection.

---

## Disclaimer

This brief is fictional and does not represent a real organization.  
It is designed to simulate common decision-making contexts encountered in real-world cloud engineering engagements.
