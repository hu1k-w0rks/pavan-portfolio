# Ransomware Detection Investigation Case Study

## Scenario
A controlled ransomware sample was executed in a monitored lab environment to observe how endpoint protection detects, blocks, and exposes malicious behavior through security telemetry.

## Objective
To understand ransomware detection behavior from an analyst perspective and review the investigation workflow using endpoint telemetry.

## Environment
- Isolated test environment
- Sophos Endpoint protection
- Threat telemetry and process graph visibility

## Detection
Sophos Endpoint detected and blocked the ransomware during execution.

## Investigation
The investigation focused on understanding:
- How the ransomware execution appeared in telemetry
- Which alerts were raised
- What process relationships were visible
- Whether the endpoint response successfully contained the threat

I reviewed the Sophos threat graph to analyze the execution chain, related process activity, and suspicious behaviors associated with the payload.

## Findings
- The detection was behavior-based and triggered during execution
- Telemetry clearly showed suspicious process activity
- The endpoint protection successfully blocked further malicious progression
- The investigation data was useful for understanding both detection logic and response effectiveness

## Response Validation
- Confirmed containment
- Reviewed relevant threat telemetry
- Documented the observed behavior and investigation findings

## Key Takeaways
- Behavioral detections are critical for modern ransomware defense
- Process visibility greatly improves analyst investigation quality
- Strong endpoint telemetry helps analysts validate both detection and containment
