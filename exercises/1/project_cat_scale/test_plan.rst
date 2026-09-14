Test Plan
=========

This is the test plan document.  Each test case is a ``.. test::`` block.
``:tests:`` names the specification(s) it verifies (comma-separated). That link
is what creates the traceability -- the matrix is built from it, so a test with
no ``:tests:`` is an orphan and a specification nobody links to is uncovered.

.. test:: System determines a valid cat name and normal weight
   :id: TEST_BASE
   :tests: SPEC_001, SPEC_004, SPEC_007

   **Preconditions**:

   - The catscale.jar file is installed in the current folder.
   - Java 11 is installed on the machine.

   **Execution Steps**:

   1. Open a shell and cd to the folder where catscale.jar is located.
   2. Run: "java -jar catscale.jar"
   3. System prompts for the name of your cat
   4. Input: "Aidan"
   5. System prompts for the weight of the cat
   6. Input: "10"

   **Postconditions**:

   - The system determines that the cat has normal weight.
   - The system prints "Aidan is normal weight."
   - The system shuts down.

.. test:: System accepts a ten-character cat name and a boundary weight
   :id: TEST_EDGE
   :tests: SPEC_001, SPEC_003, SPEC_007

   **Preconditions**:

   - The catscale.jar file is installed in the current folder.
   - Java 11 is installed on the machine.

   **Execution Steps**:

   1. Open a shell and cd to the folder where catscale.jar is located.
   2. Run: "java -jar catscale.jar"
   3. System prompts for the name of the cat
   4. Input: "Alexandria"
   5. System prompts for the weight of the cat
   6. Input: "4"

   **Postconditions**:

   - The system prints "Alexandria is underweight."
   - The system shuts down.

.. test:: System rejects an invalid cat name
   :id: TEST_003
   :tests: SPEC_006

   **Preconditions**:

   - The catscale.jar file is installed in the current folder.
   - Java 11 is installed on the machine.

   **Execution Steps**:

   1. Open a shell and cd to the folder where catscale.jar is located.
   2. Run: "java -jar catscale.jar"
   3. System prompts for the name of the cat
   4. Input: "Aidan123"

   **Postconditions**:

   - The system asks the user to try again with a shorter name.
   - The system shuts down.

.. test:: System terminates on a non-integer cat weight
   :id: TEST_004
   :tests: SPEC_002

   **Preconditions**:

   - The catscale.jar file is installed in the current folder.
   - Java 11 is installed on the machine.

   **Execution Steps**:

   1. Open a shell and cd to the folder where catscale.jar is located.
   2. Run: "java -jar catscale.jar"
   3. System prompts for the name of the cat
   4. Input: "Aidan"
   5. System prompts for the weight of the cat
   6. Input: "hi"

   **Postconditions**:

   - The system terminates.
   - The system displays a Java InputMismatchException stack trace.

.. test:: System determines an overweight cat
   :id: TEST_005
   :tests: SPEC_005, SPEC_007

   **Preconditions**:

   - The catscale.jar file is installed in the current folder.
   - Java 11 is installed on the machine.

   **Execution Steps**:

   1. Open a shell and cd to the folder where catscale.jar is located.
   2. Run: "java -jar catscale.jar"
   3. System prompts for the name of the cat
   4. Input: "Aidan"
   5. System prompts for the weight of the cat
   6. Input: "26"

   **Postconditions**:

   - The system prints "Aidan is overweight."
   - The system shuts down.