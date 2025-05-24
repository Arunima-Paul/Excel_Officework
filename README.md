Here a small part of ETL, Data Cleaning in Power Query and Power Pivot in MS Excel are shown here. 
The presentation is a practical case study of my office work, showcasing data cleaning , analysis and 
reporting using MS Excel and Power Query in the banking domain, specifically within the Small and Medium Enterprises (SME) portfolio.

Please check the video presentation here : https://youtu.be/Jo13p_jKl0k

**Purpose and Sensitivity-**
This project centers around data sent from my controlling office to support monitoring and follow-up of SME performance across branches. 
The goal is to enhance SME growth using a Business Rule Engineering (BRE) model crafted by the bank. 
Due to the sensitive nature of the customer data, traditional data sharing methods such as external emails or screen recordings were restricted, 
therefore I used screenshots of each process to showcase the analysis.

1. I imported two datasets pertaining to customers with sanctioned amounts between ₹10-50 lakhs and ₹50 lakhs and above.
2. Each dataset is housed within a "Granular" worksheet which are loaded into Power Query for transformation.
3. A blank query is created for this purpose and both queries are renamed for clarity which is an important best practice for long-term reference.
4. The two datasets, each with matching column headers, are appended into a unified table.

![thumb_2](https://github.com/user-attachments/assets/363f1bbe-a829-4db2-879c-6bd2d3c856a6)

**5. The data cleaning phase is shown as below:**
(i) Filtering by module: Only records from “BIDHANNAGAR” are retained, filtering via the MOD_NAME column.

(ii) Replacing NULLs:
SMECC_RACC_CODE nulls replaced with CUSTOMER_BRN_CODE
SMECC_RACC_NAME nulls replaced with CUSTOMER_BRN_NAME
Conditional Columns were added in Power Query for this process.

(iii) Sanction Date (SANC_DT) cleanup: Nulls from Sanction Date are excluded because we only require the Sanctioned records, Null in date means these loans are not yet sanctioned by branch.

(iv) Module standardization: There were three variations of “Bidhannagar” in the module name. These are consolidated into “BIDHANNAGAR MODULE” for uniformity.

(v) Each step is carefully renamed in Power Query for traceability and future auditing which is important for sound data practices.

**6. Building the Report-**
With a clean and transformed dataset I then proceeded to generate reports using Pivot Tables:

(i) SANC_DT in rows initially yielded calendar-based quarters which was inaccurate.

(ii) To mitigate this Custom fiscal year columns created:

FY_MONTH and FY_QTR are generated from SANC_DT using formulas, aligning with the bank’s fiscal year starting 01.04.2024.

![FY Formula 1](https://github.com/user-attachments/assets/cfb71bc6-bdc1-4c2a-a7dd-1e216cae86c7)

![FY Formula 2](https://github.com/user-attachments/assets/ae43c59b-37d5-4ae9-9510-7a90a4dcd8b8)

To validate Filters are applied on months to cross-check that FY_QTR values match expectations.

**7. Preparing the Final Report-**
(i) In the Pivot Table correct FY_QTR is used now to create MTD reports for December 2024.

(ii) Lastly summary report is prepared by copmying the Pivot Table in another sheet
and fine-tuning the formatting: Borders, font changes, Merging and resizing cell heights,
rounded to 2 decimal places.

This resulted in a professional-quality report which is ready for printing and submission.

![thumb_3](https://github.com/user-attachments/assets/82bd4bad-13da-4cac-8675-582668a6ebdb)

![CPC report](https://github.com/user-attachments/assets/8c774529-c286-490d-b2ac-13692cb28845)

**Conclusion-**
This presentation illustrates how day-to-day data analysis is conducted using Power Query, Pivot Tables and Excel’s built-in features. 

It reflects the core of a data analyst’s role:

Understanding business logic

Cleaning and transforming data

Generating stakeholder-ready reports

Thank You
Arunima Paul

