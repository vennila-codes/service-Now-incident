# ServiceNow Client Scripts & UI Policy Implementation

## Instance Details
- PDI: dev430310

## Implementation Details

### 1. UI Policy: Mandatory Assigned To Field
- **Purpose**: Enforce field mandate when Impact is High.
- **Conditions**: Impact = 1 - High
- **Affected Fields**: Assigned to (Set Mandatory = True)

### 2. onChange Client Script: Impact & Urgency Validation
- **Purpose**: Dynamically monitor form behavior on field changes.
- **Affected Fields**: Impact, Urgency

### 3. onCellEdit Client Script: Block List Edit for State Field
- **Purpose**: Prevent users from updating the State field directly from list view.
- **Affected Fields**: State
- **Expected Behavior**: Triggers alert "State cannot be updated using list editing. Please open the Incident."
