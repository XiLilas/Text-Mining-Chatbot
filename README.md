# Text-Mining-Chatbot
NLP



Work 1 “compare.ipynb” focuses on Part-of-Speech (PoS) tagging and syntactic parsing to analyze linguistic ambiguity and sentence structure in both general and scientific English texts.

We study and compare manual annotation, rule-based parsing, and automatic NLP tools, highlighting their advantages and limitations.

⸻

Part 1 – Part-of-Speech Tagging

In the first part, we perform PoS tagging on six sentences, including ambiguous examples and scientific sentences from biology and astronomy.

Three approaches are used:
	•	Manual annotation using a restricted set of Universal Dependencies PoS tags
(ADJ, ADP, AUX, DET, NOUN, NUM, PROPN, PUNCT, SCONJ, VERB)
	•	spaCy with the en_core_web_sm model for general English
	•	sciSpaCy with the en_core_sci_sm model for scientific text

Manual annotation allows multiple valid PoS interpretations for ambiguous sentences, while automatic tools provide a single best prediction. spaCy performs well on common language, whereas sciSpaCy better handles scientific terminology but may be less stable on general sentences.

⸻

Part 2 – Syntactic Parsing

In the second part, we apply the CYK (Cocke–Younger–Kasami) algorithm for constituency parsing using manually defined context-free grammar rules.

Parsing is performed using:
	•	Multiple possible PoS tags per word
	•	A limited set of non-terminals: S, NP, VP, PP

This approach generates multiple parse trees, especially for ambiguous sentences, illustrating how grammar choices influence syntactic interpretation and ambiguity.

To compare results, we also perform automatic constituency parsing using the Berkeley constituency parser online https://parser.kitaev.io, which produces more constrained and linguistically plausible parse trees.





