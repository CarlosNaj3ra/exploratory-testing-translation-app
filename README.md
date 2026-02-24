# exploratory-testing-translation-app
Lexical Corruption in EN → ES Translation with Punctuation Handling

Overview

During exploratory testing of a mobile translation application developed by Apple Inc., an inconsistency was identified when translating specific English inputs into Spanish.

The anomaly appears when exclamation marks are present in the input.

Objective

Evaluate translation consistency when punctuation marks are attached to English input tokens.

-----------------------------------------------------------------------------------------------------

Testing Methodology

Input variations tested:

- Single-word input

- Word + exclamation mark

- Word + space + exclamation mark

- Multi-word sentences ending with exclamation mark

- Comparative testing across conditions

------------------------------------------------------------------------------------------------------

- Testing approach:

- Exploratory Testing

- Input Variation Strategy

- Pattern Analysis


| Input  | Output | Observation |
| ------------- | ------------- | -------------- |
| Listen  | Escuchar  | Correct |
| Listen!  | ¡Estucha!  | Invalid Spanish word |
| Listen !  | ¡Encucha!  | Invalid Spanish word |

------------------------------------------------------------------------------------------------------
Expected Behavior

The system should generate valid Spanish translations such as:

¡Escucha!

Non-existent lexical forms should not be produced.


<img width="200" height="400" alt="IMG_1262" src="https://github.com/user-attachments/assets/14faad5b-e8c3-4292-85f1-5b7cd8ca69cf" />
<img width="200" height="400" alt="IMG_1263" src="https://github.com/user-attachments/assets/cb893fc9-12e2-4c65-ab40-e98e58a529cf" />

------------------------------------------------------------------------------------------------------
Technical Hypothesis

The behavior suggests a potential inconsistency in tokenization or punctuation preprocessing within the translation pipeline.

The issue appears sensitive to punctuation placement (attached vs separated).

Impact Assessment

- Affects translation accuracy

- Reduces linguistic reliability

- May impact user trust

Severity assessment: Medium (functional accuracy issue)

Conclusion

The issue is reproducible and context-sensitive.
It appears specifically when exclamation marks are present in English input.

This case highlights the importance of punctuation-aware token processing in translation systems.




