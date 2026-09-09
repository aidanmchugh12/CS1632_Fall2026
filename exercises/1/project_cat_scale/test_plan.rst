Test Plan
=========

This is the test plan document.  Each test case is a ``.. test::`` block.
``:tests:`` names the specification(s) it verifies (comma-separated). That link
is what creates the traceability -- the matrix is built from it, so a test with
no ``:tests:`` is an orphan and a specification nobody links to is uncovered.

.. test:: System determines aidan is a valid cat name
   :id: TEST_001
   :tests: SPEC_001

   **Preconditions**: 
   = The catscale.jar file is installed in the system.
   - Java 11 is installed on the machine.

   **Execution Steps**:

   1. Open a shell and cd to the folder where potus.jar is located.
   2. Run: "java -jar catscale.jar"
   3. System prompts for the name of your cat
   4. Input: "aidan"

   **Postconditions**:

   - The system prompts for the weight of the cat.

.. test:: System determines hi is not a valid cat weight
   :id: TEST_002
   :tests: SPEC_002

   **Preconditions**: 
   = The catscale.jar file is installed in the system.
   - Java 11 is installed on the machine.

   **Execution Steps**:

   1. Open a shell and cd to the folder where potus.jar is located.
   2. Run: "java -jar catscale.jar"
   3. System prompts for the name of the cat
   4. Input: "aidan"
   5. System prompts for weight of the cat
   6. Input: "hi"

   **Postconditions**:

   - The system asks to user to try again with a shorter name.