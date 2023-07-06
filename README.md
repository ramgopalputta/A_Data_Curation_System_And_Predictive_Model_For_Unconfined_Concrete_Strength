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

# 2. METHODOLOGY

# 2.1. About the data
The dataset used in this project comprises of Unconfined Concrete Strength test results for 
each set of specimens from various construction sites, produced by testing agencies. The data is 
currently in PDF format and needs to be extracted. Reports produced by two independent testing 
agencies were used for this project, which contain essential details related to Site, Concrete and 
Test specimens collected from wet concrete mixtures. Since the current storage system hinders 
data analysis due to its nested directories on a network-attached storage system, there is a need for 
a structured data such as a clean Excel file that categorizes and minimizes data redundancy, 
facilitating easy retrieval and analysis for engineers. This structured data enables accurate 
predictions of Unconfined Concrete Strength.

# 2.2. Designed solution
To address these problems, a robust framework is implemented, consisting of two major 
components – The Data Curation System and The Predictive System.
The Data Curation System is responsible for collecting, cleaning, and organizing the data 
for analysis. It involves scraping the data from PDF files, storing them in a structured tabular 
format, and integrating the data into a unified format before transferring them to Excel files. This 
ensures data integrity by eliminating redundancy and inconsistency. The Predictive System then 
utilizesthe curated data to develop predictive models using advanced machine learning algorithms, 
enabling DCE to accurately predict mix designs for engineering structures in specific temperature 
ranges and geographic areas.

# 2.3. Data curation system
The data curation system was developed in Python to extract and analyze the Unconfined 
Concrete Strength test data from PDF lab reports. This is accomplished through the utilization of 
text scraping techniques, using various Python libraries like Pypdfium2, Pdfplumber, Camelot and 
Tabula. These python libraries are implemented to scrape the data from different sections of the 
PDF document, including the header, footer, and body. This ensures that all relevant information 
is captured accurately and efficiently.

After extracting the necessary data from the PDF files, the next step is data cleaning. The 
Unconfined Concrete Strength test results are manually entered into the PDF format by the testing 
agencies, increasing the likelihood of errors such as incorrect field names and naming formats. To 
ensure data accuracy and integrity, the cleaning process includes the identification and correction 
of such errors. This is done using a series of conditions and codes that can also be used for future 
corrections. The cleaning process involves several stages, such as removing redundant data, filling 
in missing values, and correcting inconsistencies.
After completing the data cleaning process, the data is organized into multiple tables with 
predefined data schemas. Data schemas provide a structured framework for managing and 
organizing data within a data management system. They define field data types and establish 
relationships between tables by assigning primary keys and foreign keys. A primary key serves as 
a unique identifier for a record within a table, while a foreign key is a field in one table that 
references the primary key in another table, establishing connections and relationships between 
them. This ensures that the data is stored in a structured and organized format across different 
tables, making it easier for DCE engineers and analysts to extract valuable insights and draw 
conclusions from the data. The data curation system exports data into three clean data files:

a. Project Information: This file is created by DCE analysts and contains information related 
to a project, such as the project name, building type, number of levels, height, address, site 
latitude and longitude etc.
b. Specimen Field Report: This file includes field or site data, such as the site weather, 
concrete mix ID, concrete supplier, time of specimen molding, specimen temperature, 
specimen density, air content, required compression strength of the specimen, and other 
related data points.
c. Specimen Compression Test Report: This file includes data related to the compression tests 
conducted by a testing agency, such as date of the test, specimen age in days, load at which 
the specimen broke, and other relevant data points.

This structured data is then utilized in the designing of a predictive system, which uses 
sophisticated machine learning techniques to create models that can accurately predict the 
Unconfined Concrete Strength of a concrete specimen.

# 2.4. Predictive system
Choosing a suitable machine learning algorithm for a given problem depends on several 
factors, such as the type of data, and the desired outcome. In this case, the obtained data is labeled, 
and therefore a supervised learning method is appropriate. Additionally, since the target attribute
to be predicted is a continuous numerical value, the problem falls into the category of regression.
After considering all the above factors, an artificial neural network model was chosen to
predict the Unconfined concrete strength with high accuracy and identify the key influencing 
factors that affect the concrete strength in real-world conditions such as variations in local 
temperature. This helps an engineer to make even better-informed decisions. The subsequent 
section provides a detailed description of the model and its specifications.


