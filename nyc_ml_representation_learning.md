## Representation learning for behavior classification in network traffic

[Michal Sofka](http://www.cs.rpi.edu/~sofka/)
4/27/2017
[NYC Machine Learning Meetup](https://www.meetup.com/NYC-Machine-Learning/events/239327492/)

Malicious traffic on 100% of corporate networks

40mm anomalous incidents >> low thousands of malicious traffic

Antivirus has high precision low recall >> doesn't generalize well

Use proxy logs flow features
Hard to distinguish between auto generated domain names
Use URL as communication channel

557 features from URL (ratio of upper case letters, digits, num of special characters)
Use random forests classifier

Learned representation
Build a model which will be robust to malware modifications in the future
Divide flow into single-flow, static, and dynamic
Bag is communication between one user/device and hostname

Use self similarity matrix - invariant to future attacker changes
2d tsne shows flow based features are good for individual malware families

Sequential features
LSTM cell to build rnn (classify on URL strings)
Also look at flow sequences

Next step in unsupervised learning!  Learning malware traffic automatically.


#### cluster >> compare positive rate >> self similarity amtrix ####