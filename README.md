
# Diversity-Inclusion-Project
# Dashboard Link:https://app.powerbi.com/groups/me/reports/75f30d3c-c588-4f30-93a2-42e1c6616c9b/ReportSection7ea1278f6b81d81d8e4e?experience=power-bi&clientSideAuth=0

Human Resources at telecom client is highly into diversity and inclusion. They’ve been working hard to improve gender balance at the executive management level, but they’re not seeing any progress.

 Big company giants are often approached by clients seeking support with diversity and inclusion. Companies need a workforce of diverse talents and backgrounds to succeed in an increasingly complex and heterogeneous world. Diversity and inclusion are business imperatives, not just nice-to-haves. We aim for all of our teams to feel welcome and appreciated. But actually achieving this and unlocking its potential involves a whole set of practical challenges.

Why is this so?

Think about the importance of strategy, awareness and education, analytics and inspiration. 

Following measures are used in this Project:

 # of men = Calculate(distinctcount('HR Manager'[Employee ID]),Filter('HR Manager','HR Manager'[Gender]="Male"))

 # of women = Calculate(distinctcount('HR Manager'[Employee ID]),Filter('HR Manager','HR Manager'[Gender]="Female"))

 # of leavers = CALCULATE(COUNTA('HR Manager'[Employee ID]), 'HR Manager'[Leaver FY] IN { "FY20" })

 % employees promoted (FY21) = Divide(Calculate(distinctcount('HR Manager'[Employee ID]),Filter('HR Manager','HR Manager'[Promotion in FY21?]="Yes")),Calculate(distinctcount('HR Manager'[Employee ID]),Filter('HR Manager','HR Manager'[In base group for Promotion FY21]="Yes")))

% Promotees who were women = Divide(Calculate(distinctcount('HR Manager'[Employee ID]),Filter('HR Manager','HR Manager'[Gender]="Female")),distinctcount('HR Manager'[Employee ID]))

 % of hires men = Divide('HR Manager'[# of men],('HR Manager'[# of men]+'HR Manager'[# of women]))

 % of hires women = Divide('HR Manager'[# of women],('HR Manager'[# of women]+'HR Manager'[# of men]))

 % Turnover = Divide(Calculate(distinctcount('HR Manager'[Employee ID]),Filter('HR Manager','HR Manager'[FY20 leaver?]="Yes")),Divide(Calculate(distinctcount('HR Manager'[Employee ID]),Filter('HR Manager','HR Manager'[In base group for turnover FY20]="Y"))+Calculate(distinctcount('HR Manager'[Employee ID]),Filter('HR Manager',NOT('HR Manager'[Department @01.07.2020]=BLANK()))),2))

 men Avg Rating Men = Calculate(Average('HR Manager'[FY20 Performance Rating]),Filter('HR Manager','HR Manager'[Gender]="Male"))

 women Avg Rating Women = Calculate(Average('HR Manager'[FY20 Performance Rating]),Filter('HR Manager','HR Manager'[Gender]="Female"))


![Screenshot (16)](https://github.com/Zasrango/Diversity-Inclusion-Project/assets/169545862/30606944-d460-40fc-b0cf-c3aee968717b)
![Screenshot (17)](https://github.com/Zasrango/Diversity-Inclusion-Project/assets/169545862/3cc6a0f8-ae25-4a9d-a5e4-1bcd0de690ee)

