# BizCardX-Extracting-Business-Card-Data-with-OCR
NAME : SRINIVASAN M
BATCH: DW77
DOMAIN : DATA SCIENCE
Linkedin : https://www.linkedin.com/in/srinivasan-m-754033bb/

# BizCardX-Extracting-Business-Card-Data-with-OCR
## Project Overview
BizCardX is an innovative application designed to simplify and streamline the process of extracting and managing business card information. Leveraging cutting-edge OCR (Optical Character Recognition) technology, this app allows users to effortlessly extract text details from business card images. The application integrates a user-friendly Streamlit GUI for a seamless and intuitive experience.

## Libraries/Modules used for the project!
   - Pandas - (To Create a DataFrame with the scraped data)
   - Postgresql - (To store and retrieve the data)
   - Streamlit - (To Create Graphical user Interface)
   - EasyOCR - (To extract text from images)
   - cv2 - (For reading and writing images, image manipulation, computer vision tasks, and more)
   - os - (To perform various operations related to file and directory manipulation, such as navigating the file system, creating directories, deleting files)
   - re (Regular Expressions) - (For text processing)

## Workflow

   To get started with BizCardX Data Extraction, follow the steps below:

- Install the required libraries using the pip install command. Streamlit, psycopg2, pandas, easyocr.
   
      pip install [Name of the library]

- Execute the **“bizcardx.py”** using the streamlit run command in the terminal command prompt.

      streamlit run bizcardx.py

- A webpage is displayed in browser, I have created the app with three menu options namely **HOME, UPLOAD & EXTRACT, MODIFY** where user has the option to upload the respective Business Card whose information has to be **extracted, stored, modified or deleted** if needed.

- Once user uploads a business card, the text present in the card is extracted by **easyocr** library.

- The extracted text is sent to get_data() function(user defined- I have coded this function) for respective text classification as company name, card holder name, designation, mobile number, email address, website URL, area, city, state, and pin code using loops and some regular expression.

- The classified data is displayed on screen which can be further edited by user based on requirement.

- On Clicking **Upload to Database Button** the data gets stored in the MySQL Database. (Note: Provide respective host, user, password, database name in create_database, sql_table_creation and connect_database for establishing connection.)

- Further with the help of **MODIFY** menu the uploaded data’s in SQL Database can be accessed for **Read, Update and Delete** Operations.
