# Strict final fix notes

Applied after Elon Musk / Steve Jobs audit.

Implemented fixes, excluding requested exceptions 5, 6, 7 and 8:

- Added a final robust i18n layer using stable data-i18n keys and original Hungarian source storage.
- Removed the previous hidden-Hungarian workaround for EN/DE views; no visible Hungarian fallback should remain in English or German mode.
- Added language-specific export generation for the hidden `formattedAnswers` payload.
- Added hidden legal metadata fields for AI tools, public internet research, special-category data warning, business-secret/third-party-data authority and retention notice.
- Strengthened GDPR/AI notices for Claude, ChatGPT and Grok, including external AI-provider processing, internet research, business secrets/NDA, third-party data and retention.
- Kept the first page length, legal layout, non-step-by-step structure and client-side password model unchanged per instruction.
