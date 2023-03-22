# PREDICTIVE MODEL FOR UNCONFINED CONCRETE STRENGTH

Utilized Data Science and Analytics in a real-time development project for the client DeSimone Consulting Engineers (DCE), a leading firm in structural engineering. DCE faces a challenge with managing a large dataset of concrete test results collected from construction sites, presented in PDF format by contractors. Their current network-attached storage system complicates data retrieval and analysis. The project involved scraping data from PDF files using Python libraries like pdfplumber, Camelot, etc., and transforming it into a structured format with defined schemas. Designed a Machine Learning model that predicts compressive strength, enabling DCE to predict concrete mix designs for structures in specific temperatures and geographic locations, enhancing DCE's operational efficiency and decision-making abilities.


# PROBLEM STATEMENT

DCE currently has network-attached storage consisting of numerous files, which makes it
difficult to locate and retrieve specific reports in an efficient manner. Additionally, this format
poses a significant challenge for conducting any data analysis and data mining. A formalized
framework for data storage, retrieval, and analysis needs to be established. Furthermore, DCE
needs a machine learning model to predict the concrete strength and help determining how the key
influencing factors affect the concrete strength under real-world conditions such as variations in
local temperature. This requires a systematic approach towards data collection, cleaning,
preprocessing, and modeling to uncover meaningful insights and patterns from the data.
The dataset consists of Unconfined Concrete Strength test results for each set of specimens
from various construction sites that were tested in the lab. These files are currently stored in PDF
format and require extraction. This extraction process will be achieved through the use of text-
scraping techniques. Once the data is extracted, it will be transformed into a structured format,
such as a table. After this transformation, the data will be exported to an Excel file for proper data
analysis and building a model to predict the factors influencing the concrete strength. In the end,
DCE needs a comprehensive solution that addresses its current challenges in data storage and
analysis. The deliverables for the project should include clean, structured Excel files of unconfined
concrete strength measurements, along with the source code used in the model development and
data curation. The solution should also include machine learning model that can predict the
concrete strength value and understand how these variables affect concrete strength. Additionally, a presentation platform, such as a network-located Python Notebook or online dashboard, should
be provided to allow users to make unconfined concrete strength predictions for the main input
parameters collected, as well as including geospatial input. The organization also needs a method
to incorporate additional project source data into the dataset in the future. DCE will provide data
for a multitude of projects over a diverse geographic area, so it is important that the system is
flexible and easy to use for their staff in the future.


# REQUIREMENTS

STRUCTURED DATA:

DCE has a specific need for extracting structured data from PDF files,
and this requires the use of a PDF scraper. The PDF documents containing the unconfined concrete
compression test data are presented to the contractor in a PDF format, which requires the required
field values to be scraped from the PDF document and structured in a tabular format. To ensure
that data ingestion is efficient and accurate, it is essential that the scrapper can read all the files
from provided directories and export the data read from the given two PDF formats into Excel files
that are true to the source PDF, with no duplicate data ingested. Moreover, it is critical that the
exported data is in adequate schemas for efficient joining of data files, which would make it easier
for engineers to access and analyze the data. The proper structuring of data is key to making it easy
to understand and analyze, and this would ensure that the data is not only accurate but also easy to
use.
The current storage system of nested directories on a network-attached storage system
makes it difficult for engineers to analyze the data. Hence, there is a need for clean exported Excel
files to categorize and minimize data redundancy, enabling easy retrieval and analysis by
engineers. Additionally, a presentation platform will be developed, although the type of platform
is yet to be decided. To ensure scalability and flexibility of the solution, a method for incorporating
additional project source data into the dataset in the future will also be implemented.


PREDICTUVE MODEL: 

DCE also needs a highly accurate, scalable, and easy-to-use machine
learning model that can predict the unconfined compressive strength of wet concrete samples. The
model will utilize data collected from concrete inspection details such as weather, ambient
temperature, required load, concrete field inspection details such as lab number, concrete
temperature, density, concrete inspection test results such as date tested, age days, unit load, along
with the type and location of the structure member in the building. The problem requires a
supervised learning which can fit a non-linear relationship between the input and output variables,
and the output should be a numerical value. This makes the problem a regression problem, which
requires a model that can accurately predict continuous numerical values. The team will evaluate
and compare multiple models before selecting the best one for the client.
Building an effective Machine Learning model that predicts the unconfined compressive
strength is crucial for DCE. It will allow them to predict accurate mix designs for engineering
structures in a particular temperature range and geographic area. Additionally, it helps in
determining what types of high-strength mixes can be used in each geographic location and
recording the break history during hot and cold climates. This information will be used to improve
the quality of the concrete mixes and ensure that the structures are safe and of good quality. It is
also important to note that for a given structure member, the predicted load that the concrete can
withstand before failure should be almost equal to its expected strength value.


