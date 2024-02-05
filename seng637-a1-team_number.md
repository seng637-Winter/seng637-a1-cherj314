>   **SENG 637 - Dependability and Reliability of Software Systems**

**Lab. Report \#1 – Introduction to Testing and Defect Tracking 40%**

| Group: Group Number   6   |
|-----------------|
| Sean Temple          |   
| John Chernoff          	|   
| Nicholas Langley          	|   
| Raisa Mehjabin Azni           |   
| Eric Yoon            	|   

**Table of Contents**

(When you finish writing, update the following list using right click, then
“Update Field”)

[1 Introduction    1](#_Toc439194677)

This lab report outlines the strategies and approaches for verifying the functionality and reliability of an Automated Teller Machine (ATM) software system. The system is designed to handle transactions such as cash withdrawals, deposits, transfers, balance inquiries, and transaction aborts. It incorporates hardware components including a magnetic stripe reader, customer console (keyboard and display), envelope deposit slot, cash dispenser, printer, and a key-operated switch for machine control.

Prior to conducting this lab the team had limited knowledge of exploratory and manual testing except for one member who has work experience in testing. The team’s general understanding from lectures was that exploratory testing was a freestyle version of testing where the tester tries different actions on the system as they please in order to try and find potential bugs or errors. Whereas manual testing was understood to be based on following a rigid preconstructed test plan which ecompasses a series of test steps to be performed to check if the different parts of the system performed as predicted.

[2 High-level description of the exploratory testing plan    1](#_Toc439194678)

Test Types

The exploratory testing plan will primarily consist of unit tests on the individual components of the system such as the magnetic stripe reader and customer console. Each unit will be tested for both expected inputs and invalid inputs. Units will also be tested for edge case values such as zero or negative values. Once all units have been tested there will also be some system tests that include evaluating the entire ATM system’s functionality and its ability to perform under expected conditions. Stress tests will also be conducted to determine the system's ability to handle extreme conditions such as very large deposits or withdrawals.

All tests will be compared with the high level requirements provided in Appendix B in order to provide the expected outcome.

Scope of Testing

The first phase of testing will be functional testing to verify all of the buttons and interactions work. The features for functional testing include the magnetic strip reader, customer console, envelope deposit, cash dispenser, printer, key operated switch.

The next phase of testing is security testing which will include verifying that the machine accepts card, denies incorrect pin, accepts correct pin, and allows for multiple transactions with one pin entry.

The final phase of testing will be integration, performance, and usability testing to verify that withdrawals, deposits, transfers, balance inquiries work for all accounts and between all accounts.

Test Logistics 

The test environment will be simulated to mimic real-world ATM usage, including hardware components and a mock bank server. The test data includes valid and invalid card numbers, PINs, transaction amounts, and bank responses.

The team of five will be split up into two smaller groups to conduct the exploratory testing together. One group member will run the mouse and keyboard and physically conduct the tests, while the other group member will enter found bugs into Azure Devops. 

[3 Comparison of exploratory and manual functional testing  1](#_Toc439194679)
   
The exploratory and manual functional testing both was done on the ATM software system in this lab by two pairs of testers working on the same system simultaneously. There are some key differences and similarities between these two models.
 
The activity of the Exploratory Testing (ET) and Manual Functional Testing (MFT):
The Exploratory Testing (ET) was explicitly based on the exploration factor and the thorough evaluation of every step that currently exists in the system (version 1.0). With the exploratory approach, the functional testing of all the physical components (magnetic strip reader, customer console, envelope deposit, cash dispenser, printer, key-operated switch) and security testing (Valid and invalid PIN entry) have been intensively evaluated. The withdrawals, deposits, transfers, and balance inquiries for all accounts and interactions between accounts have also been verified which has potentially led to the discovery of a plethora of bugs and fails, as documented in a bug tracking tool (Azure DevOps) in this lab. In the Manual Functional Testing (MFT) of this system a structured test suite that includes information on, "Test Case #", "Use Case", "Function Being Tested", "Initial System State ","Input ", and "Expected Output" was being provided by the lab conductors to be followed by the testers. This test suit included most of the possible outcomes and scenarios of a potential user accessing the ATM services and its interaction with the designated bank. Exploratory testing is more adaptable and discovery-oriented, while manual functional testing is more systematic and specification-based.
 
The similarities:
In both test models (exploratory and manual functional), the main objective was to execute an effective testing session to find out the defects, ensure functionality, and verify the flexibility of the system for the user to practise. The tests were done by human testers to mimic human intervention for the real-time touch. The test sessions intensively focused on the functionality of the ATM system and its interaction with the bank on the back end. The log updates were verified in both test systems where similar defects were found when conducting version 1.0 of the system and were recorded concurrently. Both test models were conducted on a software version of the system which possibly had all the components needed to implement the system in a real-world environment, with physical components. The tests were done in a team collaboration which effectively enhanced the team communication pattern which eventually be fruitful in future lab sessions.
 
The difference:
In the Exploratory Test (ET) session, the testers (pairs 1 and 2) followed a dynamic approach where the test cases were found based on the ongoing observations of the tester team. On the other hand, in the Manual Functional Testing (MFT) session, a highly structured and well-documented test suite was followed to conduct the test session. The test suit included information regarding, "Test Case #", "Use Case", "Function Being Tested", "Initial System State", "Input", and "Expected Output". It was believed and trusted by the testers that this suit had all the possible scenarios that may have created a defect in the system execution from start to finish. The exploratory test system creates test cases, which are more holistic and can cover a wide range of functionalities that may occur in unexpected circumstances. Manual Functional Testing (MFT) more relies on the documentation of the tests, which may not portray the user experience accurately. In the Exploratory Testing (ET) session, the expected outcome is judged with real-life experience and rationality. In the Manual Functional Testing (MFT) session, the outcome of every test case is compared with a documented expected outcome mentioned in the provided test suit. A particular bug-fixing strategy should be implemented if the actual outcome is a defect but does not match the provided documentation of the expected outcome.

[4 Notes and discussion of the peer reviews of defect reports    1](#_Toc439194680)

Each pair in the team reviewed the defect reports created by the other pair and provided feedback which was implemented into the final versions of the defect reports. Overall both pairs were very detailed and caught a large amount of bugs which were documented through thorough defect reports. 

The first group could have benefitted from exploring more edge cases / abnormal inputs during exploratory testing. A lot of focus was on the main happy paths which overlapped with the scripted testing performed later, leading to redundancy in testing and reduced breadth. They could also have included information about the manual test script being followed in the report so it could be referred back to at a later date.

The second pair initially documented too many bugs resulting in overlapping or duplicated bugs which needed to be removed in later review. By investigating the root causes a bit more thoroughly the bugs could have been combined earlier, reducing clutter. They also could have had more detailed report titles to improve clarity. Details of the bugs initial state missing from the bug reports were also added.

The reports of both pairs could have been further improved with the inclusion of screenshots or videos of the bug in action. This would improve the clarity of the report and help to convey the details to any dev tasked with addressing it. The feature affected by each bug had to be added later for every report of both groups as well.

[5 How the pair testing was managed and team work/effort was
divided    1](#_Toc439194681)

The team was divided into two groups, one of two people and one of three people. Each of these groups completed the pair testing together for exploratory testing and manual scripted testing. Within the groups each individual had a role to either conduct the test or record the outcome of the test on Azure Devops. 

[6 Difficulties encountered, challenges overcome, and lessons
learned    1](#_Toc439194682)

It was difficult to coordinate the complex sequence of tasks among a large group, but through effective communication we were able to come together and work as a team to complete the assignment. We learned a lot about the software testing process and will make improvements to future bug reports and testing plans that we create. One large learning was that screenshots of bugs could be very helpful when revisiting bug reports after some time. 

The lab was a great exercise from which we learned a lot. The lab document itself was perhaps a bit too long and was difficult to read at first. We think that shortening the document and summarising some of the information within could make it more digestible in a short period of time. 

