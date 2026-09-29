# ServiceNow - Client Script & UI Policy for Incident Table

## Project Description
This project implements Client Scripts and UI Policies on the Incident table in ServiceNow to enhance form behavior and user experience.

## Implementation Details

### 1. Client Script (Incident)
- **Table:** Incident [incident]
- **Type:** onChange / onLoad
- **Purpose:** Auto-populate fields and validate inputs
- **Script:**
```javascript
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
   if (isLoading || newValue === '') {
      return;
   }
   // Example: Set priority based on impact and urgency
   g_form.addInfoMessage('Client Script executed successfully');
}
