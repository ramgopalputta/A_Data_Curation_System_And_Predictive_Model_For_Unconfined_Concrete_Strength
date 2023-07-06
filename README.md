# PREDICTIVE MODEL FOR UNCONFINED CONCRETE STRENGTH


# ABSTRACT
This project aims to improve data management in the construction industry by providing a comprehensive solution that delivers clean data and the development of a machine learning model to predict concrete strength and understand the key factors affecting it. The team, consisting of Data Science graduate students at Seattle University and liaising with a leading structural engineering firm, DeSimone Consulting Engineering, establishes a feasible approach demonstrating the potential for using technology to improve data management processes in the construction industry and will provide a comprehensive solution for the company's data analysis challenges. The solution extracts data from PDF files and transforms it into a structured format. 
The team then develops a machine learning model to predict concrete strength based on the extracted data. This project enables the construction company to have better insights into concrete strength and its influential variables, make better business decisions, and improve the overall efficiency of their operations.

# 1. INTRODUCTION
DeSimone Consulting Engineers (DCE) is a leading firm in the structural engineering, 
facade consulting, and forensic services industries. DCE provides a comprehensive range of 
services (Desimone, n.d.) for all types of buildings, with 14 offices in 4 countries and 
headquartered in New York City. DCE is highly regarded for its expertise in concrete engineering 
and for delivering high-quality engineering services for projects of varying sizes and complexity. 
Concrete is a vital composite material used in construction that consists of cement, water, 
and aggregates (such as sand, gravel, or crushed stone). Its importance lies in its strength, 
durability, and ability to withstand various environmental conditions. To test this, wet concrete 
samples are collected from construction sites, molded into a cylindrical shape (Fig. 1(a)), and are
then subjected to strength testing using a specialized machine that can apply a compressive load 
to the sample (Fig. 1(b)). The machine measures the force required to compress the sample, 
allowing engineers to determine the compression strength of the material. What sets this 
measurement apart is that it is not restricted or confined, allowing for lateral expansion while 
undergoing compression. As a result, this particular strength is referred to as unconfined 
compression strength. The reason for collecting these wet samples is to test their strength in the 
lab based on their location of placement, which is crucial for ensuring the structural integrity of 
the concrete.
![image](https://github.com/ramgopalputta/Predictive_Model_For_Unconfined_Concrete_Strength/assets/114395443/e29901ff-1dc1-4cf2-b0de-bfc4b86c3e49)

The challenge DCE faces is that it collects an abundance of field concrete samples for 
determining unconfined compressive strength, creating a vast dataset. However, currently, DCE 
lacks an efficient system to effectively store, analyze and utilize this data. This data includes details
about the site, including city, project type, building height or number of floors, ambient 
temperature; details about the concrete used in the building, like concrete Mix ID, concrete 
temperature, structural element, location of placement, and water added; and details about the 
testing sample like unit weight, air content, slump, specimen size, and date tested. The contractor 
usually presents this data to DCE in PDF format, but there is currently no system in place to 
effectively process and make use of this information. This makes it challenging for a practicing 
structural engineer to find the predominant mix design for elements in a geographic area for 
specific building types and to understand the performance of high-strength mixes in hot and cold 
cycles. This information could help identify the most successful mixes and highlight any issues 
with mixes that have strength problems.
Currently, DCE's approach for collecting and analyzing this data includes obtaining readymix concrete loads from the contractor, collecting cylindrical modeled specimens, and sending 
them to the labs for testing the unconfined concrete strength for 56 days. The results of these tests 
are then sent to the DCE's shared drive, where the engineers review them manually, and make 
decisions accordingly. Despite collecting a vast dataset of field concrete samples for unconfined 
compressive strength, DCE currently lacks an efficient system for effectively analyzing and 
utilizing this data. This poses several challenges for engineers, such as difficulties in identifying 
suitable mix designs for specific building types and elements or determining which high-strength 
mixes are performing well or have strength issues. The current network-attached storage 
exacerbates the problem, making it challenging to locate and retrieve specific reports efficiently. 
Therefore, a formalized framework for data storage, retrieval, and analysis is urgently needed. 
Furthermore, DCE requires a machine learning model to predict concrete strength and understand 
how the key influencing factors affect it under real-world conditions, such as local temperature 
variations. A systematic approach to data collection, cleaning, preprocessing, and modeling is 
necessary to uncover meaningful insights and patterns.

