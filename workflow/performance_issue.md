# Solving hub performance issues

Certain large courses or courses with complex software/compute requirements can consume lot of memory/cpu which can result in poor user experience for students and/or increased cloud costs. 

Some of the commonly reported performance issues are due to one or many  of the following reasons,

- Students are printing large data frames to a notebook directly or trying show a table that is too large in the notebook. The way to solve this issue is to ask students to slice the dataframe to a smaller sample that you want them to explore further. You can review your datasets and slice it as much as possible so that you are only sharing the data that is core to achieving the required learning outcomes for students. 
- Students are running a Python/R/Julia code with an infinite loop. You can inform students to check whether any one of their code is running an infinite loop and ask them to reach out to you/your team if they think they have problem with the code. You can also check with the infra team to identify the problematic user notebooks and can access them to check the exact issue.
- Students are joining tables that are large. Once again, try to break down the dataset to subset that is of interest to achieve the course objectives.
- Students are having multiple notebooks open at the same time across one or many browsers. If students report errors such as 503 error code, 401 etc.. ask them to check if they have notebooks open in multiple tabs. If it is the case, ask them to close the other tabs and just have a single active tab. As a best practice, please ask students to have a single active tab with notebook.
- You upgraded to the latest version of a package without testing it extensively (e.g.: Otter grader). As a rule of thumb, upgrade packages in staging  environment and test the notebooks extensively. Only when you feel comfortable with the updated environment, ask the infra team to upgrade to the latest package versionin the stable environment. If you are unsure of the URL for your staging environment, ask the infra team
- You are using databases like SQLite as part of your workflow without having a consultation about the best practices with the infrastructure team.
- You are trying to use GUI-based applications like pyqt5 and QGIS without consulting the infrastructure team