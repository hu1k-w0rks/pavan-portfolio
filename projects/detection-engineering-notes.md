# Detection Engineering Notes

## Focus
This document captures my approach to building practical and investigation-friendly KQL detections for SOC operations.

## Main Detection Areas
- Brute-force login attempts
- Suspicious PowerShell execution
- Linux privilege escalation
- Ransomware defense evasion
- Process-kill activity associated with ransomware behavior

## Detection Design Approach
When designing analytics, I focus on:
- Real attacker behavior
- Clear investigation value
- Reducing noisy alerts
- Supporting practical SOC triage

## Example Area: Ransomware Process-Kill Behavior
One area I focused on was process-kill activity that may indicate ransomware attempting to disable defenses, terminate services, or interfere with backup/security-related processes before encryption activity.

My goal in building these detections was not just alert generation, but creating alerts that provide useful context to an analyst during triage.

## Why This Matters
Detection engineering is valuable when alerts are meaningful, relevant, and useful during investigation. My focus is on building detections that support faster and better analyst decisions rather than creating high alert volume with low context.
