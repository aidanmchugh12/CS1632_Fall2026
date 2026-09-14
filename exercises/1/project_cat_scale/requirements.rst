Requirements
============

This is the requirements specification.  It is organized in 3 levels:
proj->req->spec.  The ``.. proj::`` block describes the project.  The ``..
req::`` block is a requirement linked to a project that describes a user need
in a language intended for users.  The ``.. spec::`` block is a specification
linked to a requirement that details verifiable system behavior for each
equivalence class of the requirement in a language intended for developers and
testers.

.. proj:: Cat Scale
   :id: PROJ_001

   This system determines whether your cat is overweight, underweight, or just right.

.. req:: Cat name prompt
   :id: REQ_001
   :requiredby: PROJ_001

   At launch, the system shall ask the user the name of the cat and wait for input.

.. req:: Valid cat name
   :id: REQ_002
   :requiredby: PROJ_001

   If cat name is longer than 10 characters, the system shall ask the user to try again with a shorter name and shut down. Otherwise, the system shall proceed to the next step.

.. req:: Cat weight prompt
   :id: REQ_003
   :requiredby: PROJ_001

   After cat name is entered, the system shall ask the user the weight of the cat and wait for input.

.. req:: Valid cat weight
   :id: REQ_004
   :requiredby: PROJ_001

   If cat weight is invalid, the system shall ask the user to try again with a valid weight and shut down..  Otherwise, the system shall proceed to the next step.

.. req:: Display verdict
   :id: REQ_005
   :requiredby: PROJ_001

   After the cat's weight is entered, the system shall display the verdict for the cat depending on its weight.

.. spec:: Valid cat name entered into prompt
   :id: SPEC_001
   :specifies: REQ_002, REQ_003, REQ_001

   If provided name is no longer than 10 characters, including names containing punctuation, the system shall ask the user the weight of the cat and wait for input.

.. spec:: Invalid cat weight
   :id: SPEC_002
   :specifies: REQ_004

   If the provided weight is not an integer, the system shall ask the user to try again with a valid weight and shut down.

.. spec:: Invalid cat name
   :id: SPEC_006
   :specifies: REQ_002

   If the provided name is longer than 10 characters, the system shall ask the user to try again with a shorter name and shut down.

.. spec:: Valid cat weight
   :id: SPEC_007
   :specifies: REQ_004

   If the provided weight is an integer, the system shall determine and display the cat's weight verdict.

.. spec:: Cat is underweight
   :id: SPEC_003
   :specifies: REQ_005

   If the cat's weight is 4 or less, the system shall print "[NAME] is underweight." and shut down.

.. spec:: Cat is normal weight
   :id: SPEC_004
   :specifies: REQ_005

   If the cat's weight is between 5 and 25 inclusive, the system shall print "[NAME] is normal weight." and shut down.

.. spec:: Cat is overweight
   :id: SPEC_005
   :specifies: REQ_005

   If the cat's weight is 26 or above, the system shall print "[NAME] is overweight." and shut down.


   



   