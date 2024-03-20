## Unauthorized to AI model and data

If the attacker just acts as a normal user, and output normal results as others do, then the attack can be detected like other use cases in SOC, such as abnormal logon for models or cloud spaces abnormal access, and DLP detection for data leakage.

If the unauthorized behaviours show effects on AI applications, there are some potential scenarios:
1. Evasion attacks:
Attempt to make a model output incorrect results by perturbing the data sent to the trained model.

Detection: detect input and output streams with policies.
Remediation: 1) Adversarial training 2) Gradient mask (for image inputs) 3) Randomization 4) Denoising

2. Unwanted output of sensitive training data
Detection: recognize focus spot of input data and detect in output streams
Remediation: filter and mask before output to user, and fine-tune models when detected

3. Training data poison

Happen when model update from external data uploaded by malicious user, will damage the availability and integrity of the model.
Detection: monitor the behaviour matrix of the model
Remediation: 1) filter with input policies and denoising 2) Regularly monitor and update the training datasets

4. Prompt injection (only in GenAI)
5. Training data and prompt leakage in cloud (especially GenAI)
6. Model denial of service

7. Transfer learning attack
Transfer learning attacks occur when an attacker trains a model on one task and then fine-tunes it on another task to cause it to behave in an undesirable way.
Remediation: 1) Regularly monitor and update the training datasets 2) Use secure and trusted training datasets 3) Implement model isolation 4) Use differential privacy 5) Perform regular security audits