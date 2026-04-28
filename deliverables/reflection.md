f# Reflection: SBOM and System Patching

## Overview

This lab focused on analyzing a system-level SBOM before and after applying updates in an Ubuntu Codespace environment. The goal was to observe how vulnerabilities change after patching and understand how SBOMs support system security.

## Before vs After Analysis

Before applying updates, the system SBOM scan identified 634 vulnerabilities across multiple severity levels, including critical and high-risk issues. After running `apt update` and `apt upgrade`, the vulnerability scan results remained the same.

This shows that the system was already fully updated before the lab began. As a result, there were no package changes and no reduction in vulnerabilities.


Even though the system was “up to date,” vulnerabilities still existed. This shows that:
- Not all vulnerabilities have available patches
- Some fixes are not yet included in the repository
- Security depends on more than just running updates

## Complete Mediation

Maintaining updated packages reflects complete mediation because the system must continuously re-check its components against known vulnerabilities. Security is not a one-time action; it requires ongoing verification.

## SBOM and Assurance

Generating a new SBOM after patching is critical because it provides proof of the system’s current state. Without it, there is no reliable way to confirm what has changed or whether vulnerabilities were reduced.

## Risks of Delayed Updates

Delaying updates increases exposure to known vulnerabilities. Attackers often rely on publicly documented vulnerabilities, so failing to update gives them a predictable advantage.

## Secure Design Lifecycle

This lab demonstrates that security is part of the full lifecycle, not just development. Systems must be continuously monitored, updated, and reassessed using tools like SBOMs and vulnerability scanners.

## Conclusion

SBOMs provide visibility into system components, while tools like Grype connect those components to real-world vulnerabilities. Together, they allow teams to understand and manage risk more effectively.
