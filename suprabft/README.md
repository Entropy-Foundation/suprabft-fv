This is the repository for the formal specification of the chained Moonshot protocol in IVy, as well as the proof of safety of the protocol.

Following are the relevant files:
-types.ivy: declaration of the extended datatypes we use. Also has some basic invariants.

-network.ivy: the network model; almost identical to the model used in other similar IVy models, except for the message types.

-moonshot.ivy: the chaine moonshot protocol specification.

-quorum_verification.ivy: monitors to verify that quorums are valid.

safety.ivy: the inductive invariants proving safety.

ubd_seq.ivy: declaration of the unbounded sequence data type, used for rounds and heights. Identical to the standard library module unbounded_sequence, except for a small difference in the definition of succ relation.

All the files are self-documented with comments. With a working installation of IVy (can be obtained from https://github.com/kenmcmil/ivy), run the command ivy_check trace=true complete=fo safety.ivy to verify the correctness.