Test Plan
=========

This is the test plan document.  Each test case is a ``.. test::`` block.
``:tests:`` names the specification(s) it verifies (comma-separated). That link
is what creates the traceability -- the matrix is built from it, so a test with
no ``:tests:`` is an orphan and a specification nobody links to is uncovered.

.. test:: System warns user when no argument is passed
   :id: TEST_001
   :tests: SPEC_002

   **Preconditions**: 
   = The potus.jar file is installed in the system.
   - Java 11 is installed on the machine.

   **Execution Steps**:

   1. Open a shell and cd to the folder where potus.jar is located.
   2. Run: "java -jar potus.jar"

   **Postconditions**:

   - The system informs the user that a command line argument is needed.

.. test:: System determines age 34 is too young to be POTUS
   :id: TEST_002
   :tests: SPEC_006

   **Preconditions**: 
   = The potus.jar file is installed in the system.
   - Java 11 is installed on the machine.

   **Execution Steps**:

   1. Open a shell and cd to the folder where potus.jar is located.
   2. Run: "java -jar potus.jar 34"

   **Postconditions**:

   - The system prints "34 is too young to be POTUS".

.. test:: System determines POTUS eligibility using a single intger argument
   :id: TEST_003
   :tests: SPEC_001

   **Preconditions**: 
   = The potus.jar file is installed in the system.
   - Java 11 is installed on the machine.

   **Execution Steps**:

   1. Open a shell and cd to the folder where potus.jar is located.
   2. Run: "java -jar potus.jar 34"

   **Postconditions**:

   - The system determines POTUS eligibility.

.. test:: System informs user when more than one argument is passed
   :id: TEST_004
   :tests: SPEC_003

   **Preconditions**: 
   = The potus.jar file is installed in the system.
   - Java 11 is installed on the machine.

   **Execution Steps**:

   1. Open a shell and cd to the folder where potus.jar is located.
   2. Run: "java -jar potus.jar 34 34"

   **Postconditions**:

   - The system informs the user that there needs to be exactly 1 command line argument.

.. test:: System informs user command line argument needs to be an integer
   :id: TEST_005
   :tests: SPEC_004

   **Preconditions**: 
   = The potus.jar file is installed in the system.
   - Java 11 is installed on the machine.

   **Execution Steps**:

   1. Open a shell and cd to the folder where potus.jar is located.
   2. Run: "java -jar potus.jar hi"

   **Postconditions**:

   - The system informs the user that the command line argument needs to be an integer.

.. test:: System determines age 35 is old enough to be POTUS
   :id: TEST_006
   :tests: SPEC_005

   **Preconditions**: 
   = The potus.jar file is installed in the system.
   - Java 11 is installed on the machine.

   **Execution Steps**:

   1. Open a shell and cd to the folder where potus.jar is located.
   2. Run: "java -jar potus.jar 35"

   **Postconditions**:

   - The system prints "35 is old enough to be POTUS".