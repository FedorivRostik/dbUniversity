# Rostyslav Fedoriv
## Entity-Relationship Diagram (ERD) for Coursework Grades

### Table: CourseWorkGrades
- **Grade_ID** int [pk]
- **Application_ID** int [ref: > ProjectApplications.Application_ID]
- **Quality_of_Work** int [note: '0-80']
- **Correspondence_to_Content** int [note: '0-15']
- **Disclosure_of_Theoretical_Aspects** int [note: '0-15']
- **Independence_Level** int [note: '0-10']
- **Volume_of_Materials** int [note: '0-10']
- **Compliance_with_Formatting** int [note: '0-10']
- **Defense** int [note: '0-20']
- **Presentation_of_Results** int [note: '0-10']
- **Answers_to_Questions** int [note: '0-10']
- **Final_Grade** int [note: '0-100']
- **All_Grades_Set** boolean [note: 'Indicates whether all grades are set']

### Table: ProjectApplications
- **Application_ID** int [pk]
- **Student_ID** int [ref: > Students.Student_ID]
- **Topic_ID** int [ref: > ProjectTopics.Topic_ID]
- **Status** varchar

### Table: Students
- **Student_ID** int [pk]
- **Last_Name** varchar
- **First_Name** varchar
- **Group** varchar
- **Email** varchar
- **Phone** varchar

### Table: ProjectTopics
- **Topic_ID** int [pk]
- **Title** varchar
- **Description** text
- **Professor_ID** int [ref: > Professors.Professor_ID]
- **Availability** varchar

### Table: Professors
- **Professor_ID** int [pk]
- **Last_Name** varchar
- **First_Name** varchar
- **Department** varchar
- **Email** varchar
- **Phone** varchar

### Table: TopicAllocation
- **Allocation_ID** int [pk]
- **Topic_ID** int [ref: > ProjectTopics.Topic_ID]
- **Student_ID** int [ref: > Students.Student_ID]

## Additional Information:
- **Diagram Format:** [dbdiagram.io](https://dbdiagram.io)
- **Link to Diagram:** [ERD Diagram](https://dbdiagram.io/d/url_shorter-64e2414c02bd1c4a5e147f95)

  
 ![DB Diagram](https://github.com/FedorivRostik/dbUniversity/assets/45173800/d07ce331-9759-45ef-a634-917397d64760)
