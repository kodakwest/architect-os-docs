---
name: "📖 User Story"
description: "Create a new user story for a feature or enhancement"
title: "[Story] <Brief description of the feature>"
labels: ["✨ Feature"]
body:
  - type: markdown
    attributes:
      value: |
        **For User Stories:**
        Create complete user stories following the format below. Focus on the business end user, not developers.

  - type: textarea
    id: story-phrase
    attributes:
      label: User Story Phrase
      description: "Complete the following statement"
      placeholder: |
        **As a** [Type of user],
        **I want** [What they want to do],
        **So that** [Why it's important to them]
    validations:
      required: true

  - type: textarea
    id: background
    attributes:
      label: Background
      description: Contextual information about the user and their needs
      placeholder: Describe the user persona and why they need this feature
    validations:
      required: true

  - type: textarea
    id: details
    attributes:
      label: Details
      description: Specific requirements, behaviors, or interactions
      placeholder: List specific requirements and expected behaviors
    validations:
      required: true

  - type: textarea
    id: questions
    attributes:
      label: Questions We Are Trying to Answer
      description: For SPIKE/Research stories, include a list of questions
      placeholder: What uncertainties need to be resolved?
    validations:
      required: false

  - type: textarea
    id: testing-criteria
    attributes:
      label: Testing Criteria
      description: How to verify the story is complete
      placeholder: List acceptance tests and verification steps
    validations:
      required: true

  - type: textarea
    id: dev-tasks
    attributes:
      label: Potential Development Tasks
      description: Breakdown of work needed
      placeholder: "- [ ] Task 1\n- [ ] Task 2"
    validations:
      required: false

  - type: textarea
    id: measurement-criteria
    attributes:
      label: Measurement Criteria/Cases
      description: How to track success after implementation
      placeholder: Define metrics or success indicators
    validations:
      required: false

  - type: dropdown
    id: feature-flag
    attributes:
      label: Feature Flag
      description: Is a feature flag needed?
      options:
        - "Yes"
        - "No"
        - "Not Applicable"
    validations:
      required: true

  - type: textarea
    id: snackbar-messaging
    attributes:
      label: Snackbar Messaging
      description: UI/UX notifications (if applicable)
      placeholder: What messages should users see?
    validations:
      required: false

  - type: dropdown
    id: audit-history
    attributes:
      label: Audit History Enablement
      description: Should changes be tracked in audit history?
      options:
        - "Yes"
        - "No"
        - "Not Applicable"
    validations:
      required: true

  - type: textarea
    id: acceptance-criteria
    attributes:
      label: Acceptance Criteria (Gherkin)
      description: Write acceptance criteria in Gherkin format
      placeholder: |
        ```gherkin
        Feature: [Feature name]
          As a [Type of user]
          I want [What they want to do]
          So that [Why it's important to them]

          Scenario: [Specific scenario to test]
            Given [Precondition]
            When [Action]
            Then [Expected result]
        ```
      render: gherkin
    validations:
      required: true
