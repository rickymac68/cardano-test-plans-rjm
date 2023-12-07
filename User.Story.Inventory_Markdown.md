# User Story Inventory

# 

# Document Summary

Upon socialising of this Inventory, and eventual agreement, we will progress to detailing how the Acceptance will be accomplished and signoff achieved, the ‘Accepted’ column will be marked Yes once consensus is reached.

# Change Management

Upon agreement on the User Story Inventory, a suitable level of Change Management will be applied, this will enable us to phase-deliver Governance on Cardano and to fulfil the ongoing Ecosystem and Community needs. Additional User Stories will be proposed, reviewed, approved and accepted using

# 

# Source Areas Under Consideration

# 

# This section shows the areas or sources thus far

# 

# 

| Source | Outline Contribution | State | Key Contract |
| --- |  --- |  --- |  --- | 
| Voltaire | Use Cases for Governance, voting, delegation | Initial Capture Complete | Outreach in progress |
| CIP-1694 | Blockchain level User Stories on voting, delegation, identity, consensus | Initial Capture Complete | Outreach in progress |
| Smart Contracts | Plutus v3 and BLS | Initial Capture Complete | Outreach in progress |
| CLI-API | Interface outline and definition  | Initial Capture Complete | Outreach in progress |
| Sidechains | Interaction with BLS primitives | Outreach in progress | Outreach in progress |
| DApps | To be defined and elaborated | To be defined | Outreach in progress |
| Exchanges | To be defined and elaborated | To be defined | Outreach in progress |
| Other | To be defined and elaborated | To be defined | Outreach in progress |

# 

# User Story (Voltaire, API, CIP-1694, Community et al)

# 

| UID | User Story | Functional Requirement | Acceptance Criteria | Link | Accepted | Source | Enabler(Y,N) |
| --- |  --- |  --- |  --- |  --- |  --- |  --- |  --- | 
| CH.VO1 | As a DRep or Ada Holder I want to connect my wallet to GovTool so that I can post transactions on-chain | Connect with multiple stake key wallet | Given I am on the homepage with no wallet connected.
When I click the Connect Wallet button 
Then a modal window opens showing my CIP-95 compatible wallets 
When I select a wallet with multiple stake keys from this list
Then I am asked which stake key I wish to connect with
When I select a stake key 
Then the wallet opens and I can connect with it on the selected stake key. | pending |  | Voltaire | N |
|  |  |  | Given I am on the homepage without my wallet connected
When I click the Connect Wallet button
Then I am not shown any non CIP-95 compatible wallets.  | pending |  | Voltaire | N |
|  |  |  | Given I am on the homepage without my wallet connected
When I click the Connect Wallet button and select a CIP-95 compliant, multiple stake key wallet, containing zero ADA (or tADA for SanchoNet)
Then a modal window opens showing my CIP-95 compatible wallets 
When I select a wallet with multiple stake keys from this list
Then I am asked which stake key I wish to connect with
When I select a stake key 
Then the wallet opens and I can connect with it on the selected stake key. | pending |  | Voltaire | N |
|  |  |  | Given i am on the homepage without my wallet connected
When I click the Connect Wallet button and select a CIP-95 compliant, single stake key wallet, containing more than zero ADA (or tADA for SanchoNet)
Then a modal window opens showing my CIP-95 compatible wallets 
When I select a wallet with multiple stake keys from this list
Then I am asked which stake key I wish to connect with
When I select a stake key 
Then the wallet opens and I can connect with it on the selected stake key. | pending |  | Voltaire | N |
|  |  | Connect with single stake key wallet | Given I am on the homepage with no wallet connected

When I click the Connect Wallet button and select a CIP-95 compliant single stake key wallet 

Then my wallet appears and I can connect with it | pending |  | Voltaire | N |
|  |  |  | Given I am on the homepage without my wallet connected

When I click the Connect Wallet button

Then I am not shown any non CIP-95 compatible wallets.  | pending |  | Voltaire | N |
|  |  |  | Given I am on the homepage without my wallet connected

When I click the Connect Wallet button and select a CIP-95 compliant, single stake key wallet, containing zero ADA (or tADA for SanchoNet)

Then my wallet appears and I can connect with it | pending |  | Voltaire | N |
|  |  |  | Given I am on the homepage without my wallet connected

When I click the Connect Wallet button and select a CIP-95 compliant, single stake key wallet, containing more than zero ADA (or tADA for SanchoNet)

Then my wallet appears and I can connect with it | pending |  | Voltaire | N |
|  |  | Disconnect wallet | Given that I am on the dashboard with my wallet connected

If I click the Disconnect button

Then my wallet is disconnected from GovTool and I am redirected to the homepage. | pending |  | Voltaire | N |
|  |  |  | Given that I am connected to GovTool with my wallet 

When I disconnect 

Then I will be redirected to the homepage, and will not have access to delegation or voting features. | pending |  | Voltaire | N |
|  |  | Check the wallet is on the correct network | Given I am on the homepage
When I compare the networkId with the environment value set on the deployment for the network.
Then if there are exceptions raised, fail the test.
If no exceptions, connect the wallet to the network (pass) | pending |  | Voltaire | N |
| CH.VO2 | As an Ada Holder I want to delegate my voting power to a DRep so that I can claim my staking rewards | Delegate to DRep ID | Given that I have my wallet connected, and am on the Delegate to DRep page
When I select the delegate to DRep ID option and I enter a DRep ID which has not been registered and I press delegate
Then I will be presented with an error message explaining that the DRep ID was not found. | pending |  | Voltaire | N |
|  |  |  | Given that I have my wallet connected, and am on the delegate to DRep page,
When I choose the Delegate to DRep ID option and I enter a registered DRep ID and I press the Delegate button 
Then I am able to delegate to that DRep ID via my connected wallet | pending |  | Voltaire | N |
|  |  |  | Given that I have connected to GovTool with zero* ADA (or tADA in the case of SanchoNet)
When I choose the Delegate to DRep ID option and I enter a registered DRep ID and I press the Delegate button 
Then I am presented with a warning message and cannot proceed with delegation. 
*or at least a number below transaction costs | pending |  | Voltaire | N |
|  |  | Access Delegate to DRep page | Given that I do not have a compatible wallet connected to GovTool
When I attempt to visit the URL of the Delegate to DRep page
Then I am redirected to the homepage | pending |  | Voltaire | N |
|  |  |  | Given that I  have a compatible wallet connected to GovTool and I am looking at the dashboard
When I click on the the Delegate button (or Change Delegation button if you are already registered) 
Then I am shown the Delegate to DRep page | pending |  | Voltaire | N |
|  |  | Verify DRep behaviour in connected state  | Given that I'm not connected to the wallet
When I visit the DRep delegation page, and I click the delegate-connect-wallet-button
 Then the connect your wallet-modal is visible | pending |  | Voltaire | N |
|  |  | Verify DRep behaviour in disconnected state | Given that I have a preset dRep wallet loaded
Then Delegate button is clicked
Then it is expected that delegation options card is visible
delegate to myself is expected to be visible
Then Other options is clicked
Expect that signal no confidence card and vote abstain cards are visible 
Next, delegate to dRep card is clicked, followed by next step button
Then expected that dRep ID input is visible along with delegate button | pending |  | Voltaire | N |
|  |  | Delegate to myself | Given that I am a registered DRep who is connected to GovTool with my wallet, and I am on the Delegate to DRep page 
When I choose the Delegate to DRep ID option and I enter my own DRep ID and I press the Delegate button 
Then I am able to delegate to myself via my connected wallet | pending |  | Voltaire | N |
|  |  |  | Given that I am a registered DRep who is connected to GovTool with my wallet, and I am on the Delegate to DRep page 
When I select the Delegate to Myself option and press the Delegate button 
Then I will be able to send a transaction to delegate to myself via my wallet | pending |  | Voltaire | N |
|  |  |  | Given that I am not a registered DRep, and I am connected to GovTool with my wallet,
When I am on the Delegate to DRep page
I cannot see a Delegate to Myself option  | pending |  | Voltaire | N |
|  |  | Change my DRep delegation | Given that I am I am already delegated to a DRep
When I look at the dashboard 
GovTool will know that I am delegated and  will invite me to “change my delegation” rather than to delegate.  | pending |  | Voltaire | N |
|  |  |  | Given that I am already delegated 
When I go to change my delegation
I can delegate to any registered DRep, If I am delegated to myself then the option to “delegate to myself” will not be shown, If I am delegated to a specific predefined DRep then this predefined option will not be shown. | pending |  | Voltaire | N |
|  |  | Check the validity of a DRep ID | Given that I have selected the “delegate to a DRep ID” option in the delegation user journey.
When I enter anything in the  DRep ID input box that is not a registered DRep ID. 
Then I will not be able to delegate to this DRep ID and will get a warning message. | pending |  | Voltaire | N |
|  |  | Delegate to Abstain | Given that I am a DRep 
When I delegate using the “delegate to abstain” feature 
Then it will only delegate my own lovelace’s voting power to Abstain and NOT the voting power (if any) that has been delegated to me by others.  I will be notified that my delegation translation was sent. | pending |  | Voltaire |  |
|  |  |  | Given that I am not a DRep
When I delegate using the “delegate to abstain” feature 
Then it will delegate any voting power I have to Abstain. I will be notified that my delegation translation was sent. | pending |  |  |  |
|  |  | Delegate to No-Confidence | Given that I am a DRep 
When I delegate using the “delegate to no-confidence” feature 
Then it will only delegate my own lovelace’s voting power to No-Confidence and NOT the voting power (if any) that has been delegated to me by others.  I will be notified that my delegation translation was sent. | pending |  | Voltaire |  |
|  |  |  | Given that I am not a DRep
When I delegate using the “delegate to no-confidence” feature 
Then it will delegate any voting power I have to No-Confi. I will be notified that my delegation translation was sent. | pending |  | Voltaire |  |
|  |  | Guardrails for Voltaire  | This work is in progress | pending |  | Voltaire |  |
| CH.VO3 | As a DRep I want to register so that I can vote on governance actions | Register as a DRep | Given that I am connected to GovTool with a compatible wallet
When I go through the DRep registration process, and do not include a metadata anchor  
Then I can register as a DRep via my wallet (because metadata anchors are optional) | pending |  | Voltaire | N |
|  |  |  | Given that I am connected to GovTool with a compatible wallet
When I go through the DRep registration process, and include metadata anchor information in the wrong format 
Then I will not be able to progress further in the process and I will be told that it is because the format is incorrect. | pending |  | Voltaire | N |
|  |  |  | Given that I am connected to GovTool with a compatible wallet
When I go through the DRep registration process, and include metadata anchor information in the correct format 
Then I will be able to register as a DRep via my wallet, GovTool will include the metadata anchor in the registration certificate transaction. | pending |  | Voltaire | N |
|  |  | Confirm transaction has been sent | Given that I have gone through the DRep registration process 
When I press the button on my wallet to submit the transaction 
Then I will receive a confirmation message from GovTool that will include a link to the transaction in a block explorer. | pending |  | Voltaire | N |
|  |  | Status of transaction is displayed | Given that I have just submitted a DRep registration transaction, and I am looking at the dashboard 
When the registration has not yet been confirmed by the blockchain, 
Then the registration status will show as “In Progress” until it is confirmed. | pending |  | Voltaire | N |
| CH.VO4 | As a DRep I want to vote so that I can fulfil my role | Should be able to access the governance actions page as a DRep with my wallet connected | Given that I am a DRep and I am connected to GovTool
When I visit the url of the governance actions page 
Then the governance actions page is displayed | pending |  | Voltaire | N |
|  |  |  | Given that I am a DRep and connected to GovTool
When I look at the governance actions page 
Then my voting power is displayed | pending |  |  |  |
|  |  |  | Given that I am a DRep and Connected to GovTool, and I am on the governance actions page
When I click Disconnect Wallet
Then my wallet is disconnected and I am redirected to the same page, but without the DRep functionality (i.e. ability to vote) | pending |  |  |  |
|  |  |  | Given that I am a DRep and I am on the governance actions page 
When I click on the “view proposal details” button
Then I will be shown the page for that individual governance action and be able to view its details  | pending |  |  |  |
|  |  | A DRep should be able to vote on a live governance action | Given that I am a DRep 
When I look at the details page of an individual governance action 
Then I can see how many votes the governance action currently has for, against and abstaining. | pending |  | Voltaire | N |
|  |  |  | Given that I am a DRep
When I look at the details page of an individual governance action 
Then there are buttons allowing me to vote for, against or abstain. | pending |  |  |  |
|  |  |  | Given that I am a DRep, on the details page of an individual governance action
When I select yes/ no/ abstain, and click vote 
Then I can sign & submit this vote via my wallet | pending |  |  |  |
|  |  |  | Given that I am a DRep
When I have submitted a vote 
Then Immediately after this GovTool will display a message informing me that my transaction has been sent and providing me with a link to a block explorer where I can view the transaction | pending |  |  |  |
|  |  | People without the (t)ADA needed to pay for voting transactions should not be able to submit a voting transaction | Given I have less Lovelace in my wallet than a transaction costs
When I attempt to vote
The GovTool will tell me that there is an error | pending |  | Voltaire | N |
|  |  | People without their wallet connected or who do have their wallet connected but have not registered as DReps should not be able to vote | Given that I do not have a wallet connected to GovTool
When I visit the details of a governance action
Then I am not shown a vote button. | pending |  | Voltaire | N |
|  |  | No one should be able to vote on a governance action that has expired, or been ratified, or enacted.  | Given that I am on the governance action page
When I examine the governance actions
None of the governance actions shown on the page have expired or been ratified or enacted. | pending |  | Voltaire | N |
|  |  | A DRep should be able to change their vote  | Given that I am a DRep and I have already voted on a given governance action 
When I submit a different vote for the same transaction within the same snapshot 
Then the most recent vote will be counted. | pending |  | Voltaire | N |
|  |  |  | Given that I have already cast a vote on a governance action 
When I examine this specific governance action’s page
Then I can  see that I have already voted and what my most recent vote was | pending |  |  | N |
|  |  |  | Given that I have already cast a vote on a given governance action
When I examine this specific governance action’s page
Then instead of seeing a “vote” button I should see a “change vote” button | pending |  | Voltaire | N |
|  |  | Only the votes of participants who are still DReps at the relevant epoch boundary will be accepted | Given that I am a DRep and I vote yes or abstain on a live governance action.
At the epoch boundary
My votes are counted. | pending |  | Voltaire | N |
|  |  |  | Given that I was a DRep that voted yes or abstain on a live governance action but then retired.
At the next epoch boundary
My votes will not be counted towards the total tally of DRep votes. | pending |  | Voltaire | N |
|  |  | DReps can attach a metadata anchor to their votes | Given that I have chosen how to vote on the UI of a governance action’s details

When I add a metadata anchor to the UI also and click the vote button 

Then the resulting transaction will include my metadata anchor | pending |  | Voltaire | N |
| CH.VO5 | As a DRep I want to retire so that I can reclaim my DRep Deposit | Only a user who is registered as a DRep can retire  | Given that I am not registered as a DRep, 
When I look for a retirement option in GovTool 
Then there is none. | pending |  | Voltaire | N |
|  |  |  | Given that I am registered as a DRep, 
When I look for a retirement option in GovTool there is one. And when I choose this option
Then my wallet opens and I can sign a retirement action which is registered on-chain. | pending |  |  |  |
|  |  | When I retire I get my deposit back | Given that I am a DRep
When I register a valid retirement transaction on chain
then my DRep registration deposit will be returned to me.  | pending |  |  | N |
|  |  | Only a user who has the wallet that they registered as a DRep with can retire.  | Given that I am not connected to GovTool 
When I look at the homepage
Then I will not see an option to retire | pending |  | Voltaire | N |
|  |  |  | Given that I am connected to GovTool with an account that is not associated with a registered DRep certificate
When I look at the homepage 
Then I see an option to register as a DRep | pending |  | Voltaire | N |
|  |  |  | Given that I am a registered DRep with my wallet account connected

When I click the retire as a DRep option on the homepage and then send the retirement transaction with my wallet

Then the blockchain will register my retirement certificate, and I will be retired.  | pending |  | Voltaire | N |
| CH.VO6 | As a DRep I want to update my details so that I can better advertise myself to Ada Holders  | A DRep can update their registration after registering | Given that I am a DRep and am connected to GovTool and am on the dashboard.
Then when I click the “change metadata” button on the DRep tab.
Then I am directed to update my metadata and can submit a DRep update certificate to register this on-chain. | pending |  | Voltaire | N |
| CH.VO7 | As any user I want to view governance actions so I can see what is being proposed | Anyone should be able to access the governance actions page without a wallet connected | Given that I am on the GovTool homepage, 
When I click the “Governance actions” in the topbar 
Then I am sent to the governance actions page.  | pending |  | Voltaire | N |
|  |  | I can see all live governance actions | Given that I am on the Governance Actions page 
When I review the governance actions available to view on the page, 
Then all of the non expired/ ratified/enacted governance actions. | pending |  | Voltaire | N |
|  |  | Anyone with a CIP-95 compatible wallet connected should be able to access the governance actions page | Given that I am on the GovTool dashboard, 
When I click the View Governance Actions tab, or “Governance actions” in the sidebar 
Then I am sent to the governance actions page.  | pending |  | Voltaire | N |
|  |  | Should be able to see if a governance action has been accepted or rejected by the Constitutional Committee | Given that I am looking at an individual governance action, When I look at how many votes it has, it shows the number of CC votes and whether this is acceptance/veto or neither.  | pending |  | Voltaire | N |
|  |  | Should be able to view relevant information about governance actions | Given that I am looking at a Treasury Withdrawal governance action then I can see the amount of ADA that the proposal submitter wants to withdraw, and the address that they want to withdraw it to.  | pending |  | Voltaire | N |
|  |  |  | Given that I am looking at a Proposal Parameter Change governance action, then I can see the parameter(s) that the Proposal Submitter is proposing to change along with what the current values are, and what he wants to change them to.  | pending |  |  |  |
|  |  |  | Given that I am looking at a Constitutional Committee Update governance action, I can see the following (where applicable):
- Old Committee Member Cold Key Hash to be removed
- Float, (a rational number in the range from 0 to 1 inclusive. Of course if all you have in a tool is Floats, than that is what it will have to be)
- Map of committee cold key credentials that will be added to the committee with absolute epoch number number when they will expire | pending |  |  |  |
|  |  |  | Given that I am looking at an Update to the Constitution governance action I should be able to see:
- The Constitution URL
- The Constitution hash
- The proposal policy script (if provided when the governance action was submitted) | pending |  |  |  |
|  |  |  | Given that I am looking at a Hard Fork Initiation governance action then I should be able to see:
- The new major protocol version | pending |  |  |  |
|  |  | The governance action as displayed should include a link to its metadata  | Clicking the “view other details” link on the governance action details page will prompt a warning, and will ask if you want to continue. If you continue the external url will open in a new tab. | pending |  | Voltaire | N |
|  |  |  | The warning will explain that you are visiting an external link and will show you the url of the governance action will be displayed | pending |  | Voltaire | N |
|  |  | Verify the integrity of a governance action’s metadata | Given that I am looking at a governance action then I can see whether a hash of that governance action’s metadata matches the metadata hash included in the anchor. | pending |  | Voltaire | N |
| CH.VO8 | As a potential Constitutional Committee Member I want to become a Constitutional Committee Member so that I can vote on the corresponding governance actions | Create a set of keys  | Given that I have the CLI open in front of me, when I run the corresponding command, then I can verify that I have created a new key pair | pending |  | Voltaire | N |
|  |  | Include these keys in a New Committee Cold Key Hash or Script Hash | Given that I am using CLI and I have created my set of keys, when they are registered in the ledger, then I can verify that my set of keys corresponds to a CC member | pending |  | Voltaire | N |
|  |  | Create an authorization certificate | Given that I am using CLI and I have created my set of cold/hot key pairs, when I run the corresponding command, then I can verify that the certificate is stored on-chain and it delegates rights from the cold key to the hot key | pending |  | CIP-1694
L993 | N |
|  |  | Only votes from active Committee members are considered.  | Given that my set of keys does not correspond to an active CC member, when I try to vote as a CC member using CLI, then I get an error message telling me that my credentials are not valid | pending |  | CIP-1694
L993 | N |
| CH.VO9 | As a CC Member I want to review a governance action so that I can scrutinise whether or not it is aligned with the Constitution | Access GovTool

 | Given that I am on the GovTool homepage, when I click the “Governance actions” in the topbar then I am sent to the governance actions page.  | pending |  | Voltaire | N |
|  |  | See list of current governance actions | Given that I am on the Governance Actions page When I review the governance actions available to view on the page, then all of the non expired/ ratified/enacted governance actions. | pending |  | Voltaire | N |
|  |  | See details of a specific governance action | Given that I am on the Governance Actions page, When I click on an individual governance action, Then I can see the relevant information | pending |  | Voltaire | N |
|  |  | See metadata | Given that I am looking at an individual governance action page, when I click on “view other details” and I click on continue in the warning message, Then an external url will open in a new tab. | pending |  | Voltaire | N |
|  |  | Verify metadata integrity | Given that I am looking at a governance action then I can see whether a hash of that governance action’s metadata matches the metadata hash included in the anchor. | pending |  | Voltaire | N |
| CH.VO10 | As a CC Member I want to vote on a governance action so that I can approve governance actions that align with the constitution | Find a specific governance action using CLI
 | Given that I am using CLI and I know the governance action ID, When I run the command to review a specific governance action, Then I can see the details of that individual governance action. | pending |  | Voltaire | N |
|  |  | Vote as a Constitutional Committee member using CLI | Given that I am using CLI and I know the governance action ID, When I build the transaction to vote on a governance action, Then I can specify my role (ccm), the action ID, and the intent to vote (YES/NO/ABSTAIN) | pending |  | Voltaire | N |
|  |  |  | Given that I am using CLI and I have built the transaction to vote on a specific governance action, When I run the command to sign the transaction, Then I can submit the transaction and pay the transaction costs | pending |  | Voltaire | N |
|  |  | Provide rationale for vote with a metadata anchor
 | Given that I am using CLI, When I am building a transaction to vote on a specific governance action, Then I can use the metadata anchor to provide a rationale for my vote | pending |  | Voltaire | N |
|  |  | Change vote | Given that I have submitted a vote on a specific governance action, When I vote again on the same governance action, Then I can change the intent to vote (YES/NO/ABSTAIN) | pending |  | Voltaire | N |
| CH.VO11 | As a CC Member I want to change my voting credentials so I can manage my organisation’s voting | Create a new authorization certificate | Given that I am a CC member and I have enough funds to pay the transaction fees, When I create a new authorisation certificate using the same cold key, Then a new hot key is authorised to vote as a valid CC member | pending |  | Voltaire | N |
| CH.VO12 | As a CC Member I want to retire so my credentials are no longer valid | Create a resignation certificate | Given that I am a CC member and I have enough funds to pay the transaction fees, When I create a resignation certificate, Then my cold key and the derived hote keys are no longer valid to vote as a CC member | pending |  | Voltaire | N |
| CH.CLI1 | As a Plutus developer I want the Node to support Plutus V3 requirements for CIP-1694 | Correct operation of BLS primitives.
Correct operation of new bitwise primitives.
New Plutus V3 cost model is used correctly for the new primitives.
Plutus scripts are correctly used for DRep voting.
Plutus scripts on the constitution correctly control CC voting.
Benchmark execution times are within acceptable range. | Detail pending | pending | Detail pending | API/CLI |  |
| CH.API11 | Ledger API User Story | This is a placeholder | Detail pending | pending |  | API/CLI | UPDATE/REMOVE |
| VO16 | SPO Interface User Story |  |  | pending |  | API/CLI | UPDATE/REMOVE |
| INT1 | As a user of the system I want governance actions to be correctly submitted on chain |  | Detail pending | pending |  |  |  |
| INT2 | As a user of the system I want All actions to be ratified on-chain correctly according to the CIP-1694 rules  | (voter type, thresholds, DRep activity) | Detail pending | pending |  |  |  |
| INT3 | As a user of the system I want All governance actions to be enacted on time on-chain following ratification | Timely  |  | pending |  |  |  |
|  |  | Correctly according to CIP-1694 rules:Parameter updates, Info, Hard Forks, No Confidence, New Committee, New Constitution, Treasury Withdrawals.  This will expand into many requirements.
 |  | pending |  |  |  |
| SYSTEM LEVEL (not fully completed yet) |  |  |  |  |  |  |  |
| CIP1 | As any persona
I want the hash value of the off-chain Constitution to be recorded on-chain
So that I can verify the authenticity of the off-chain document | Hash value of the off-chain Constitution is recorded on-chain | Given that I access a Cardano Explorer and that it display the ledger states accurately,  Then I can access a map of the current constitution hash and the URL of the off-chain document | pending | Detail Pending | CIP-1694
L958 |  |
| CIP2 | As an ada holder
I want the key hash of active and expired Committee Members and their terms to be registered on-chain 
So that the system can count their votes | Committee members key hashes must be recorded on chain and be publicly accessible
ADA holder must be able to check that the key hashes of active and expired committee members are registered  on-chain status
 | Given that the node is up to date, then it should include a record for each committee member detailing their key-hashes, term information (end epochs), and the corresponding cold to hot key authorization maps. | pending | Detail Pending | CIP-1694
L993 |  |
| CIP3 | As an ada holder
I want to be able to submit a proposal to replace all or part of the current constitutional committee
So that committee members that have lost confidence of ada holders can be removed from their duties.  
 | It must be possible to replace the constitutional committee via a governance action
 | Any ada holder can submit a governance action that proposes to add or remove one or many new committee members. 
Given that a governance action to update the committee has been proposed And both SPO and DRep YES votes are equal or greater than the required threshold (depending on state of no-confidence or normal state)
The governance action is ratified and enacted automatically at the next epoch transition, otherwise it’s expired.  | pending | Detail Pending | CIP-1694
L997 |  |
| CIP4 | As an ada holder
I want the size of the constitutional committee
To be not-fixed
So that I can propose a different size via a governance action | Size of the constitutional committee must be variable | Detail Pending | pending | Detail Pending | L1009 |  |
| CIP5 | As an ada holder,
I want that the committee threshold (the fraction of committee is not fixed
So that I can propose a different threshold via a governance action | Size of committee threshold must be variable | Detail Pending | pending | Detail Pending | L1011 |  |
| CIP6 | As an ada holder
I want to be able to have elect an empty committee if the community wishes to abolish the constitutional committee entirely
So that SPO and Dreps can continue to ratify governance actions without the need of a constitutional committee | Users must be able to elect an empty committee

Ratifying governance actions must be possible without constitutional committee | Detail Pending | pending | Detail Pending | L1014 |  |
| CIP7 | As an Ada holder,
I want to submit a governance action,
So that it can be considered by the governance bodies/process. | There must be a command in in the Cardano CLI allowing the user to submit a governance action

The input must include validation checks for format and criteria

After successful validation the 
user must be informed of confirmation through the CLI 

An action should have an accepted or rejected status? | Detail Pending | pending | Detail Pending | CIP-1694 |  |
| CIP8 | As a delegate representative (DRep),
I want to vote on submitted governance actions,
So that I can represent the interests of my delegates. | DReps must have access to the list of current governance actions (can we specify where they get it?).
DReps should be able to cast their vote on each action (through the CL or through an app)?
An action should have an accepted or rejected status? | 
Given that a Drep has casted a vote the system accurately records and reflects these votes. | pending | Detail Pending | CIP-1694 |  |
| CIP9 | As an Ada holder,
I want to view the status of governance actions,
So that I am informed about the governance process. | Users must be able to view a list of governance actions with their current status.
The status must include stages like submission, voting, ratification, timeline.
The system must provide real-time updates on the status. | Detail Pending | pending | Detail Pending | CIP-1694 |  |
| CIP10 | As an Ada holder,
I want to delegate my voting rights to a DRep,
So that my interests are represented in the governance process. | ADA holders can select a DRep to delegate their voting rights.
The delegation process should be user-friendly and must be secure.
The system must confirms successful delegation. | Detail Pending | pending | pending |  |  |
| CIP11 | As an SPO,
I want to participate in the governance voting,
So that I can contribute to the decision-making process. | SPOs must have access to governance actions for voting.
SPOs can cast their votes based on the ADA staked in their pools.
The system accurately reflects the votes of SPOs. | Detail Pending | pending | pending |  |  |
| CARDANO CLI US |  |  |  |  |  |  |  |
| CLI01 | As an Ada holder,
I want to obtain the hash of the off-chain text of a Constitution
So that I can compare it against the hash registered on-chain to verify its authenticity. | When I provide the off-chain text of the Constitution, the cardano-cli should calculate and return the corresponding blake2b-256 hash of the document.  | Given that a holder provides the offchain text of the constitution then cardo-cli should return the corresponding blake2b-256 hash
Given that it is the same document, the resulting hash should match the one registered on-chain.  | pending | pending | L958 |  |
| CLI02 | As an Ada holder,
I want to generate the hash of the off-chain text for a proposed Constitution
So that the hash can be utilized in a governance action.
 | When I provide the off-chain text of the Constitution, the cardano-cli should calculate and return the corresponding blake2b-256 hash of the document.  | Given that a holder provides the offchain text of the constitution then cardo-cli should return the corresponding blake2b-256 hash
Given that it is the same document, the resulting hash should match the one registered on-chain. 
 | pending | pending | L958 |  |
| CLI03 | As a potential Constitutional Committee member, 
I want to generate COLD key pair 
So that I can be proposed for the Committee in a Governance action | The feature implementation should include a new command: 

cardano-cli conway governance committee key-gen-cold | Typing  cardano-cli conway governance committee key-gen-cold with accepted input parameters generates a COLD key pair. If a parameter or the command format is incorrect an error is raised | pending | pending | L966
L993 |  |
|  |  | Includes a corresponding CLI usage  describing the feature, how to use it and the types of the inputs and outputs. | Typing  cardano-cli conway governance committee key-gen-cold —-help displays command usage | pending | pending | L966
L993 |  |
|  |  | The command must accept two flags
--cold-verification-key-file
--cold-signing-key-file | Both flags are mandatory and each produces the corresponding verification or signing key file  | pending | pending | L966
L993 |  |
|  |  | The generated key pair should be stored in the specified files: 

the verification key is saved in the file specified by --cold-verification-key-file 

 the signing key saved in the file specified by 
--cold-signing-key-file | Given that the user specifies a valid path and file name, Then the keys are saved on that file and location.    | pending | pending | L966
L993 |  |
|  |  | The generated keys should adhere to text envelope format used for other credentials  | Given that the cli has created the verification and signing keys, then these conform to the text envelope format used  consisting of a json object with type, description and cborhex fields.  | pending | pending | L966
L993 |  |
|  |  | The signing key text envelope contains the correct type, description, and CBOR value.

Type "ConstitutionalCommitteeColdSigningKey_ed25519" 

Description 
"Constitutional Committee Cold Signing Key" | Given that the signing key is saved on a text envelope format, the type and description fields are: 

Type "ConstitutionalCommitteeColdSigningKey_ed25519" 

Description 
"Constitutional Committee Cold Signing Key" | pending | pending | L966
L993 |  |
|  |  | The verification key text envelope has: 
Type "CConstitutionalCommitteeColdVerificationKey_ed25519"  
Description
"Constitutional Committee Cold Verification Key"  | Given that the verification key is saved on a text envelope format, the type and description fields are:

Type "CConstitutionalCommitteeColdVerificationKey_ed25519"  
Description
"Constitutional Committee Cold Verification Key"   | pending | pending | L966
L993 |  |
|  |  | Failing to provide a file name for any of 

--cold-verification-key-file 
--cold-signing-key-file 

fails with an appropriate error message. | Given the user has not inputed either --cold-verification-key-file OR
--cold-signing-key-file parameters THEN the command fails and returns an error to the users informing them to fill those parameters in. The error message should prompt the user to consult the command usage (--help) 
 | pending | pending | L966
L993 |  |
| CLI04 | As potential Constitutional Committee member, 
I want to generate HOT key pair 
So that I can authorise the Hot key to sign votes on behalf of the Cold key | The feature implementation should include a new command: 

cardano-cli conway governance committee key-gen-hot | Given that a potential constitutional committee member has entered the cardano-cli conway governance committee key-gen-hot command with all the required and correct parameters then the command is executed successfully and a HOT key pair is generated. 
If a parameter or the command format is incorrect an error is raised
 | pending | pending | L966
L993 |  |
|  |  | Includes a corresponding CLI usage  describing the feature, how to use it and the types of the inputs and outputs. | Typing  cardano-cli conway governance committee key-gen-hot displays command usage | pending | Detail Pending | L966
L993 |  |
|  |  | The command must accept two flags 
--verification-key-file
--signing-key-file | Both flags are mandatory and each produces the corresponding verification or signing key file  | pending | Detail Pending | L966
L993 |  |
|  |  | The generated key pair should be stored in the specified files: 

the verification key saved in the file specified by 
--verification-key-file

the signing key saved in the file specified by 
--signing-key-file | Given that the user specifies a valid path and file name, Then the keys are saved on that file and location.   | pending | pending | L966
L993 |  |
|  |  | The generated keys should adhere to text envelope format used for other credentials | Given that the cli has created the verification and signing keys, then these conform to the text envelope format used  consisting of a json object with type, description and cbor hex fields. | pending | pending | L966
L993 |  |
|  |  | The signing key text envelope contains the correct type, description, and CBOR value.

Type "ConstitutionalCommitteeColdSigningKey_ed25519" 

Description
"Constitutional Committee Cold Signing Key" | Given that the signing key is saved on a text envelope format, the type and description fields are: 
Type "ConstitutionalCommitteeColdSigningKey_ed25519" 

Description
"Constitutional Committee Cold Signing Key" | pending | pending | L966
L993 |  |
|  |  | The verification key text envelope has: 
Type
"CConstitutionalCommitteeColdVerificationKey_ed25519"  
Description
"Constitutional Committee Cold Verification Key" | Given that the verification key is saved on a text envelope format, the type and description fields are:
Type
"CConstitutionalCommitteeColdVerificationKey_ed25519"  
Description
"Constitutional Committee Cold Verification Key"  | pending | pending | L966
L993 |  |
|  |  | Failing to provide a file name for any of the flags 

--verification-key-file 
--signing-key-file 

fails with an appropriate error message. | Given the user has not inputted either --verification-key-file OR
--signing-key-file parameters THEN the command fails and returns an error to the users informing them to fill those parameters in. The error message should prompt the user to consult the command usage (--help)  | pending | pending | L966
L993 |  |
| CLI05 | As a committee member 
I want to issue a authorization certificate from my cold key to a hot key

So that I can sign my votes using the hot key and keep the cold key in cold storage and can authorise a new hot key in case the original one is compromised. | The feature implementation should include a new command in the cardano-cli: 

cardano-cli conway governance committee create-hot-key-authorization-certificate | Typing  cardano-cli conway governance committee create-hot-key-authorization-certificate with accepted input parameters generates a hot key authorization certificate. If a parameter or the command format is incorrect an error is raised | pending | pending | L993 |  |
|  |  | The command should accept the necessary flags: 

--cold-verification-key, --cold-verification-key-file, --cold-verification-key-hash, --hot-verification-key, --hot-verification-key-file, --hot-verification-key-hash, and --out-file. | The command allows passing credentials as follows

Cold verification key <- string
Cold verification key file <- file
Cold verification key hash <- string

Hot verification key <- string 
Hot verification key file <- file
Hot verification key hash <- string 

Failing to provide the right input results in a clear error message that helps the user to identify the problem | pending | pending | L993 |  |
|  |  | Running the command with the appropriate flags should generate a hot key authorization certificate and be saved in the specified output file. | Given that the user specifies a valid path and file name, then the command produces a Cold to Hot authorization certificate on the right location and name.    | pending | pending | L993 |  |
|  |  | The hot key authorization certificate should follow the text envelope format of other existing certificates, including the type, description, and CBOR hex value.

{
    "type": "CertificateConway",
    "description": "Constitutional Committee Hot Key Authorization Certificate",
    "cborHex": ""
} | Given that the authorization certificate is saved, then it is in a text envelope format consisting of a json object with type, description and cbor hex fields. | pending | pending | L993 |  |
|  |  | The type of the certificate should be:  "CertificateConway"  | The type field ont the text envelope of the certificate is 
"CertificateConway"  | pending | pending | L993 |  |
|  |  | The description of the certificate should be: 

"Committee HotKey Authorization Certificate" | The description  field on the text envelope of the certificate is 
"Committee HotKey Authorization Certificate" | pending | pending | L993 |  |
|  |  | The certificate must comply with the cddl:

 auth_committee_hot_cert = (14, committee_cold_credential, committee_hot_credential) | Given that the authorization certificate is saved,then it is on the form of a text envelope consisting of a json object with type, description and cbor hex fields , where 

Cbor hex conforms to the authorization certificate as defined on the cddl 

auth_committee_hot_cert = (14, committee_cold_credential, committee_hot_credential) | pending | pending | L993 |  |
|  |  | The command should handle potential errors, such as missing or invalid flags, and provide appropriate error messages indicating the missing or required parameters. | The command should handle potential errors, such as missing or invalid flags, and provide appropriate error messages indicating the missing or required parameters. | pending | pending | L993 |  |
|  |  | Documentation should be provided, including a corresponding CLI usage, describing the feature, its purpose, and how to use it, along with the expected types of inputs and outputs. | Typing  cardano-cli conway governance committee create-hot-key-authorization-certificate —-help displays command usage | pending | pending | L993 |  |
| CLI06 | As a potential constitutional committee member 
I want to generate the key hashes for my cold and hot keys 
So that they can be used by third parties to propose me as a new committee member and for identification purposes once Ive been elected as committee member | The command generates the blake2b 256 hash of the verification key
cardano-cli conway governance committee key-hash | Typing  cardano-cli conway governance committee key-hash with accepted input parameters generates blake2b 256 hash of the verification key. If a parameter or the command format is incorrect an error is raised | pending | pending |  |  |
|  |  | Accepts the flags 
--verification-key --verification-key-file 
To provide the verification key. | Both flags are mandatory and each produces the corresponding verification or signing key file  | pending | pending |  |  |
|  |  | The command gives the option –out-file.  If the --out-file flag is provided, the key hash should be saved to the specified file.  | Given that the user specifies the –out-file parameter and a valid path and file name, Then the key hash is saved on that file and location.   | pending | pending |  |  |
|  |  | If the --out-file flag is not provided, the key hash should be printed to the standard output (stdout) in a readable format. | Given that the user has not specified the –out-file parameter then the key hash must returned in clear text through stdout (cmd output)  | pending | pending |  |  |
|  |  | The command should handle potential errors, such as missing flags or invalid input, and provide appropriate error messages or exceptions to guide the user. | Given that the user has executed the correct command but has either filled incorrectly any of the parameters, missed any mandatory flag and/or parameter  then an exception should be raised and an error message should be returned with clear indication as to how to fix the issue. When not feasible, the user should be directed to the usage page of the command (cardano-cli conway governance committee key-hash --help)   | pending | pending |  |  |
|  |  | Documentation should be provided, including a corresponding CLI usage, describing the feature, its purpose, and how to use it, along with the expected types of inputs and outputs. | Typing cardano-cli conway governance committee key-hash --help display the command usage page | pending | pending |  |  |
| CLI07 | As a constitutional committee member 
I want to be able to generate a resignation certificate 
So that i can submit it it to the chain on a transaction to signal to the ada holders that I’m resigning from my duties as cc member
 | The command should be implemented in the cardano-cli as cardano-cli governance committee create-cold-resignation-certificate | Typing cardano-cli governance committee create-cold-resignation-certificate with accepted input parameters generates a cold resignation certificate. | pending | pending |  |  |
|  |  | The command should accept the following ways to supply credentials:  cold verification  key file, the cold verification key or the cold verification key hash so it accepts  the following flags: 

--cold-verification-key, 
--cold-verification-key-file,
--cold-verification-key-hash. | The command allows passing credentials as follows

Cold verification key <- string
Cold verification key file <- file
Cold verification key hash <- string

If any of the inputs has the wrong format the cli raises an arrow message indicating  the missing or incorrect parameter. | pending | pending |  |  |
|  |  | The command allows an optional anchor (url/hash) for the resigning 
cc member to express their
motivation for resigning.  | The command allows for an OPTIONAL anchor comprised of a URL containing a document where the resigning CC member expresses the motivations and the hash of the document

The CLI does not check for the validity of the URL, the contents, or that the documents and declared hash match.   | pending | pending |  |  |
|  |  |  The resignation certificate should be saved in the specified output file using the --out-file flag. | Given that the CC member issuing the resignation certificate provides a valid path and file name, then the certificate is saved on the specified location.  | pending | pending |  |  |
|  |  | The generated resignation certificate should be consistent with the text envelope format of existing certificates in Cardano, including the specified JSON structure with the correct type, description, and CBOR-encoded value.



{
    "type": "CertificateConway",
    "description": "Constitutional Committee Cold Key Resignation Certificate",
    "cborHex": ""
} | Given that the resignation certificate is saved, then it is in a text envelope format consisting of a json object with type, description and cbor hex fields. | pending | pending |  |  |
|  |  | The certificate type should be ConwayResignCommitteeColdKey to indicate a resignation of the Committee Cold Key. | Given that the certificate is in a text envelope format, then its type is 

Type: ConwayResignCommitteeColdKey | pending | pending |  |  |
|  |  | The certificate description  should be

"description": "Constitutional Committee Cold Key Resignation Certificate"  | Given that the certificate is in a text envelope format, then its description field  is 

"description": "Constitutional Committee Cold Key Resignation Certificate" | pending | pending |  |  |
|  |  |  The command should generate a resignation certificate according to the conway cddl: 
resign_committee_cold_cert = (15, committee_cold_credential, anchor / null) | Given that the certificate is in a text envelope format, then its cbor hex  field  conforms to the conway cddl 

resign_committee_cold_cert = (15, committee_cold_credential, anchor / null) | pending | pending |  |  |
|  |  | The command should handle potential errors, such as missing or invalid flags or keys, and provide appropriate error messages indicating the missing or required parameters. | If any required input parameter is missing or incorrect, the command should raise an error indicating the missing or incorrect parameter. | pending | pending |  |  |
|  |  | Documentation should be provided, including a corresponding CLI usage, describing the feature, its purpose, and how to use it, along with the expected types of inputs and outputs.
 | Given that the user has executed the correct command but has either filled incorrectly any of the parameters, missed any mandatory flag and/or parameter  then an exception should be raised and an error message should be returned with clear indication as to how to fix the issue. When not feasible, the user should be directed to the usage page of the command (cardano-cli governance committee create-cold-resignation-certificate --help)   | pending | pending |  |  |
| CLI08 | As an ada holder 
I want to generate Ed25519 keys 
So that I can register as a DRep

 | The command is implemented as 

cardano-cli conway governance drep key-gen | Typing cardano-cli conway governance drep key-gen with accepted input parameters generates an Ed25519 key pair | pending | pending |  |  |
|  |  | The command supports the --verification-key-file FILE option to specify the file where the generated verification key will be saved. | The flag --verification-key-file is mandatory, 
 | pending | pending |  |  |
|  |  | The command supports the --signing-key-file FILE option to specify the file where the generated signing key will be saved. File is saved on the specified path | The flag --signing-key-file is mandatory, 

 | pending | pending |  |  |
|  |  | When the command is executed, it generates both the verification key and signing key  File is saved on the specified path | Given that the user specifies valid paths and file names then, the  corresponding verification and signing key files are saved on the paths specified by the user. 

If the paths do not exist or are  inaccessible, an error message is raised. | pending | pending |  |  |
|  |  | The key generation should follow the current design for key generation and output in an envelope format.
 | Given that the verification and signing key files are saved, then they are in a text envelope format consisting of a json object with type, description and cbor hex fields, where: 

{
 "type": "DRepVerificationKey_ed25519",
 "description": "Delegate Representative Verification Key",
  "cborHex": ""
}

{
 "type": "DRepSigningKey_ed25519",
 "description": "Delegate Representative VSigning Key",
  "cborHex": ""
}

  | pending | pending |  |  |
| CLI09 | As a DRep 
I want to generate a Drep Id
So that ada holder can use it to delegate their votes to me and my voting record can be tracked
 | The command is implemented as cardano-cli conway governance drep id
and generates the blake2b-224 hash digest of the serialised DRep credential (verification key)
 | Typing cardano-cli conway governance drep id
with accepted input parameters generates a DRep ID, the blake2b-224 hash digest of the serialised DRep credential (verification key) | pending | pending |  |  |
|  |  | The command accepts supplying the verification key with either 

--drep-verification-key
–drep-verification-key-file options
 | Using one of the flags is mandatory,  the flags are mutually exclusive and take a string and file respectively:
--drep-verification-key <- string
–drep-verification-key-file  <- file  | pending | pending |  |  |
|  |  | The command supports the --out-file FILE option (optional) to enable users to save the generated DRep ID to the specified file. | Given that the user wants to save the DrepId to a file, and specifies a valid path and file name, then, using the –out-file flag saves the drep id to a file on the specified location.

If the specified path does not exist or is inaccessible the cli returns an error message. 

If the –out-flag is not used the Drep ID is printed on stdout | pending | pending |  |  |
|  |  | The command should support the an option to specify the output format 
Accepted output formats are "hex" and "bech32", where "bech32" is the default format. | Given that the optional --output-format flag is used, and  “bech32” is given as an argument, then the DRep Id is printed in bech32 format with the “drep” prefix.

Given that the optional --output-format flag is used, and the hex is given as an argument, then the DRep Id is printed in hex format

If the --output-format STRING option is not specified, the DRep ID should be displayed in "bech32" format by default. | pending | pending |  |  |
|  |  | The command supports an optional –out-file to save the Drep Id to a file  | If the --out-file FILE option is specified, the generated DRep ID should be saved to the specified file, otherwise it is printed on stdout | pending | pending |  |  |
|  |  | The feature is well-documented, providing clear usage instructions for the cardano-cli conway governance drep id command. | Typing cardano-cli conway governance drep id --help 
displays the command usage page | pending | pending |  |  |
|  |  | The command handles errors gracefully and provides helpful error messages when required options are missing or invalid inputs are provided. | If any required input parameter is missing or incorrect, the command should raise an error indicating the missing or incorrect parameter. | pending | pending |  |  |
| CLI10 | As a DRep 
I want to generate a Drep registration certificate
So that I can submit it on a transaction and the ada holders can delegate their votes to me.  
 | The command is implemented as 
cardano-cli conway governance drep registration-certificate | Running 
cardano-cli conway governance drep registration-certificate with accepted input parameters generates a drep registration certificate. | pending | pending |  |  |
|  |  | The command requires the user to provide the amount required for drep key deposit to comply with the conway cddl -> “reg_drep_cert” 
 | The flag --key-reg-deposit-amt is mandatory and takes the deposit amount in lovelace as argument.   | pending | pending |  |  |
|  |  | The command allows the user to provide the DRep credential  in the following ways:

Drep verification key 
Drep verification key file 
Drep Id
 | The command presents the options to pass the Drep credential: 
 
--drep-verification-key STRING 
--drep-verification-key-file FILE 
--drep-id STRING 

Using one of these is mandatory but are mutually exclusive. 

Failing to provide the right input results in a clear error message that helps the user to identify the problem | pending | pending |  |  |
|  |  | The command allows adding an optional anchor (url/hash) to submit any drep metadata.  | Given that the user wants to include an anchor with the Dreps metadata, then the command requires both the url and the hash to be provided. Only url or only hash is not allowed.

--drep-metadata-url TEXT                                                                    --drep-metadata-hash HASH

Failing to provide the right input results in a clear error message that helps the user to identify the problem | pending | pending |  |  |
|  |  | When the --drep-metadata-url and --drep-metadata-hash

are provided, the resulting certificate should include the url and hash on the anchor position, otherwise the field is null.  | The anchor is included in the certificate on the last position: 

reg_drep_cert = (16, drep_credential, coin, anchor / null) | pending | pending |  |  |
|  |  | The --out-file FILE option is  mandatory and used to specify the file where the generated DRep registration certificate will be saved. | Detail Pending | pending | pending |  |  |
|  |  | The command generates a registration certificate compliant with the conway cddl 

reg_drep_cert = (16, drep_credential, coin, anchor / null) | Detail Pending | pending | pending |  |  |
|  |  | The certificate should be on a text envelope format, similar to what we have for stake pools registration certificates
{
    "type": "CertificateConway",
    "description": "DRep Registration Certificate",
    "cborHex": "00000000"
}
 | Detail Pending | pending | pending |  |  |
|  |  | The feature implementation should be well-documented, providing clear usage instructions for the cardano-cli conway governance drep registration-certificate command. | Detail Pending | pending | pending |  |  |
|  |  | The command should handle errors gracefully and provide helpful error messages when required options are missing or invalid inputs are provided. | Detail Pending | pending | pending |  |  |
| CLI11 | As a DRep 
I want to generate a Drep retirement (unregistration) certificate
So that I can submit it on a transaction and can get my DRep deposit back.  
 | The command allows the user to provide the DRep credentials in the following ways:
Using the --drep-verification-key STRING option to specify the DRep verification key directly as a string.
Using the --drep-verification-key-file FILE option to specify the file containing the DRep verification key.
Using the --drep-id STRING option to specify the DRep ID directly as a string. 
cardano-cli conway governance drep retirement-certificate | Detail Pending | pending | pending |  |  |
|  |  | The command has the mandatory flag --deposit-amt to require the user to provide the drep deposited amount  that is to be returned. 

Must match the deposit originally paid when registering as DRep but is only checked when submitting the transaction.  | Detail Pending | pending | pending |  |  |
|  |  | The --out-file FILE option should be mandatory and used to specify the file where the generated DRep retirement certificate will be saved | Detail Pending | pending | pending |  |  |
|  |  | The certificate should be on a text envelope format, similar to what we have for stake pools deregistration certificates
{
    "type": "CertificateConway",
    "description": "DRep Retirement Certificate",
    "cborHex": "00000000"
}
 | Detail Pending | pending | pending |  |  |
|  |  | The output certificate complies with the conway cddl 

unreg_drep_cert = (17, drep_credential, coin) | Detail Pending | pending | pending |  |  |
|  |  | The feature implementation should be well-documented, providing clear usage instructions | Detail Pending | pending | pending |  |  |
|  |  | The command handles errors gracefully and provides helpful error messages when required options are missing or invalid inputs are provided. | Detail Pending | pending | pending |  |  |
| CLI12 | As a Drep 
I want to generate the hash of my DRep metadata
So that I can supply it when registering as DRep | The command calculates the blake2b 256 hash of the file supplied by the user. 
cardano-cli conway governance drep metadata-hash | Detail Pending | pending | pending |  |  |
|  |  | The command requires the --drep-metadata-file FILE option to specify the file containing the DRep metadata. | Detail Pending | pending | pending |  |  |
|  |  | The command supports the --out-file FILE option (optional) to enable users to save the calculated metadata hash to the specified file. If the flag is not used, the hash is printed to stdout | Detail Pending | pending | pending |  |  |
|  |  | The command handles errors gracefully and provides helpful error messages when required options are missing or invalid inputs are provided. | Detail Pending | pending | pending |  |  |
| CLI13 | As an ada holder
I want to create a governance action that updates the constitution 
So that it can be submitted to the chain and be voted by the governance bodies | The command requires either --mainnet or --testnet-magic NATURAL option to specify the target network for which the governance action is generated 
cardano-cli conway governance action create-constitution | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide the the deposit amount for submitting governance actions via the flag --governance-action-deposit | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide the stake credential that will receive the deposit return when the action is enacted/expired. It accepts: 
--stake-verification-key-file
--stake-verification-key
--stake-key-hash  | Detail Pending | pending | pending |  |  |
|  |  | The command allows the user to provide the transaction id and index of the previously enacted action of this type. These flags are optional (but if one is used the other one must be used too)  to support the very first action of this type on the system which does not require information about previously enacted actions. The flags are:
--governance-action-tx-id 
--governance-action-index | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide an anchor (url / hash) of the proposal. A document where the proposer exposes the reasoning behind the proposed change. 
--anchor-url
--anchor-data-hash  | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide an anchor (url / hash) of the new constitution. 
--constitution-url
--constitution-hash
 | Detail Pending | pending | pending |  |  |
|  |  | The command has the mandatory flag –out-file to specify the file here the governance action (the proposal) will be saved.  | Detail Pending | pending | pending |  |  |
|  |  | The generated governance action complies with the conway cddl, where: 
proposal_procedure =
  [ deposit : coin
  , reward_account
  , gov_action
  , anchor
  ]

new_constitution = (5, gov_action_id / null, constitution)

constitution =
  [ anchor
  , scripthash / null
  ] | Detail Pending | pending | pending |  |  |
| CLI14 | As an ada holder
I want to create a governance action that updates the constitutional committee
So that it can be submitted to the chain and be voted by the governance bodies | The command requires either --mainnet or --testnet-magic NATURAL option to specify the target network for which the action is generated
 | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide the the deposit amount for submitting governance actions via the flag --governance-action-deposit | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide the stake credential that will receive the deposit return when the action is enacted/expired. It accepts: 
--stake-verification-key-file
--stake-verification-key
--stake-key-hash  | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide an anchor (url / hash) of the proposal. A document where the proposer exposes the reasoning behind the proposed change. 
--anchor-url
--anchor-data-hash  | Detail Pending | pending | pending |  |  |
|  |  | The command offers the option to remove many CC members, it accepts:
--remove-cc-cold-verification-key-hash
--remove-cc-cold-verification-key
--remove-cc-cold-verification-key-file | Detail Pending | pending | pending |  |  |
|  |  | The command offers the option to add many CC members.  
--add-cc-cold-verification-key
--add-cc-cold-verification-key-file
--add-cc-cold-verification-key-hash | Detail Pending | pending | pending |  |  |
|  |  | When adding a new member, the command requires the user to also provide a term for each new member using the flag –epoch  | Detail Pending | pending | pending |  |  |
|  |  | The command allows proposing a new quorum threshold:

When adding members
When removing members
As standalone action (no adds or removals)  | Detail Pending | pending | pending |  |  |
|  |  | The command has the flag –out-file to specify the file where the governance action (the proposal) will be saved. 


 | Detail Pending | pending | pending |  |  |
|  |  | The generated governance action complies with the conway cddl, where: 

proposal_procedure =
  [ deposit : coin
  , reward_account
  , gov_action
  , anchor
  ]


update_committee = (4, gov_action_id / null, set<committee_cold_credential>, { committee_cold_credential => epoch }, unit_interval) | Detail Pending | pending | pending |  |  |
| CLI15 | As an ada holder
I want to create a governance action to withdraw funds from the treasury 
So that it can be submitted to the chain and be voted by the governance bodies
cardano-cli conway governance action create-treasury-withdrawal | The command requires either --mainnet or --testnet-magic NATURAL option to specify the target network for which the action is generated
 | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide the the deposit amount for submitting governance actions via the flag --governance-action-deposit | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide the stake credential that will receive the deposit return when the action is enacted/expired. It accepts: 
--stake-verification-key-file
--stake-verification-key
--stake-key-hash  | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide an anchor (url / hash) of the proposal. A document where the proposer exposes the reasoning behind the proposed change. 
--anchor-url
--anchor-data-hash  | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide the stake credential that will receive the funds if the governance action is ratified.  It accepts: 
--stake-verification-key-file
--stake-verification-key
--stake-key-hash 
 | Detail Pending | pending | pending |  |  |
|  |  | Requires the user to provide the amount in lovelace that will be transferred from the treasury to the stake credential if the action is ratified.  | Detail Pending | pending | pending |  |  |
|  |  | The command has the flag –out-file to specify the file where the governance action (the proposal) will be saved.  | Detail Pending | pending | pending |  |  |
|  |  | The generated governance action complies with the conway cddl, where: 

proposal_procedure =
  [ deposit : coin
  , reward_account
  , gov_action
  , anchor
  ]

treasury_withdrawals_action = (2, { reward_account => coin })
 | Detail Pending | pending | pending |  |  |
| CLI16 | As an ada holder
I want to create an info governance action
So that it can be submitted to the chain and be voted by the governance bodies
cardano-cli conway governance action create-info | The command requires either --mainnet or --testnet-magic NATURAL option to specify the target network for which the action is generated. | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide the the deposit amount for submitting governance actions via the mandatory flag --governance-action-deposit | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide the stake credential that will receive the deposit return when the action is enacted/expired. It accepts: 
--stake-verification-key-file
--stake-verification-key
--stake-key-hash  | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide an anchor (url / hash) of the proposal. A document where the proposer exposes the reasoning behind the proposed change. 
--anchor-url
--anchor-data-hash  | Detail Pending | pending | pending |  |  |
|  |  | The command has the flag –out-file to specify the file where the governance action (the proposal) will be saved.  | Detail Pending | pending | pending |  |  |
|  |  | The generated governance action complies with the conway cddl, where: 

proposal_procedure =
  [ deposit : coin
  , reward_account
  , gov_action
  , anchor
  ]

info_action = 6 | Detail Pending | pending | pending |  |  |
| CLI17 | As an ada holder
I want to create a governance action to update protocol parameters
So that it can be submitted to the chain and be voted by the governance bodies
cardano-cli conway governance action create-protocol-parameters-update | The command requires either --mainnet or --testnet-magic NATURAL option to specify the target network for which the DRep registration certificate is generated. | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide the the deposit amount for submitting governance actions via the mandatory flag --governance-action-deposit | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide the stake credential that will receive the deposit return when the action is enacted/expired. It accepts: 
--stake-verification-key-file
--stake-verification-key
--stake-key-hash  | Detail Pending | pending | pending |  |  |
|  |  | The command allows the user to provide the transaction id and index of the previously enacted action of this type. These flags are optional (but if one is used the other one must be used too)  to support the very first action of this type on the system which does not require information about previously enacted actions. The flags are:
--governance-action-tx-id 
--governance-action-index | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide an anchor (url / hash) of the proposal. A document where the proposer exposes the reasoning behind the proposed change. 
--anchor-url
--anchor-data-hash  | Detail Pending | pending | pending |  |  |
|  |  | The command includes dedicated flags to reference the protocol parameter that the user is attempting to modify. The parameters that can be included in this type of proposal are: 
The network group consists of:
maximum block body size (maxBBSize)
maximum transaction size (maxTxSize)
maximum block header size (maxBHSize)
maximum size of a serialized asset value (maxValSize)
maximum script execution units in a single transaction (maxTxExUnits)
maximum script execution units in a single block (maxBlockExUnits)
maximum number of collateral inputs (maxCollateralInputs)
The economic group consists of:
minimum fee coefficient (minFeeA)
minimum fee constant (minFeeB)
delegation key Lovelace deposit (keyDeposit)
pool registration Lovelace deposit (poolDeposit)
monetary expansion (rho)
treasury expansion (tau)
minimum fixed rewards cut for pools (minPoolCost)
minimum Lovelace deposit per byte of serialized UTxO (coinsPerUTxOByte)
prices of Plutus execution units (prices)
The technical group consists of:
pool pledge influence (a0)
pool retirement maximum epoch (eMax)
desired number of pools (nOpt)
Plutus execution cost models (costModels)
proportion of collateral needed for scripts (collateralPercentage)
The governance group consists of all the new protocol parameters that are introduced in this CIP:
governance voting thresholds
dRepVotingThresholds
dvtCommitteeNoConfidence
dvtCommitteeNormal
dvtHardForkInitiation
dvtMotionNoConfidence
dvtPPEconomicGroup
dvtPPGovGroup
dvtPPNetworkGroup
dvtPPTechnicalGroup
dvtTreasuryWithdrawal
dvtUpdateToConstitution
poolVotingThresholds
pvtCommitteeNoConfidence
pvtCommitteeNormal
pvtHardForkInitiation
pvtMotionNoConfidence
governance action maximum lifetime in epochs (govActionLifetime)
governance action deposit (govActionDeposit)
DRep deposit amount (drepDeposit)
DRep activity period in epochs (drepActivity)
minimal constitutional committee size (ccMinSize)
maximum term length (in epochs) for the constitutional committee members (ccMaxTermLength) | Detail Pending | pending | pending |  |  |
|  |  | The command has the flag –out-file to specify the file where the governance action (the proposal) will be saved.  | Detail Pending | pending | pending |  |  |
|  |  | The generated governance action complies with the conway cddl, where: 

proposal_procedure =
  [ deposit : coin
  , reward_account
  , gov_action
  , anchor
  ]

parameter_change_action = (0, gov_action_id / null, protocol_param_update) | Detail Pending | pending | pending |  |  |
| CLI18 | As an ada holder
I want to create a no-confidence governance action
So that it can be submitted to the chain and be voted by the governance bodies

cardano-cli conway governance action create-no-confidence | The command requires either --mainnet or --testnet-magic NATURAL option to specify the target network for which the action is generated. | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide the the deposit amount for submitting governance actions via the mandatory flag --governance-action-deposit | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide the stake credential that will receive the deposit return when the action is enacted/expired. It accepts: 
--stake-verification-key-file
--stake-verification-key
--stake-key-hash  | Detail Pending | pending | pending |  |  |
|  |  | The command allows the user to provide the transaction id and index of the previously enacted action of this type. These flags are optional (but if one is used the other one must be used too)  to support the very first action of this type on the system which does not require information about previously enacted actions. The flags are:
--governance-action-tx-id 
--governance-action-index | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide an anchor (url / hash) of the proposal. A document where the proposer exposes the reasoning behind the proposed change. 
--anchor-url
--anchor-data-hash  | Detail Pending | pending | pending |  |  |
|  |  | The command has the flag –out-file to specify the file where the governance action (the proposal) will be saved.  | Detail Pending | pending | pending |  |  |
|  |  | The generated governance action complies with the conway cddl, where: 

proposal_procedure =
  [ deposit : coin
  , reward_account
  , gov_action
  , anchor
  ]

no_confidence = (3, gov_action_id / null) | Detail Pending | pending | pending |  |  |
| CLI19 | As an ada holder
I want to create a governance action to initiate a hardfork
So that it can be submitted to the chain and be voted by the governance bodies

 | The command requires either --mainnet or --testnet-magic NATURAL option to specify the target network for which the action is generated. | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide the the deposit amount for submitting governance actions via the mandatory flag --governance-action-deposit | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide the stake credential that will receive the deposit return when the action is enacted/expired. It accepts: 
--stake-verification-key-file
--stake-verification-key
--stake-key-hash  | Detail Pending | pending | pending |  |  |
|  |  | The command allows the user to provide the transaction id and index of the previously enacted action of this type. These flags are optional (but if one is used the other one must be used too)  to support the very first action of this type on the system which does not require information about previously enacted actions. The flags are:
--governance-action-tx-id 
--governance-action-index | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to provide an anchor (url / hash) of the proposal. A document where the proposer exposes the reasoning behind the proposed change. 
--anchor-url
--anchor-data-hash  | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to input the new protocol version number | Detail Pending | pending | pending |  |  |
|  |  | The command has the flag –out-file to specify the file where the governance action (the proposal) will be saved.  | Detail Pending | pending | pending |  |  |
|  |  | The generated governance action complies with the conway cddl, where: 

proposal_procedure =
  [ deposit : coin
  , reward_account
  , gov_action
  , anchor
  ]

hard_fork_initiation_action = (1, gov_action_id / null, [protocol_version]) | Detail Pending | pending | pending |  |  |
| CLI20 | As an ada holder
I want to inspect the contents of a governance action file 
So that I can verify it is correct before submitting it in a transaction

cardano-cli conway governance action view
 | The command takes an action file as input | Detail Pending | pending | pending |  |  |
|  |  | Gives an option to select the output format (json or yaml)  | Detail Pending | pending | pending |  |  |
|  |  | The command has the flag –out-file to specify the file where the output is saved, if it is not specified it is printed to stdout | Detail Pending | pending | pending |  |  |
|  |  | The output shows the information of the proposal based on the proposal procedures on a human readable format:

proposal_procedure =
  [ deposit : coin
  , reward_account
  , gov_action
  , anchor
  ] | Detail Pending | pending | pending |  |  |
| CLI21 | As a Drep, SPO or CC member 
I want to create a vote for a governance action 
So that I can include it in a transaction and submit it to the chain 

 cardano-cli conway governance vote create
 | The command provides a way to vote 
yes, 
no 
abstain | Detail Pending | pending | pending |  |  |
|  |  | Requires to specify the governance action ID and index that the vote is about.  | Detail Pending | pending | pending |  |  |
|  |  | Requires the user to provide DRep, SPO or CC credentials  | Detail Pending | pending | pending |  |  |
|  |  | The command allows the user to provide an optional anchor (url / hash) if the user wishes to share the reasoning behind the vote.
--anchor-url
--anchor-data-hash  | Detail Pending | pending | pending |  |  |
|  |  | The command has the flag –out-file to specify the file where the vote will be saved.  | Detail Pending | pending | pending |  |  |
|  |  | The generated vote complies with the conway cddl where 

voting_procedures = { + voter => { + gov_action_id => voting_procedure } }

voting_procedure =
  [ vote
  , anchor / null
  ]

; no - 0
; yes - 1
; abstain - 2
vote = 0 .. 2 | Detail Pending | pending | pending |  |  |
| CLI22 | As a DRep, SPO or CC member 
I want to inspect the contents of a vote file 
So that I can verify it is correct before submitting it in a transaction

cardano-cli conway governance vote view
 | The command takes a vote file as an input | Detail Pending | pending | pending |  |  |
|  |  | Gives an option to select the output format (json or yaml)  | Detail Pending | pending | pending |  |  |
|  |  | The command has the flag –out-file to specify the file where the output is saved, if it is not specified it is printed to stdout | Detail Pending | pending | pending |  |  |
|  |  | The output shows the information of the proposal based on the voting procedures in a human readable format (english):

voting_procedures = { + voter => { + gov_action_id => voting_procedure } }

voting_procedure =
  [ vote
  , anchor / null
  ]

; no - 0
; yes - 1
; abstain - 2
vote = 0 .. 2 | Detail Pending |  | pending |  |  |
| CLI23 | As an ada holder 
I want to build a transaction that includes a proposal (containing a governance action)
So that I can later sign and submit to the chain 
transaction build | Transaction build has a new flag to supply a proposal file as input for the transaction body | Detail Pending | pending | pending |  |  |
|  |  | When constructing a transaction body that includes a proposal, the resulting tx body conforms to the conway cddl so that proposal procedures are recorded with the key 20
transaction_body =
  { 0 : set<transaction_input>             ; inputs
  , 1 : [* transaction_output]
  , 2 : coin                               ; fee
  , ? 3 : uint                             ; time to live
  , ? 4 : certificates
  , ? 5 : withdrawals
  , ? 7 : auxiliary_data_hash
  , ? 8 : uint                             ; validity interval start
  , ? 9 : mint
  , ? 11 : script_data_hash
  , ? 13 : nonempty_set<transaction_input> ; collateral inputs
  , ? 14 : required_signers
  , ? 15 : network_id
  , ? 16 : transaction_output              ; collateral return
  , ? 17 : coin                            ; total collateral
  , ? 18 : nonempty_set<transaction_input> ; reference inputs
  , ? 19 : voting_procedures               ; New; Voting procedures
  , ? 20 : proposal_procedures             ; New; Proposal procedures
  , ? 21 : coin                            ; New; current treasury value
  , ? 22 : positive_coin                   ; New; donation
  }
 | Detail Pending | pending | pending |  |  |
| CLI24 | As a DRep, SPO or CC member
I want to build a transaction that includes my vote on a particular governance action
So that I can later sign and submit to the chain
transaction build | Transaction build has a new flag to supply a vote file as input for the transaction body | Detail Pending | pending | pending |  |  |
|  |  | When constructing a transaction body that includes a vote, the resulting tx body conforms to the conway cddl so that voting procedures are recorded with the key 19
transaction_body =
  { 0 : set<transaction_input>             ; inputs
  , 1 : [* transaction_output]
  , 2 : coin                               ; fee
  , ? 3 : uint                             ; time to live
  , ? 4 : certificates
  , ? 5 : withdrawals
  , ? 7 : auxiliary_data_hash
  , ? 8 : uint                             ; validity interval start
  , ? 9 : mint
  , ? 11 : script_data_hash
  , ? 13 : nonempty_set<transaction_input> ; collateral inputs
  , ? 14 : required_signers
  , ? 15 : network_id
  , ? 16 : transaction_output              ; collateral return
  , ? 17 : coin                            ; total collateral
  , ? 18 : nonempty_set<transaction_input> ; reference inputs
  , ? 19 : voting_procedures               ; New; Voting procedures
  , ? 20 : proposal_procedures             ; New; Proposal procedures
  , ? 21 : coin                            ; New; current treasury value
  , ? 22 : positive_coin                   ; New; donation
  }
 | Detail Pending | pending | pending |  |  |
| CLI25 | As an ada holder 
I want to build a transaction that includes a proposal (containing a governance action)
So that I can later sign and submit to the chain 
transaction build-raw | Transaction build-raw has a new flag to supply a proposal file as input for the transaction body | Detail Pending | pending | pending |  |  |
|  |  | When constructing a transaction body that includes a proposal, the resulting tx body conforms to the conway cddl so that proposal procedures are recorded with the key 20
transaction_body =
  { 0 : set<transaction_input>             ; inputs
  , 1 : [* transaction_output]
  , 2 : coin                               ; fee
  , ? 3 : uint                             ; time to live
  , ? 4 : certificates
  , ? 5 : withdrawals
  , ? 7 : auxiliary_data_hash
  , ? 8 : uint                             ; validity interval start
  , ? 9 : mint
  , ? 11 : script_data_hash
  , ? 13 : nonempty_set<transaction_input> ; collateral inputs
  , ? 14 : required_signers
  , ? 15 : network_id
  , ? 16 : transaction_output              ; collateral return
  , ? 17 : coin                            ; total collateral
  , ? 18 : nonempty_set<transaction_input> ; reference inputs
  , ? 19 : voting_procedures               ; New; Voting procedures
  , ? 20 : proposal_procedures             ; New; Proposal procedures
  , ? 21 : coin                            ; New; current treasury value
  , ? 22 : positive_coin                   ; New; donation
  }
 | Detail Pending | pending | pending |  |  |
| CLI26 | As a DRep, SPO or CC member
I want to build a transaction that includes my vote on a particular governance action
So that I can later sign and submit to the chain

transaction build-raw | Transaction build-raw has a new flag to supply a vote file as input for the transaction body | Detail Pending | pending | pending |  |  |
|  |  | When constructing a transaction body that includes a vote, the resulting tx body conforms to the conway cddl so that voting procedures are recorded with the key 19
transaction_body =
  { 0 : set<transaction_input>             ; inputs
  , 1 : [* transaction_output]
  , 2 : coin                               ; fee
  , ? 3 : uint                             ; time to live
  , ? 4 : certificates
  , ? 5 : withdrawals
  , ? 7 : auxiliary_data_hash
  , ? 8 : uint                             ; validity interval start
  , ? 9 : mint
  , ? 11 : script_data_hash
  , ? 13 : nonempty_set<transaction_input> ; collateral inputs
  , ? 14 : required_signers
  , ? 15 : network_id
  , ? 16 : transaction_output              ; collateral return
  , ? 17 : coin                            ; total collateral
  , ? 18 : nonempty_set<transaction_input> ; reference inputs
  , ? 19 : voting_procedures               ; New; Voting procedures
  , ? 20 : proposal_procedures             ; New; Proposal procedures
  , ? 21 : coin                            ; New; current treasury value
  , ? 22 : positive_coin                   ; New; donation
  }
 | Detail Pending | pending | pending |  |  |
| CLI27 | As an ada holder
I want to create a conway cddl-compliant stake registration certificate 
stake-address | Allows the user to provide credentials in any of the following forms:

Stake verification key
Stake verification key file 
Stake address
Stake script file | Detail Pending | pending | pending |  |  |
|  |  | Requires the user to provide the required key deposit in lovelace  | Detail Pending | pending | pending |  |  |
|  |  | The command has the flag –out-file to specify the file where the registration certificate will be saved.  | Detail Pending | pending | pending |  |  |
|  |  | The command handles errors gracefully and provides helpful error messages when required options are missing or invalid inputs are provided. | Detail Pending | pending | pending |  |  |
|  |  | The certificate should be saved on a text envelope format: 
{
    "type": "CertificateConway",
    "description": "Stake Address Registration Certificate",
    "cborHex": ""
}
 | Detail Pending | pending | pending |  |  |
|  |  | The resulting certificate conforms with the conway cddl, where 

reg_cert = (7, stake_credential, coin) | Detail Pending | pending | pending |  |  |
| CLI28 | As an ada holder
I want to create a conway cddl-compliant stake deregistration certificate to get my deposit back

stake-address | Allows the user to provide credentials in any of the following forms:

Stake verification key
Stake verification key file 
Stake address
Stake script file | Detail Pending | pending | pending |  |  |
|  |  | Requires the user to provide key deposit (in lovelace) that was paid by the target stake credential when it registered  | Detail Pending | pending | pending |  |  |
|  |  | The command has the flag –out-file to specify the file where the registration certificate will be saved.  | Detail Pending | pending | pending |  |  |
|  |  | The command handles errors gracefully and provides helpful error messages when required options are missing or invalid inputs are provided. | Detail Pending | pending | pending |  |  |
|  |  | The certificate should be saved on a text envelope format: 
{
    "type": "CertificateConway",
    "description": "Stake Address Deregistration Certificate",
    "cborHex": ""
}
 | Detail Pending | pending | pending |  |  |
|  |  | The resulting certificate conforms with the conway cddl, where 

unreg_cert = (8, stake_credential, coin) | Detail Pending | pending | pending |  |  |
| CLI29 | As an ada holder
I want to delegate my votes to a DRep (registered or default)
So that my stake is counted when the DRep vote.  

Stake-address

 | Allows the user to provide credentials in any of the following forms:

Stake verification key
Stake verification key file 
Stake address
Stake script file | Detail Pending | pending | pending |  |  |
|  |  | When delegating to a registered DRep, the user can provide the target Drep with: 
DRep script hash
DRep verification key
DRep verification key file 
DRep key hash (Drep ID)     | Detail Pending | pending | pending |  |  |
|  |  | When delegating to a default DRep the user can use a flag to select either always-abstain or always-no-confidence, but not both.   | Detail Pending | pending | pending |  |  |
|  |  | The command has the flag –out-file to specify the file where the vote delegation certificate will be saved.  | Detail Pending | pending | pending |  |  |
|  |  | The command handles errors gracefully and provides helpful error messages when required options are missing or invalid inputs are provided. | Detail Pending | pending | pending |  |  |
|  |  | The certificate should be saved on a text envelope format: 
{
    "type": "CertificateConway",
    "description": "Vote Delegation Certificate",
    "cborHex": ""
}
 | Detail Pending | pending | pending |  |  |
|  |  | The resulting certificate conforms with the conway cddl, where 

vote_deleg_cert = (9, stake_credential, drep) | Detail Pending | pending | pending |  |  |
| CLI30 | As an ada holder
I want to delegate my stake to a stake pool AND my votes to a DRep (registered or default) with a single certificate.
stake-address | Allows the user to provide credentials in any of the following forms:

Stake verification key
Stake verification key file 
Stake address
Stake script file | Detail Pending | pending | pending |  |  |
|  |  | The user can provide the target stake pool with: 
Stake pool cold verification key
Stake pool cold verification key file 
Stake pool ID    | Detail Pending | pending | pending |  |  |
|  |  | Allows the user to provide the target DRep credential with 

DRep script hash
DRep verification key
DRep verification key file 
DRep key hash (Drep ID)     | Detail Pending | pending | pending |  |  |
|  |  | When delegating to a default DRep the user can use a flag to select either always-abstain or always-no-confidence, but not both.   | Detail Pending | pending | pending |  |  |
|  |  | The command has the flag –out-file to specify the file where the stake and vote delegation certificate will be saved.  | Detail Pending | pending | pending |  |  |
|  |  | The command handles errors gracefully and provides helpful error messages when required options are missing or invalid inputs are provided. | Detail Pending | pending | pending |  |  |
|  |  | The certificate should be saved on a text envelope format: 
{
    "type": "CertificateConway",
    "description": "Stake and Vote Delegation Certificate",
    "cborHex": ""
}

 | Detail Pending | pending | pending |  |  |
|  |  | The resulting certificate conforms with the conway cddl, where 

stake_vote_deleg_cert = (10, stake_credential, pool_keyhash, drep) | Detail Pending | pending | pending |  |  |
| CLI31 | As any persona
I want to query the nodes for the current
Governance state 
So that I can inform my decisions | The new command is implemented as cardano-cli conway query gov-state

 | Detail Pending | pending | pending |  |  |
|  |  | The command requires the user to specify the network id (mainnet or testnet magic) | Detail Pending | pending | pending |  |  |
|  |  | The command has the flag –out-file to specify the file where the output  will be saved.  | Detail Pending | pending | pending |  |  |
|  |  | The output is a JSON showing, at least,  the following information:

Previous protocol parameters
Current protocol parameters
Last enacted governance actions IDs for committee, constitution, hardfork initiation and parameter updates
Ratified governance actions that will be enacted at next epoch transition
Active governance actions proposals including their type, stake address that collects the deposit, governance action id, expiration, spo, drep and cc votes  | Detail Pending | pending | pending |  |  |
|  |  | The command handles errors gracefully and provides helpful error messages when required options are missing or invalid inputs are provided. | Detail Pending | pending | pending |  |  |
| CLI32 | As a CC member 
I want to query the committee state
So that I can find my expiration term and whether my hot key authorization certificate has been recorded on chain
 | The command is implemented as cardano-cli conway query committee-state | Detail Pending | pending | pending |  |  |
|  |  | Requires the user to provide the network id  | Detail Pending | pending | pending |  |  |
|  |  | Supports a query for an specific CC credential 
CC cold verification key
CC cold verification key file
CC cold verification key hash
CC hot verification key
CC hot verification key file
CC hot verification key hash 
 | Detail Pending | pending | pending |  |  |
|  |  | When no CC key is specified, the command outputs information for all committee members | Detail Pending | pending | pending |  |  |
|  |  | The command allows filtering by active, expired and unrecognized members (registered hot keys to an unknown cc cold key)  | Detail Pending | pending | pending |  |  |
|  |  | The output is a JSON showing, the following information:

Cold key hash 
Hot credential status (Authorized/NotAuthorized) 
When Authorized, shows the hot key hash
Status (Active, Expired, Unrecognized) 
Expiration epoch
Current epoch (when you ran the query)
Quorum | Detail Pending | pending | pending |  |  |
|  |  | The command has the flag –out-file to specify the file where the output  will be saved.  | Detail Pending | pending | pending |  |  |
|  |  | The command handles errors gracefully and provides helpful error messages when required options are missing or invalid inputs are provided. | Detail Pending | pending | pending |  |  |
| CLI33 | As an ada holder
I want to query the DRep state 
So that …    | The command is implemented as cardano-cli conway query drep-state | Detail Pending | pending | pending |  |  |
|  |  | Requires the user to provide the network id  | Detail Pending | pending | pending |  |  |
|  |  | Supports a query for an specific DRep credential

DRep verification key
DRep verification key file 
DRep verification key hash (DRep ID) | Detail Pending | pending | pending |  |  |
|  |  | If no Drep credential is specified it returns all DReps | Detail Pending | pending | pending |  |  |
|  |  | The command has the flag –out-file to specify the file where the output  will be saved.  | Detail Pending | pending | pending |  |  |
|  |  | The output is a JSON showing, the following information:
Drep Key hash
Anchor (Drep metadata)
Deposit
Expiry (from Drep activity) | Detail Pending | pending | pending |  |  |
|  |  | The command handles errors gracefully and provides helpful error messages when required options are missing or invalid inputs are provided. | Detail Pending | pending | pending |  |  |
| CLI34 | As an ada holder and DRep
I want to query the DRep stake distribution
So that I can find the weight (of the votes) of each DRep | The command is implemented as cardano-cli conway query drep-stake-distribution | Detail Pending | pending | pending |  |  |
|  |  | Supports a query for an specific DRep credential

DRep verification key
DRep verification key file 
DRep verification key hash (DRep ID) | Detail Pending | pending | pending |  |  |
|  |  | If no Drep credential is specified it returns all DReps | Detail Pending | pending | pending |  |  |
|  |  | The command has the flag –out-file to specify the file where the output  will be saved.  | Detail Pending | pending | pending |  |  |
|  |  | The output is a JSON showing, the following information:
Drep Key hash
Stake delegated to this DRep | Detail Pending | pending | pending |  |  |
|  |  | The command handles errors gracefully and provides helpful error messages when required options are missing or invalid inputs are provided. | Detail Pending | pending | pending |  |  |
| CLI35 | As an ada holder,
I want to query my stake address information so that I can learn to which pool and drep Im delegating to and the value in lovelace of my deposits for delegating and for submitting governance actions.  | Expand the command query stake-address-info to return the drep id of the DRep that the stake credential is delegated to and the value of the existing deposits.  |  | pending | pending |  |  |
|  | Script as a DRep |  |  | pending | pending |  |  |
| Sidechain User Stories |  |  |  |  |  |  |  |
| CH.SID1 | As a Sidechain, I wish to use BLS primitives to record settlement operations on Cardano | posted your ‘thread comments’ to initiate
 | Detail Pending | pending | Detail Pending | Sidechain |  |
| CH.SID2 | Sidechain will use BLS for tokenomics, in particular to support multi-sig certificates about Sidechain activity that can be verified by Plutus contracts | Detail Pending | Detail Pending | pending | Detail Pending | Sidechain |  |
| Plutus Component Level User Stories |  |  |  |  |  |  |  |
| CIP-85 | As a DApp developer I would like to use sums-of-products instead of Scott-encoding in my Plutus scripts to get better performance | Sums-of-products is available to use in Plutus V3 scripts and is the default way of encoding data types in Plutus Tx. | Detail Pending | pending | pending | Plutus |  |
| CIP-101 | User stories for Keccak256 primitive | Detail Pending | Detail Pending | pending | pending | Plutus |  |
|  | As a DApp developer I want to use the Blake2b-224 hashing function to compute PubKeyHash onchain | The Blake2b-224 is available to use in Plutus V3 after the HF | Detail Pending | pending | pending | Plutus |  |

# 