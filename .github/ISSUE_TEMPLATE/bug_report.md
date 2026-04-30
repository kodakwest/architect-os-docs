---
name: "🐛 Bug Report"
description: "Report a bug or unexpected behavior"
title: "[Bug] <Brief description of the issue>"
labels: ["🐛 Bug"]
body:
  - type: markdown
    attributes:
      value: |
        **For Bug Tickets:**
        Create comprehensive bug tickets using this template. Be specific and include all relevant details.

  - type: textarea
    id: issue-description
    attributes:
      label: Issue Description
      description: Clear summary of the problem
      placeholder: What is happening that shouldn't be?
    validations:
      required: true

  - type: textarea
    id: preconditions
    attributes:
      label: Preconditions
      description: What must be true before the issue can occur
      placeholder: |
        - Systems accessed
        - Platforms used
        - Access levels and roles of each actor
    validations:
      required: true

  - type: textarea
    id: steps-to-reproduce
    attributes:
      label: Steps to Reproduce
      description: Detailed steps to consistently reproduce the bug
      placeholder: |
        1. Go to '...'
        2. Click on '...'
        3. Scroll down to '...'
        4. See error
    validations:
      required: true

  - type: textarea
    id: expected-result
    attributes:
      label: Expected Result
      description: What should happen according to design or requirements
      placeholder: Describe the expected behavior
    validations:
      required: true

  - type: textarea
    id: actual-result
    attributes:
      label: Actual Result
      description: What actually happens when following the steps
      placeholder: Describe what actually occurs
    validations:
      required: true

  - type: dropdown
    id: impact
    attributes:
      label: Impact
      description: Severity of the issue
      options:
        - "🔴 Critical - System down, data loss, security breach"
        - "🟡 High - Major functionality broken, workaround exists"
        - "🟢 Medium - Minor issue, minimal impact on users"
        - "🔵 Low - Cosmetic, typo, nice-to-have fix"
    validations:
      required: true

  - type: textarea
    id: environment
    attributes:
      label: Environment/URL/Folder or UI Location/User Info
      description: Where the bug occurs
      placeholder: |
        - Browser/OS version
        - URL or file path
        - User role/permissions
    validations:
      required: true

  - type: textarea
    id: error-messages
    attributes:
      label: Error Messages or Error Codes
      description: Any technical details that might help diagnose
      placeholder: Copy/paste any error messages or codes
    validations:
      required: false

  - type: textarea
    id: testing-criteria
    attributes:
      label: Testing Criteria
      description: How to verify the bug is fixed
      placeholder: What tests should pass after the fix?
    validations:
      required: true

  - type: textarea
    id: potential-tasks
    attributes:
      label: Potential Tasks
      description: Breakdown of work needed to fix the issue
      placeholder: "- [ ] Investigate root cause\n- [ ] Implement fix\n- [ ] Add tests"
    validations:
      required: false

  - type: textarea
    id: definition-of-done
    attributes:
      label: Definition of Done
      description: Criteria for closing the ticket
      placeholder: What must be complete to close this ticket?
    validations:
      required: true

  - type: textarea
    id: attachments
    attributes:
      label: Screenshots/Attachments
      description: Add any relevant screenshots, logs, or files
      placeholder: Drag and drop images or files here
    validations:
      required: false
