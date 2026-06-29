# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

---

## Additional Personas (Suggested additions)

The following personas are suggested additions to improve clarity, accountability, and cross-functional collaboration. Each entry includes a short role summary, responsibilities, and interactions with existing roles.

### Engineering Manager

#### Role Summary
Engineering Managers balance team delivery, people development, and technical direction.

#### Responsibilities
- Team capacity planning and resource allocation
- Performance coaching and career development for engineers
- Technical leadership and ensuring engineering best practices
- Escalation point for resourcing or technical impediments

#### Interactions
- Works with Project Manager for resourcing and timeline adjustments
- Collaborates with Product Manager on roadmap feasibility and technical trade-offs
- Supports Developers through code reviews and technical guidance

---

### UX Researcher / Designer

#### Role Summary
UX Researchers and Designers ensure product decisions are informed by user insights and usability best practices.

#### Responsibilities
- Plan and run user research and usability tests
- Define UX acceptance criteria and design specs
- Create wireframes, prototypes, and interaction patterns
- Validate implemented features against usability goals

#### Interactions
- Feeds research insights to Product Manager and PM
- Works with Developers to implement designs and resolve trade-offs
- Supports QA with usability-focused acceptance checks

---

### Release Manager

#### Role Summary
Release Managers coordinate and govern the release process to production.

#### Responsibilities
- Maintain and enforce the release checklist and gating criteria
- Schedule and approve deployment windows where needed
- Coordinate rollback and mitigation plans
- Ensure stakeholder and customer communications for releases

#### Interactions
- Coordinates with DevOps/Platform and Engineers for deploy readiness
- Works with Project Manager to align release timing with stakeholder needs
- Communicates with Customer Support / Success for post-release monitoring

---

### DevOps / Platform Engineer

#### Role Summary
Platform engineers maintain the CI/CD pipelines, observability, and infrastructure that enable reliable delivery.

#### Responsibilities
- Maintain CI/CD pipelines and automation
- Configure and operate observability and alerting
- Ensure security scans and infrastructure readiness
- Support incident response and post-mortems

#### Interactions
- Works with Developers on deployment and infra-related changes
- Collaborates with Release Manager to validate deployment steps
- Coordinates with Security Liaison for remediation and compliance

---

### Customer Success / Support Lead

#### Role Summary
Customer Success and Support representatives surface customer issues and help prioritize customer-facing improvements.

#### Responsibilities
- Triage and communicate customer-impacting issues
- Prioritize support-driven bugs and feature requests
- Provide customer context and feedback to Product and PM
- Coordinate customer communications during incidents or releases

#### Interactions
- Works with Product Manager to influence prioritization
- Collaborates with Project Manager / Release Manager on customer communications
- Escalates urgent customer-impacting issues to the PM and Engineering Manager

---

### Data Analyst

#### Role Summary
Data Analysts define, measure, and interpret success metrics to guide product decisions.

#### Responsibilities
- Define and track success metrics and KPIs
- Instrument events and validate telemetry
- Analyze experiments and provide insights
- Help set targets and measure impact after releases

#### Interactions
- Works with Product Manager to refine success criteria
- Partners with Developers to ensure instrumentation is implemented correctly
- Provides analytics for retrospectives and planning

---

### Security Liaison

#### Role Summary
The Security Liaison coordinates security reviews, risk management, and incident response related to product work.

#### Responsibilities
- Coordinate security reviews and threat modeling
- Track and triage security findings and remediation
- Participate in incident response when security is involved
- Ensure secure design and compliance requirements are considered early

#### Interactions
- Works with DevOps, Engineers, and Product to ensure secure implementations
- Escalates high-severity security risks to Project Manager and Product Lead

---

### Program / Portfolio Manager

#### Role Summary
Program or Portfolio Managers coordinate across multiple related projects to manage dependencies and consolidated reporting.

#### Responsibilities
- Coordinate dependencies and timelines across projects
- Consolidate reporting and stakeholder briefings
- Manage cross-project risks and escalations
- Align priorities across product and engineering teams

#### Interactions
- Works with Project Managers for cross-team coordination
- Collaborates with Product Leads to balance roadmap priorities
- Escalates portfolio-level blockers to sponsors

---

## Example machine-readable persona mapping

The following YAML snippet can be used to seed automation (labels, CODEOWNERS, or templates) or be adapted for team tooling:

```yaml
personas:
  - id: engineering_manager
    display_name: "Engineering Manager"
    responsibilities:
      - "Capacity planning"
      - "People development"
      - "Technical oversight"
    contacts:
      - role: project_manager
      - role: product_manager

  - id: ux_researcher
    display_name: "UX Researcher / Designer"
    responsibilities:
      - "User research"
      - "Design acceptance"
    contacts:
      - role: product_manager
      - role: developers

  - id: release_manager
    display_name: "Release Manager"
    responsibilities:
      - "Release coordination"
      - "Rollback planning"
    contacts:
      - role: devops
      - role: project_manager

  - id: devops
    display_name: "DevOps / Platform Engineer"
    responsibilities:
      - "CI/CD maintenance"
      - "Observability"
    contacts:
      - role: developers
      - role: security_liaison

  - id: customer_success
    display_name: "Customer Success / Support Lead"
    responsibilities:
      - "Customer communications"
      - "Support prioritization"
    contacts:
      - role: product_manager
      - role: project_manager

  - id: data_analyst
    display_name: "Data Analyst"
    responsibilities:
      - "Instrumentation"
      - "Metrics tracking"
    contacts:
      - role: product_manager
      - role: developers

  - id: security_liaison
    display_name: "Security Liaison"
    responsibilities:
      - "Security reviews"
      - "Incident participation"
    contacts:
      - role: devops
      - role: engineering_manager

  - id: program_manager
    display_name: "Program / Portfolio Manager"
    responsibilities:
      - "Cross-project coordination"
      - "Consolidated reporting"
    contacts:
      - role: project_manager
      - role: product_lead
```

---

## Suggested next steps
- Add these personas to the roles document and link them from relevant process docs (planning, release, risk, retrospectives).
- Review with PMs, Product Leads, Engineering Managers, Security, and Support to refine responsibilities and owners.
- Consider seeding automation (labels, templates, CODEOWNERS) using the YAML mapping above.
