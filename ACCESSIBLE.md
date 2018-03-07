# A few crucial Accessibility Requirements

## 1. Text Alternatives


| WCAG 2.0 | 2017 Section 508 |
| -- | -- |
| [1.1.1](https://www.w3.org/TR/UNDERSTANDING-WCAG20/text-equiv-all.html) | 501 (Web)(Software)<br>504.2 (Authoring Tool)<br>602.3 (Support Docs)|

> All non-text content that is presented to the user has a text alternative that serves the equivalent purpose, with certain exceptions.

This means that non-text content like images should use the `alt` attribute to provide alternate text to summarize the content of the images for non-sighted users. Decorative images or images that do not convey meanings should use `alt=""`.

Text alternatives are a primary way for making information accessible because they can be rendered through any sensory modality (e.g.,, visual, auditory or tactile) to match the needs ofthe user.

## 2. Info and Relationships

### Clear Semantics


| WCAG 2.0 | 2017 Section 508 |
| -- | -- |
| [1.3.1](https://www.w3.org/TR/UNDERSTANDING-WCAG20/content-structure-separation-programmatic.html) | 501 (Web)(Software)<br>504.2 (Authoring Tool)<br>602.3 (Support Docs)|

> Information, structure, and relationships conveyed through presentation can be programmatically determined or are available in text.

This means that webpages should have good semantic structure. Assistive Technologies (AT) rely on semantic code to drive their behavior. Information architecture is important. Non-sighted users should be able to infer the same information as sighted users without depending on colors, shape, or typography for context.

### Bypass Blocks

| WCAG 2.0 | 2017 Section 508 |
| -- | -- |
| [2.4.1](https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-skip.html) | 501 (Web)(Software) – Does not apply to non-web software<br>504.2 (Authoring Tool)<br>602.3 (Support Docs) – Does not apply to non-web docs |

> A mechanism is available to bypass blocks of content that are repeated on multiple Webpages.

This means that pages should have mechanisms like [Skip-Navigation](https://webaim.org/techniques/aria/#landmarks) and [WAI ARIA landmark roles](https://webaim.org/techniques/aria/#landmarks) for users to jump to the main content or a particular content area.

### Labels or Instructions

| WCAG 2.0 | 2017 Section 508 |
| -- | -- |
| [3.3.2](https://www.w3.org/TR/UNDERSTANDING-WCAG20/minimize-error-cues.html) |  501 (Web)(Software)<br>504.2 (Authoring Tool)<br>602.3 (Support Docs) |

> Labels or instructions are provided when content requires user input.

This means that labels should be associated with form inputs so that users know what input data is expected.

## 3. Keyboard

### Keyboard Operable

| WCAG 2.0 | 2017 Section 508 |
| -- | -- |
| [2.1.1](https://www.w3.org/TR/UNDERSTANDING-WCAG20/keyboard-operation-keyboard-operable.html) |  501 (Web)(Software)<br>504.2 (Authoring Tool)<br>602.3 (Support Docs) |

> All functionality of the content is operable through a keyboard interface without requiring specific timings for individual keystrokes, except where the underlying function requires input that depends on the path of the user's movement and not just the endpoints.

This means that keyboard users should be able to use all page functionalities using keyboard only. They should be able to tab through links/forms or navigate the page by screen readers with keyboard.

### Focus Order

| WCAG 2.0 | 2017 Section 508 |
| -- | -- |
| [2.4.3](https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-focus-order.html) |  501 (Web)(Software)<br>504.2 (Authoring Tool)<br>602.3 (Support Docs) |

> If a Web page can be navigated sequentially and the navigation sequences affect meaning or operation, focusable components receive focus in an order that preserves meaning and operability.

This means that interactive elements on a page like forms, links, buttons, etc. should be in logical and sequential order.

### Focus Visible

| WCAG 2.0 | 2017 Section 508 |
| -- | -- |
| [2.4.7](https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-focus-visible.html) |  501 (Web)(Software)<br>504.2 (Authoring Tool)<br>602.3 (Support Docs) |

> Any keyboard operable user interface has a mode of operation where the keyboard focus indicator is visible.

This means that users should be able to see which element of a webpage has keyboard focus.

### No Keyboard Trap

| WCAG 2.0 | 2017 Section 508 |
| -- | -- |
| [2.1.2](https://www.w3.org/TR/UNDERSTANDING-WCAG20/keyboard-operation-trapping.html) |  501 (Web)(Software)<br>504.2 (Authoring Tool)<br>602.3 (Support Docs) |

> If keyboard focus can be moved to a component of the page using a keyboard interface, then focus can be moved away from that component using only a keyboard interface, and, if it requires more than unmodified arrow or tab keys or other standard exit methods, the user is advised of the method for moving focus away.

This means that content does not "trap" keyboard focus within subsections of content on a Web page. Users should be able to exit modals, dialog windows, off-canvas navigation, and panels via keyboard navigation (e.g., cancel buttons or "x" close links.)

## 4. Color

### Use of Color

| WCAG 2.0 | 2017 Section 508 |
| -- | -- |
| [1.4.1](https://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-without-color.html) |  501 (Web)(Software)<br>504.2 (Authoring Tool)<br>602.3 (Support Docs) |

> Color is not used as the only visual means of conveying information, indicating an action,prompting a response, or distinguishing a visual element.

This means that color cannot be the sole means of inferring meaning from content. Providing the information conveyed with color through another visual means ensures users who cannot see color can still perceive the information.

### Minimum Contrast

| WCAG 2.0 | 2017 Section 508 |
| -- | -- |
| [1.4.3](https://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-contrast.html) |  501 (Web)(Software)<br>504.2 (Authoring Tool)<br>602.3 (Support Docs) |

> The visual presentation of text and images of text has a contrast ratio of at least 4.5:1, except
for the following: 1) large text, 2) incidental text, or 3) logotype.

This means that pages should provide enough contrast between text and its background sothat it can be read by people with moderately low vision.

## 5. Language

| WCAG 2.0 | 2017 Section 508 |
| -- | -- |
| [3.1.1](https://www.w3.org/TR/UNDERSTANDING-WCAG20/meaning-doc-lang-id.html) |  501 (Web)(Software)<br>504.2 (Authoring Tool)<br>602.3 (Support Docs) |

> The default human language of each Web page can be programmatically determined.

This means that every webpage should have a language assigned. Setting a language is important because the way that screen readers pronounce words depends on the HTML language assigned to the webpage.
