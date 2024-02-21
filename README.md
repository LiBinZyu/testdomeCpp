**Sliding Window**

Your company is analyzing malware which targets numerical record files.
The malware uses a sliding window over the array of numbers in a file, and tries to match the following pattern:
Tl, -, -, X, -, -, -, Tr
The entire window is moved so that 'X' passes through all the values and is compared to the numbers at the 'TI' and 'Tr' locations, which are positioned at a constant offset to 'X.
The malware has the following rules:
• If the value at the 'T!' or 'Tr' position of the pattern is bigger or equal to the value at the 'X' position, the malware replaces the value at 'X' with o.
• If the value at the 'TI' or 'Tr offset is out of bounds, then the value at 'X' is only compared to the other existing value.
• The record is processed in two stages: first, all the positions that should be set to 0 are located, using the original values for comparison. Only after all positions have been identified do they get set to 0.
For example, if the values in a record file are the following:
11, 2, 0, 5, 0, 2, 4, 3, 3, 3}
The expected values after the malware runs are:
{1, О, О, 5, 0, 0, 0, 3, 3, 0}
In this example, both '2's, the '4' and the last '3' were replaced by 0.
Implement the simulate function so that the malware behavior is replicated for further study.
