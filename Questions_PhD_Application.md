# Reconstruct Your Previous Conversations! Comprehensively Investigating Privacy Leakage Risks in Conversations with GPT Models
* Introduce the threat model of the proposed attack.
* Is there any difference between this threat model and the threat model of membership inference attack against in context learning?
* Introduce the real-world attack scenarios.
* Introduce the UNR attack.
* Introduce the PBU attack.
* What is the intuition to design the PBU attack? In other words, why the authors think the PBU attack could work?
* The authors provide a section about Root Cause Analysis. Please introduce this part?
* Do you agree with this cause analysis? Or you think there are some other reasons to explain why these attacks could succeed.?
* In the paper, the authors test three possible defenses. And according to the results, the few-shot based defense could not work well against PBU attack and even make the target models more vulnerable. Why does this happen?
* In this paper, we propose a new attack. Do you think this attack could work on the in context learning domain? For example, could we use this attack to reconstruct the examples of in context learning?
* We could use this new attack to reconstruct the examples, so why we still need to do MIA of in context learning?
