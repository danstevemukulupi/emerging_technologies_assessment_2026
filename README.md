
# EMERGING TECHNOLOGIES ASSESSMENT 2026

###  STEP 1: CLONING THE PROJECT

git clone https://github.com/danstevemukulupi/emerging_technologies_assessment_2026.git
cd emerging_technologies_assessment_2026

Install

 pip install python
 pip install -r requirements.txt
 jupyter notebook
 python -m venv .venv




Classical to Quantum: From Boolean Functions to Deutsch–Jozsa Algorithm

This project presents a step-by-step progression from classical computation to quantum algorithms, culminating in the implementation of both Deutsch’s Algorithm and the Deutsch–Jozsa Algorithm using Qiskit.

The primary goal is to explore how quantum computation leverages superposition and interference to determine global properties of Boolean functions more efficiently than classical approaches.


Overview of Problems
  Problem 1: Generating Classical Boolean Functions

We began by constructing a Python function capable of generating random Boolean functions with four inputs. Each function was guaranteed to be either:

Constant (same output for all inputs), or
Balanced (equal number of 0s and 1s)

This established the black-box (oracle) model, where:

The internal structure of the function is unknown
Only input-output queries are allowed


Problem 2: Classical Computational Cost

Next, we analysed the classical complexity of determining whether a function is constant or balanced.

For a function with 4 inputs → 2
4
=16 possible inputs
In the worst case, all inputs must be evaluated

  This highlights a fundamental limitation of classical computation:

Global properties cannot be determined without sufficient local evaluations.

Problem 3: Quantum Oracles

We then introduced the quantum model by constructing reversible quantum oracles for Boolean functions.

A quantum oracle is defined as:

∣x⟩∣y⟩→∣x⟩∣y⊕f(x)⟩

Key properties:

Reversible (unitary) transformation
Encodes classical logic into quantum circuits
Forms the foundation for quantum algorithms

This step bridges classical computation → quantum computation.



Problem 4: Deutsch’s Algorithm

We implemented Deutsch’s Algorithm, which solves the problem for a single-bit input function.

  Key Insight:

Using quantum mechanics, we can evaluate the function for both inputs simultaneously.

How it works:
Prepare a superposition of inputs using Hadamard gates
Apply the oracle
Use interference to extract global information
  Result:
Constant function → output 0
Balanced function → output 1

 Only one oracle query is required.

This demonstrates a clear quantum advantage over classical methods.



Problem 5: Deutsch–Jozsa Algorithm

Finally, we extended the approach to the multi-bit case using the Deutsch–Jozsa Algorithm.

Handles functions with multiple input bits (e.g., 4 inputs)
Uses multi-qubit superposition
Applies the oracle once
 Outcome:
Correctly classifies functions as constant or balanced
Requires only one evaluation, regardless of input size

Artificial Intelligence Tools Used

The following AI tools were used to support development, debugging, and documentation throughout this project:

1. ChatGPT

Assisted with conceptual explanations of quantum computing topics
Helped improve clarity and structure of written content
Provided code suggestions and refactoring guidance
Supported comparison between original implementations and improved versions
Simplified complex ideas into more understandable explanations

2. Claude

Used for cross-checking solutions and validating logic
Helped review and verify code correctness and explanations
Provided an additional layer of quality assurance

3. GitHub Copilot (via Visual Studio Code)

Assisted in identifying syntax errors and missing dependencies
Helped resolve runtime issues and debugging problems
Provided inline code suggestions to improve efficiency
Supported general code completion and polishing

