# Lateral Movement Datasets - LMD Dataset Collections

LM Datasets (LMD) is the first, to our knowledge, EVTX origined dataset and currently the only benchmark corpus comprising of Sysmon logs. Two separate folders are enclosed within the specified git repository, namely **LMD-2022** and **LMD-2023** respectively. The former is related to the first version of LMD that was created in 2022 as supplementary experimental material for the presented Endpoint-Detection and Response policy in **Smiliotopoulos, C.; Barmpatsalou , K.; Kambourakis, G. Revisiting the Detection of Lateral Movement through Sysmon. Appl. Sci. 2022, 12, 7746. https://doi.org/10.3390/app12157746**. On the other hand the latter is the enhanced equivalent of the 2022 version with more LM attacks and various versions to serve as the base for the execution of LM Machine Learning (ML) experiments, both Shallow and Deep Learning.

## LMD-2022

The **2022 LMD version (LMD-2022)** incorporates normal and malicious traffic logs originated from the execution of nine state-of-the-art LM techniques, including four variants of the so-called * *Exploitation of Remote Services* * LM methodology and five equivalents * *credential exploitation techniques* * . The attacks were recorded under the MS Windows Domain testbed presented in **https://doi.org/10.3390/app12157746**. Specifically, the nine assaults range from the execution of the legacy Exploitation of Remote Services techniques via the * *ms17-010* * , * *EternalBlue* * and * *Bluekeep* * Windows vulnerabilities, to the more advanced deployment of the * *WannaCry* * malware and more elevated ones, including * *Pass the Hash (PtH)* * , * *Pass the Ticket (PtT)* * , * *Golden Ticket (GT)* * , * *Silver Ticket (ST)* * and credential exploitation with * *LaZagne Project tool* * .

As shown in the highlighted box that follows, the LMD-2022 corpus comprises four subsets that were thoroughly presented in **https://doi.org/10.3390/app12157746** , namely * *Normal* *, * *NormalVsMalicious01* * , * *NormalVsMalicious02* * , and * *FullSet* *. Specifically, the * *Normal* * subset incorporates logs related to legitimate network traffic that were collected prior and during the execution of nine executed LM techniques, namely * *Exploitation of Remote Services (EoRS)* * (four variants of EoRS techniques) and * *Exploitation of Hashing Techniques (EoHT)* * (five variants of EoHT techniques). More precisely, * *NormalVsMalicious01* * set of logs encloses the traffic that was captured before, during and upon termination of the * *Exploitation of Remote Services (ERS)* * attacks category, while * *NormalVsMalicious02* * comprises logs collected during the execution of the five aforesaid distinct credentials exploitation techniques. Both, * *NormalVsMalicious01* * and * *NormalVsMalicious02* * are mixed with normal traffic logs respectively. Finally, * *FullSet* * is the fusion of the three aforesaid distinct subsets.
		**LMD-2022 Contents:**
		- Normal 80,000 (Legitimate network traffic (LNT))
		- NormalVsMalicious01 290,000 (LNT, EoRS (ms17-010, EternalBlue, Bluekeep, WannaCry))
		- NormalVsMalicious02 415,000 (LNT, EoHT (PtH, PtT, GT, ST [via Mimikatz], LaZagne Project))
		- FullSet 870,000 (LNT, EoRS, EoHT)
    
## LMD-2023

For the need of the work that is entitled * *On the Detection of Lateral Movement through Supervised Machine Learning and ETCExp Tool (Submitted-Under Review in the International Journal of Information Security [https://www.springer.com/journal/10207/])* * , the LMD-2022 logset was enhanced with both normal and malicious traffic collected from various personal and virtual machine (VM) computing stations. Precisely, the already existing nine LM techniques were re-executed multiple times and populated with six more up-to-date state-of-the-art LM techniques, which correspond to Common Vulnerabilities and Exposures (CVEs) IDs issued from 2020 until today. As shown in the highlighted box that follows, , the added attacks (those having an asterisk affixed) include * *Log4Shell* * , * *Follina* * , * *Windows Spooler Privilege Escalation* * , * *SMBGhost* * , * *SMBleed* * , and * *Zerologon* * , each of them executed multiple times.

		- ms17-010 **CVE-2017-0148 (EoRS)**
		- EternalBlue **CVE-2017-0144 & EoRS**
		- Bluekeep **CVE-2019-0708 & EoRS**
		- WannaCry **CVE-2017-0143, CVE-2017-0145, CVE-2017-0146 & EoRS**
		- Mimikatz (EoHT) **CVE-2021-36934 & EoHT**
		- LaZagne Project **CVE-2021-40444 & EoHT**
		- Log4Shell **CVE-2020-1472, CVE-2021-44228 & EoRS**
		- Follina **CVE-2022-30190 & EoRS**
		- Windows Spooler Privilege Escalation **CVE-2022-29104 & EoRS**
		- SMBGhost **CVE-2020-0796 & EoRS**
		- SMBleed **CVE-2020-1206 & EoRS**
		- Zerologon **CVE-2020-1472 & EoRS**

The resulted LMD-2023 dataset, which is used in the context of the aforementioned work, comprises a full set of 1,752,890 log samples (EventIDs). LMD-2023 is offered in both CSV and Sysmon's generic EVTX (raw .xml data) formats. The CSV file contains 93 features extracted with the ETCExp which is available in * *[https://github.com/ChristosSmiliotopoulos/evtx_To_CSV_ExportTool]* *. 16 distinct EventIDs (out of the total 27 presented in Sysmon's manual * *[https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon]* *) are identified within LMD-2023. Note that the rest 11 Sysmon EventIDs, such as EventID_6 (Driver loaded), Event_8 (CreateRemoteThread) etc., are not present in LMD-2023 due to the nature of the implemented EoRS and EoHT techniques. The analysis of the included in LMD-2023 Sysmon EventIDs are presented as follows:

		- EventID 1:Process creation \\
		- EventID 2:A process changed a file creation time \\
		- EventID 3:Network connection \\
		- EventID 4:Sysmon service state changed\\
		- EventID 5:Process terminated \\
		- EventID 7:Image loaded \\
		- EventID 10:ProcessAccess \\
		- EventID 11:FileCreate \\
		- EventID 12:RegistryEvent (Object create and delete) \\
		- EventID 13:RegistryEvent (Value Set) \\
		- EventID 16:ServiceConfigurationChange \\
		- EventID 17:PipeEvent (Pipe Created) \\
		- EventID 18:PipeEvent (Pipe Connected)\\
		- EventID 22:DNSEvent (DNS query) \\
		- EventID 23:FileDelete (File Delete archived)* \\
		- EventID 255:EventID 255: Error* \\


The contents of the LMD-2023 dataset is presented in the highlighted box below. It should be noted that three different versions (considering the number of each dataset's samples) are included as follows:

		**LMD-2023 Contents:**
		- LMD-2023 (1.75M Elements)
		- LMD-2023 (1.87M Elements)
		- LMD-2023 (2.31M Elements)
		
**Each version of the LMD-2023 dataset encloses a raw unmodified version, the labelled equivalent and three different subsets each including Normal, EoRS and EoHT traffic respectively.**
