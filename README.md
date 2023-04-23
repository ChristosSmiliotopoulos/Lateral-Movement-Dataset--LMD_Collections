# Lateral Movement Datasets - LMD Dataset Collections

LM Datasets (LMD) is the first, to our knowledge, EVTX origined dataset and currently the only benchmark corpus comprising of Sysmon logs. Two separate folders are enclosed within the specified git repository, namely LMD-2022 and LMD-2023 respectively. The former is related to the first version of LMD that was created in 2022 as supplementary experimental material for the presented Endpoint-Detection and Response policy in Smiliotopoulos, C.; Barmpatsalou , K.; Kambourakis, G. Revisiting the Detection of Lateral Movement through Sysmon. Appl. Sci. 2022, 12, 7746. https://doi.org/10.3390/app12157746. On the other hand the latter is the enhanced equivalent of the 2022 version with more LM attacks and various versions to serve as the base for the execution of LM Machine Learning (ML) experiments, both Shallow and Deep Learning.

The 2022 LMD version (LMD-2022) incorporates normal and malicious traffic logs originated from the execution of nine state-of-the-art LM techniques, including four variants of the so-called Exploitation of Remote Services LM methodology and five equivalents credential exploitation techniques. The attacks were recorded under the MS Windows Domain testbed presented in Smiliotopoulos, C.; Barmpatsalou , K.; Kambourakis, G. Revisiting the Detection of Lateral Movement through Sysmon. Appl. Sci. 2022, 12, 7746. https://doi.org/10.3390/app12157746. Specifically, the nine assaults range from the execution of the legacy Exploitation of Remote Services techniques via the ms17-010, EternalBlue and Bluekeep Windows vulnerabilities, to the more advanced deployment of the WannaCry malware and more elevated ones, including ``Pass the Hash'' (PtH), ``Pass the Ticket'' (PtT), ``Golden Ticket'' (GT), ``Silver Ticket'' (ST) and credential exploitation with \textit{LaZagne Project} tool.
