# ✍️ Writing Tips for Product Specs (ChatGPT-style Applications)

Use these guidelines when drafting product requirement documents, JIRA tickets, prompt instructions, or UX flows for AI chat-based tools.

---

## ✍️ Writing Principles

### 1. Start with the Problem

* Clearly define what problem is being solved and why it matters.
* Avoid jumping straight into solutions.

### 2. Keep Sentences Short and Direct

* Use fewer than 30 words per sentence.
* Eliminate unnecessary modifiers and redundant phrases.

### 3. Be Specific and Testable

* Ensure every requirement is verifiable and measurable.
* Write for QA, not just engineers or stakeholders.

### 4. Replace Fluff with Data

* Avoid adjectives like "robust" or "fast."
* Provide metrics wherever possible.

### 5. Eliminate Weasel Words

* Avoid vague qualifiers like "some," "many," or "significantly."
* Use precise, supported claims.

### 6. Avoid Jargon and Explain Acronyms

* Spell out acronyms on first use.
* Use plain, accessible language.

### 7. Separate Requirements from Implementation

* Define "what" before "how."
* Allow engineering flexibility.

### 8. Use Active Voice and Assign Ownership

* Be explicit about who or what performs each action.
* Avoid passive constructions.

### 9. Use Lists, Tables, and Visual Structure

* Organize data clearly with bullets, numbered steps, and tables.
* Improve scanability and comprehension.

### 10. Use Consistent Terms

* Stick to one term for each concept across the doc.
* Prevent confusion and misalignment.

### 11. Include Units, Metrics, and Timeframes

* Always specify values clearly (e.g., "2.5s latency," "20MB files").
* Avoid vague timing references like "soon."

### 12. Be Concise, Not Abrupt

* Write efficiently but preserve clarity.
* Trim filler words and redundancies.

### 13. Acknowledge Exceptions Thoughtfully

* Note when a rule might not apply (e.g., for marketing tone).
* Justify deviations with intent.

### 14. End with Next Steps or Open Questions

* Clarify ownership, dependencies, and decisions pending.

---

## 📘 Examples for ChatGPT-style Application Specs

### Example 1: Problem-First, Data-Backed

**Bad**: We want the assistant to be more helpful.

**Better**: 37% of multi-turn chats fail to resolve the user's question. The assistant often ignores prior turns.

---

### Example 2: Testable, Specific Requirements

**Bad**: Improve model relevance and response time.

**Better**:

* Return responses within 1.8 seconds p90 latency.
* Generate replies rated ≥85% relevant in Q3 grounding eval.

---

### Example 3: Avoid Weasel Words and Hype

**Bad**: This feature will revolutionize how users interact with AI.

**Better**: Adding retrieval grounding is projected to reduce hallucination rates by 30% (internal eval 5.3).

---

### Example 4: Active Voice, Clear Ownership

**Bad**: An error message is returned if the query is invalid.

**Better**: The assistant API returns a 400 error with validation details.

---

### Example 5: Separate Requirement from Solution

**Bad**: Fine-tune GPT-4 on internal docs.

**Better**: Assistant must answer 90% of internal queries from document uploads. Solutions may include RAG, fine-tuning, or hybrids.

---

### Example 6: Use Lists and Structure

**Acceptance Criteria**:

* [ ] Response latency ≤ 2s (p90)
* [ ] Shows 3 source documents when grounded
* [ ] Includes section-level citation metadata

---

### Example 7: Include Units and Limits

**Bad**: Keep prompts short.

**Better**: Ensure system + user + assistant messages remain ≤4096 tokens (GPT-4o limit).

---

### Example 8: UX Flow Detail

1. User uploads PDF.
2. System parses and embeds sections.
3. User types question.
4. System retrieves top 3 chunks.
5. Assistant replies with inline citations and toggleable sources.

---

### Example 9: Clarify Decisions and Next Steps

**Next Steps**:

* Define fallback behavior for missing document grounding.
* Assign owner for hallucination eval rubric.
* Decide whether to display model uncertainty scores to user.
