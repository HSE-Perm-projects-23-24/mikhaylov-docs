# TOGAF in the Creation of Educational IT-Infrastructure

## Abstract
Abstract — This article is devoted to the study and application of the TOGAF methodology, the architecture development method (ADM). Based on this methodology, a model of the platform architecture was implemented for practical training in the framework of the discipline "Algorithms and Data Structures" in the ArchiMate modeling language. The developed platform has provided the ability to perform tasks related to writing program code and automatic verification of solutions. The platform implements tasks related to the support and development of the real web application "Online Algorithm Calculator". 

Keywords — TOGAF, ArchiMate, ADM, IT-infrastructure.

## I INTRODUCTION
In today's rapidly evolving technological world, the education of IT professionals must encompass not only fundamental knowledge, which remains relevant and important, but also the development of practical skills. The application of theoretical knowledge in practice becomes a key factor for success, contributing to the solution of professional tasks. Therefore, educational programs should include practical exercises and projects that provide students with the opportunity to apply their acquired knowledge in real conditions and contribute to the development of professional and flexible skills necessary for working in the IT field.

Modern software systems and applications are characterized by a high degree of complexity, including the use of artificial intelligence, distributed systems, and microservices, which complicates their reproduction on students' personal computers. In this context, the presence of a suitable IT infrastructure that students can use for practical assignments becomes critically important. Such infrastructure will allow students to apply and deepen their theoretical knowledge in a practical context, as well as develop professional skills in an environment that is as close as possible to the real software development environment.

The development of information technology and the processes of digital transformation in Russia have led to a significant increase in demand for IT specialists. However, the education system does not always manage to adequately respond to these changes, leading to a deficit of qualified IT specialists. The presence of a deficit of IT specialists is noted both in press publications, for example, in the article of the Russian newspaper "V Rossii ustanovilsya deficit ajtishnikov. Kak ego vospolnit'?" [1], and in scientific publications, for example in the work "Deficit it-kadrov v rossii na sovremennom etape: prichiny i puti preodoleniya" [2]. With the growth of demand for specialists, the number of students studying in higher education programs in the field of IT and mathematical specialties is also growing. According to the federal project "Kadry dlya cifrovoj ekonomiki" the number of students admitted to these programs in 2024 should reach 120,000 [3]. With the increase in the number of students, the load on teachers increases, including the preparation and checking of assignments for writing program code. An important aspect of using IT infrastructure for practical assignments is the possibility of automating the checking of assignments related to writing program code. Modern technologies and development tools allow automating the code checking process, which reduces the load on teachers and allows them to focus on more important aspects of education, such as feedback and individual work with students. At the same time, this contributes to the formation of students' skills in working with modern development tools and practices, such as continuous integration and continuous testing, which are key in the modern IT industry.

## II MOTIVATION

The importance of a digital infrastructure is underscored in higher education standards. For instance, the Federal State Educational Standards "Programmnaya inzheneriya" [4] and "Prikladnaya informatika" [5] specify the need for a software suite in the requirements for the material and technical support of the program. In the context of IT specialist training, this requirement should include not only educational and scientific programs, but also professional tools for software development. Moreover, the standard emphasizes the importance of providing students with access to modern professional databases and information reference systems, which, in the context of IT specialist training, may include access to scientific and technical databases, code libraries, software repositories, and other resources that may be useful in the learning process.

In addition, educational standards contain requirements for the use of an electronic information and educational environment for access to educational materials, the formation of a student's electronic portfolio, and the recording of the educational process. Most publications on the topic of the digital infrastructure of an educational organization are devoted to the information and educational environment. For example, in the work of Davidenko, L.M. "Informacionnaya arhitektura elektronnogo uchebnogo kursa" [6], the experience of using the LMS Moodle platform in educational institutions of Kazakhstan is considered. In the work of Zhukovsky I.E. "Cifrovye platformy - vazhnyj aspekt cifrovizacii vysshego obrazovaniya" [7], various platforms used for organizing the educational process are considered, including LMS Moodle, Linkedin Learning, platforms for developing educational courses, online learning and testing, for example, Mooc, Udacity. In the work of Shevkun A.V. "Formirovanie elektronno-obrazovatel'noj sredy v usloviyah cifrovizacii professional'nogo obrazovaniya" [8], in addition to LMS Moodle, video conferencing services, cloud storage for collaborative work on educational materials, Trello, Padlet and Miro services are considered.

Against the background of the mentioned works, the articles of Samokhvalov A.V. "Interaktivnye trenazhery i ih primenenie v processe podgotovki IT-specialistov v sisteme distancionnogo obucheniya Moodle" [9] and Protasova S.I. “Opyt ispol'zovaniya sistemy upravleniya obucheniem (LMS) i avtomatizirovannyh sistem testirovaniya v prepodavanii disciplin s modul'no-rejtingovoj strukturoj kursa” [10] contains a description of the experience of integrating LMS Moodle with automated systems for checking programming assignments. In addition, many works of modern researchers [11, 12] consider the use of contest systems, in particular the Yandex.Contest platform, designed for holding exams, olympiads, individual and team programming competitions, which allows automating the checking of program code.

Contest systems are useful and effective tools for training IT specialists. They provide students with the opportunity to practice programming skills, solve various problems and participate in competitions. However, despite their effectiveness in teaching the basics of programming and algorithmic thinking, contest systems have some limitations. They do not provide students with the context that is present when solving real tasks in a professional environment. In addition, they do not teach students to work within the processes that are usually used in IT companies. Therefore, despite their value, contest systems should be used in combination with other learning methods to ensure a comprehensive training of future IT specialists.

Based on the analysis of existing research, it can be concluded that a large number of works are devoted to the electronic information and educational environment, automatic programming assignment checking systems or individual student software development projects. These works often focus on specific methodologies, technologies and tools. However, the issue of analyzing and modeling the IT infrastructure associated with software development for the training of IT specialists requires further research. Studying this issue is important for providing quality education that will prepare specialists capable of filling the workforce gap in the dynamically evolving IT sector.

## III RELATED WORKS

The scientific literature presents numerous works dedicated to the description and use of the TOGAF methodology, the Architecture Development Method (ADM), and the ArchiMate modeling language. In particular, the works of A.D. Borremans [13] and A.T. Synbulatova [14] provide a comparison of methodologies such as TOGAF (The Open Group Architecture Framework), Zachman, Gartner, and others. The experience of using the TOGAF methodology for modeling the architecture of an educational organization is described in the works of K.G. Skripkin [15] and A.Yu. Sapozhnikova [16]. V.A. Knyshov [17] considers the ArchiMate modeling language, developed by The Open Group and suitable for use within the TOGAF methodology. As an example of a work that thoroughly describes the practical application of the ADM method, one can note the article "Adaptaciya adm metoda standarta togaf k razrabotke i vnedreniyu arhitekturnyh reshenij v sfere setevogo  FMCG-ritejla" [18] by authors Voronova O.V. and Ilyin I.V. Some works describe the application of TOGAF in the context of educational organizations, including works [16] and [19] and others by a team of authors Kuznetsov A.A., Sapozhnikova A.Yu., Kulikova G.G., considering the processes of digital transformation of universities and enterprises using the TOGAF methodology for the transition to Industry 4.0. The main focus in the team's works is on designing a knowledge management system for joint use by universities and industrial enterprises. 

The work "Arhitekturnye podhody v upravlenii informatizaciej obrazovatel'nogo uchrezhdeniya" [20], authored by N.V. Bradula, is most closely related to the topic of this research. It considers the problem of building the IT infrastructure of an educational institution and choosing methods to align the infrastructure with the real needs of the organization. The work carries out a comparative analysis of architectural approaches to IT management in an educational institution, including the Zachman model, EAP, TOGAF, FEAF, GERAM, and GEAF. The author demonstrates the appropriateness of using the TOGAF architecture for higher education institutions. All these studies confirm the significance of TOGAF and ADM in the context of developing and managing enterprise architecture. They also highlight the flexibility and adaptability of these tools, indicating the possibility of their application in the educational sphere for modeling and developing IT infrastructure intended for practical sessions in the process of training professionals of IT specialties.

## IV SETTING THE TASK

The aim of this research is to apply an architectural development method for modeling a platform that provides IT infrastructure for practical sessions in the training of IT specialists, exemplified by seminar sessions on the discipline "Algorithms and Data Structures".

A significant aspect of using the platform is the ability to automate the checking of tasks related to writing program code, including running a set of tests to check the functionality of the code, checking the code style to comply with standards and coding guidelines, and static code analysis to identify potential errors and vulnerabilities.

The implementation of the automatic task checking process reduces the workload on teachers and contributes to the formation of students' skills in working with modern practices and development tools.

The object of the study is the infrastructure for training IT specialists. The subject of this research is the use of an architectural method for modeling a platform designed for practical sessions in the process of training IT specialists.

To achieve the set goal, the following tasks were formulated:
1. To explore the approaches, technologies, and tools that can be used for the development and management of IT infrastructure in the educational process.
2. Using the architectural development method, to develop a platform for practical sessions that implements IT infrastructure and provides for the execution of coding tasks and automatic solution checking.

## V GENERAL DESIGN
In the context of this research, the focus is on modeling and developing IT infrastructure for the practical training of IT specialists, using the discipline "Algorithms and Data Structures" as an example. This limitation is introduced for several reasons:
1. "Algorithms and Data Structures" is one of the key disciplines in the training of IT specialists, and its content and practical skills requirements are well-known and standardized.
2. Limiting the scope to one discipline allows for a concentrated focus on the details and peculiarities of modeling and developing IT infrastructure, without being distracted by the multitude of different requirements and contexts that may arise when considering a full training program.
3. The experience gained and the infrastructure developed can be used in the future as a basis for scaling to an educational program. Thus, although this research is limited to one discipline, it provides a foundation for broader application and further development.

The methodological basis of the research is the architectural approach used in informatization, which involves a systematic and holistic consideration of the object under study, taking into account all its components and the relationships between them.

The research methods used include:
- System analysis and synthesis for considering the object under study in a complex, identifying the main components and relationships, and forming a general understanding of the research object.
- Analysis of theoretical sources, which involves studying and analyzing scientific literature on the research topic to identify the main approaches and methods used in this field, as well as identifying gaps in existing research.
- Comparison and generalization for comparing different approaches, methods, research results, as well as for generalizing the data obtained and forming general conclusions.
- Analysis of documents related to the research topic, including regulatory documents, standards, conference materials, etc.
- SWOT analysis to assess the strengths and weaknesses, opportunities and threats associated with the object or situation under study. This method allows for a comprehensive understanding of the situation, identifying internal resources and external factors that may affect the achievement of goals.

The theoretical base of the research includes articles in scientific journals, conference materials, regulatory documents, and standards.

## VI IMPLEMENTATION

The modeling and development of the platform for practical sessions were carried out in accordance with the architecture development method of the TOGAF framework. As of now, the latest relevant version of TOGAF is version 10 [21], published in 2022. ArchiMate language was used for modeling, which, like the TOGAF framework, is supported by The Open Group, allowing them to be used together for architecture development. The current relevant version is ArchiMate 3.2 [22], released by The Open Group in 2023.

Figure 1 demonstrates the capabilities of ArchiMate in relation to the stages of the TOGAF architecture development method. ArchiMate offers a multi-level representation of architecture, which allows modeling the domains defined in TOGAF.

![Implementation of the architecture development method using the ArchiMate modeling language](https://cdn-images.visual-paradigm.com/guide/togaf/togaf-adm-tutorial/02-togaf-adm.png)

Fig. 1. Implementation of the architecture development method using the ArchiMate modeling language [23]

The developing ArchiMate architecture model is hosted on GitHub and is publicly accessible [24]. It is provided in HTML format to enable viewing of the created views using a web browser.

The process of modeling and developing the infrastructure according to the architecture development method was implemented in stages:

### A. Preliminary Phase
At this stage, key technologies and tools that can be used for the development and management of IT infrastructure in the educational process were identified:
- Cloud technologies. The use of cloud services such as AWS, Yandex Cloud, and VK Cloud ensures the availability and scalability of educational resources and reduces the cost of their maintenance.
- Containerization and orchestration. The application of Docker and Kubernetes standardizes the process of developing and deploying applications, simplifying their use in the educational process.
- Version control systems. The use of Git, GitHub, and GitLab provides effective code version management and collaborative work on projects by students.
- Development environments. The application of modern IDEs, such as Visual Studio Code, PyCharm, IntelliJ IDEA, facilitates the process of writing and debugging code.
- Project management systems. The use of Jira, Trello, and Asana aids in project organization and management, contributing to the development of project management skills in students.
- Continuous integration and delivery systems (CI/CD). The application of Jenkins, GitHub Actions, GitLab CI, and other tools automates the process of testing and deploying code, accelerating the development process and improving the quality of the final product.
- Virtualization systems. The use of VMware, VirtualBox, and others allows the creation of virtual machines for studying and testing various systems and technologies.

The main approach to infrastructure development is Infrastructure as Code (IaC). This approach allows the management and configuration of IT infrastructure using code, ensuring repeatability, scalability, and automation of processes, which is especially useful in the educational process, where it is necessary to quickly and efficiently deploy and configure resources for a large number of students.

In addition, the DevOps methodology, which combines development and operation processes, can be used to implement the infrastructure. This can accelerate the development process and improve the quality of the final product. In the context of education, this can help students better understand the full cycle of software development, including writing code, testing, deployment, and support. Moreover, DevOps tools and practices can be used to automate processes related to practical assignments, including automatic testing processes, application build and deployment processes.

### B. Phase A: Architecture Vision

At this stage, using the motivation extension of the ArchiMate language, modeling of stakeholders, driving forces of changes, business goals, principles, and requirements was  carried out. The results of the analysis of driving forces are presented in the form of assessments. The assessments are grouped into strengths and weaknesses, opportunities and threats, after which a SWOT analysis was conducted, business goals and expected results were formulated.

The stakeholders identified include the teacher, the student, the employer, and the head of the department. The primary driver for change is the quality of student preparation, with the goal of the changes being to enhance this quality.

### C. Phase B: Business Architecture

At this stage, the internal structure of the organization was modeled, and the competencies, authority, and responsibility of employees were identified. Analysis and modeling of existing business processes were carried out with decomposition from the level of the educational process as a whole to the level of performing tasks in seminar classes on the considered discipline.

As a result, model views have been developed from the Organization Viewpoint and the Business Process Cooperation Viewpoint.

### D. Phase C: System Architecture

At this stage, business process modeling was carried out, taking into account planned changes related to the implementation of the platform for practical classes, as well as modeling of platform components with an illustration of how the components interact with each other and support business processes.

For modeling process support, a view from the Application Usage Viewpoint has been developed. The "Online Algorithm Calculator" web application has been chosen for task execution in an environment closely resembling real software development. This application was created by students of HSE University-Perm as an open project for software product development, which can be used to solve educational tasks in software engineering [25]. The architecture of the application allows for easy expansion of its functionality by adding new algorithms, making it possible to use it for practical assignments in the "Algorithms and Data Structures" course.

### E. Phase D: Technology Architecture

At this stage, the platform infrastructure was designed, and the support of platform components by software and hardware technologies was modeled. Requirements for hardware, network infrastructure, software, and other resources have been defined.

As a result, a model view from the Technology Usage Viewpoint has been developed. The infrastructure includes an organization created on the GitHub service, with a project for task management and a set of repositories for tasks, methodological materials, and the source code of the web application. The GitHub Actions continuous integration service is used for automatic task checking, testing, building, and deploying the web application. For static code analysis, integration of GitHub and Sonar Cloud services is used. A cloud server is used for hosting the web application.

For the designed platform, all previously identified technologies are used:
- Project management systems - GitHub Issues is used to manage tasks for the discipline. The course is represented as a kanban board, tasks are created as task cards on the project board.
- Version control systems - the source code of the web application, tasks, and methodological materials of the course are stored in Git version control system repositories and are placed for collaborative work on the GitHub service.
- Development environments - work with the source code and task materials is carried out by students and teachers using the integrated development environment PyCharm.
- Cloud technologies - repositories with course materials are located in the GitHub cloud service. In addition, the "Online Algorithm Calculator" web application is deployed in the cloud infrastructure.
- Containerization and orchestration - the web application is deployed in a docker container.
- Continuous integration and delivery systems - with the help of the GitHub Actions service, automatic checking of tasks related to writing program code is organized, and processes of automatic testing, assembly, and deployment of the web application are set up.
- Virtualization systems - automatic CI/CD processes are performed on virtual machines of the GitHub Actions service.

### F. Phase E: Opportunities and Solutions

At this stage, opportunities for platform implementation were identified, and a corresponding project was formed.

As a result, a model view from the Value Stream Viewpoint has been developed, which represents a sequence of actions that create an overall result for a stakeholder. Each stage creates additional value and is supported by corresponding capabilities. Project hosting and system administration capabilities are required to create an organization on the GitHub service, set up the project, and repositories. Infrastructure capabilities, as well as web development and DevOps capabilities, are necessary for the integration of the web application and the setup of automatic task checking. At the stage of integrating the platform into the educational process, support capabilities are important, including training and user support.

### G. Phase F: Migration Planning

At this stage, architecture implementation plans were developed, resources needed for implementation and associated risks were identified. 

A model view from the Resource Map Viewpoint has been developed, illustrating which resources provide capabilities for platform implementation. To illustrate the connection of project stages to those parts of the architecture they implement, and to analyze consistency between project dependencies, a view from the Implementation and Migration Viewpoint has been developed.

The following risks associated with the use of IT infrastructure in the educational process were identified:
- Data security, including the risk of unauthorized access, data leakage or loss, including personal data of students and teachers, as well as intellectual property.
- Service unavailability - failures in the operation of the IT infrastructure can seriously disrupt the educational process. This can be caused by technical problems, DDOS-attacks, or insufficient system scalability.
- Supplier dependence - the risk of dependence on suppliers is a significant factor, especially when using cloud services or other external resources.
- Insufficient staff skills - a lack of qualified IT staff or insufficient skills of teachers and students in the field of IT have been noted as significant obstacles to the effective use of IT infrastructure.
- Risks associated with changes - the introduction of new elements of the IT infrastructure or changes to existing ones can lead to compatibility issues.
- Legal risks, including the importance of compliance with legislation in the field of data protection, copyright, and other areas.

### H. Phase G: Implementation Governance 

At this stage, monitoring and control over the implementation of the platform development and implementation project was carried out.

During the infrastructure setup on the GitHub service, organizations were created for two groups of students taking the course. Repositories for manual tasks and programming tasks were created for the organizations, as well as repositories for auxiliary course materials, such as instructions for working on the platform and setting up the necessary software. A project "Algorithms and Data Structures 23/24" was created in the organization for course task management, and a kanban board was set up to visualize project task cards.

For the integration of the web application, forks of repositories with the source code of the server and client parts of the Online Calculator web application were added into the organization. The process of automatic assembly and updating of deployed web application stands was implemented on a rented cloud server according to the CI/CD scenario using the GitHub Actions service.

During the work on setting up automatic task checking, the functionality of performing auto-tests, code style checking, and static code analysis using the SonarCloud service was implemented.

At the stage of integrating the platform into the educational process, students were added to the organization's members for conducting the course and distributed into teams, necessary materials and introductory tasks for learning to work with the platform were added to the project.

### I. Phase H: Architecture Change Management

Based on the results of the platform development and implementation, an analysis was conducted and directions for possible development were identified, including:
- Based on the knowledge gained, training materials can be developed for fellow teachers on using IT infrastructure for practical sessions.
- Seminars and training sessions can be organized for teachers and students to pass on the acquired knowledge and skills.
- The developed approach to modeling and developing infrastructure can be adapted for developing infrastructure that supports practical sessions with IT students within the educational program.

## CONCLUSION AND FUTURE WORK

The experience gained during the research showed that effective use of IT infrastructure for practical classes requires an analysis of requirements, based on the curricula of educational programs, taking into account specific tasks that students will have to solve during their studies. In addition, it is necessary to model the proposed infrastructure, including the creation of architectural models describing the structure and interaction of its components, as well as modeling the processes of using the infrastructure by students and teachers.

The developed architectural model and its representations from different perspectives will help convey to decision-makers the motivation for using such infrastructure, considering that its creation and maintenance require significant costs. Illustrating how the infrastructure contributes to the development and application of students' knowledge and skills in conditions as close as possible to the real software development environment can justify these costs.

The research confirmed the possibility of using the TOGAF framework and the architecture development method for modeling and developing the infrastructure for training IT specialists. The platform developed as part of the research for practical sessions demonstrates the applicability of key IT infrastructure creation technologies in an educational context.

The developed platform for practical sessions includes a web application "Online Algorithm Calculator", deployed on a cloud server, an organization created on the GitHub service, with a set of repositories, including the source code of the web application, tasks, and methodological materials of the course, a Kanban board with course tasks, as well as the workplaces of teachers and students with the PyCharm IDE integrated with GitHub. Using the GitHub Actions service, automatic task checking, testing, building, and deployment of the web application have been set up. Students have been given the opportunity to practically apply theoretical knowledge by developing a real web application "Online Algorithm Calculator". The automation of testing, building, and deploying the application has allowed students to focus on studying the material and developing software, rather than routine operations. As a result, students have not only mastered the theoretical material but also acquired practical skills in working with modern software development tools, which is an important component of IT specialist training.

During the work, risks associated with the use of IT infrastructure in the educational process were identified and analyzed, including risks of data leakage, infrastructure component failures, dependence on software and equipment suppliers, insufficient staff qualifications, risks of compatibility violations of infrastructure components, and legal risks in the field of data protection and copyright.

The results of the current work should be considered as the first step in researching the possibilities of an architectural approach to creating and managing IT infrastructure for the educational process. Further research in this area can refine and supplement the conclusions obtained, including a wider range of disciplines and educational programs for which IT infrastructure may be required. Overall, the results confirm the significance and relevance of the research topic and indicate opportunities for further development in this area.

## REFERENCES

1. Zhandarova, I. V Rossii ustanovilsya deficit ajtishnikov. Kak ego vospolnit'? / I. Zhandarova, O. Kapranov. - Tekst : elektronnyj // Rossijskaya gazeta : sajt. - 2023. - 17 avg. - URL: https://рг.ру/2023/08/17/vziat-v-razrabotku.html.
2. Vasil'eva E.V., Kamanina A.N. DEFICIT IT-KADROV V ROSSII NA SOVREMENNOM ETAPE: PRIChINY I PUTI PREODOLENIYA // Diskussiya. 2023. №2 (117). URL: https://cyberleninka.ru/article/n/defitsit-it-kadrov-v-rossii-na-sovremennom-etape-prichiny-i-puti-preodoleniya.
3. Pasport federal'nogo proekta «Kadry dlya cifrovoj ekonomiki» nacional'noj programmy «Cifrovaya ekonomika Rossijskoj Federacii».URL: https://www.consultant.ru/document/cons_doc_LAW_328933.
4. Federal'nyj gosudarstvennyj obrazovatel'nyj standart vysshego obrazovaniya - bakalavriat po napravleniyu podgotovki 09.03.04 Programmnaya inzheneriya: utv. Prikazom Ministerstva obrazovaniya i nauki RF ot 19 sentyabrya 2017 g. № 920.
5. Federal'nyj gosudarstvennyj obrazovatel'nyj standart vysshego obrazovaniya - bakalavriat po napravleniyu podgotovki 09.03.03 Prikladnaya informatika: utv. Prikazom Ministerstva obrazovaniya i nauki RF ot 19 sentyabrya 2017 g. № 922.
6. Davidenko, L. M. Informacionnaya arhitektura elektronnogo uchebnogo kursa / L. M. Davidenko, P. V. Davidenko // Informacionnye tehnologii v modelirovanii i upravlenii: podhody, metody, resheniya : В Vserossijskaya nauchnaya konferenciya s mezhdunarodnym uchastiem: sbornik materialov, Tol'yatti, 20–22 aprelya 2022 goda / Otv. za vypusk E.V. Panyukova. – Tol'yatti: Tol'yattinskij gosudarstvennyj universitet, 2022. – S. 320-327.
7. Zhukovskaya, I. E. Cifrovye platformy - vazhnyj aspekt cifrovizacii vysshego obrazovaniya / I. E. Zhukovskaya // Otkrytoe obrazovanie. – 2022. – Т. 26, № 4. – С. 30-40. – DOI 10.21686/1818-4243-2022-4-31-40.
8. Shevkun, A. V. Formirovanie elektronno-obrazovatel'noj sredy v usloviyah cifrovizacii professional'nogo obrazovaniya / A. V. SHevkun, A. M. Pirozhnikova // Uchenye zapiski Zabajkal'skogo gosudarstvennogo universiteta. – 2023. – T. 18, № 1. – S. 100-106. – DOI 10.21209/2658-7114-2023-18-1-100-106. – EDN RWRWVA.
9. Samohvalov, A. V. Interaktivnye trenazhery i ih primenenie v processe podgotovki IT-specialistov v sisteme distancionnogo obucheniya Moodle / A. V. Samohvalov, D. S. Solov'ev, A. A. Skvorcov // Vestnik Tambovskogo universiteta. Seriya: Gumanitarnye nauki. – 2023. – Т. 28, № 5. – S. 1063-1076. – DOI 10.20310/1810-0201-2023-28-5-1063-1076. – EDN AFFGLK.
10. Protasov, S. I. Opyt ispol'zovaniya sistemy upravleniya obucheniem (LMS) i avtomatizirovannyh sistem testirovaniya v prepodavanii disciplin s modul'no-rejtingovoj strukturoj kursa / S. I. Protasov // Obrazovatel'nye tehnologii i obschestvo. – 2017. – Т. 20, № 1. – S. 410-416. – EDN XQZMVH.
11. Kapitanov, A. I. Primenenie onlajn-platformy YAndeks.Kontest dlya provedeniya kontrol'nyh meropriyatij po programmirovaniyu na yazyke Python / A. I. Kapitanov, I. I. Kapitanova // Molodoj uchenyj goda 2023 : sbornik statej V Mezhdunarodnogo nauchno-issledovatel'skogo konkursa, Penza, 05 marta 2023 goda. – Penza: Nauka i Prosveschenie (IP Gulyaev G.YU.), 2023. – S. 11-13. – EDN FBBEBE.
12. Larina, YU. A. Provedenie prakticheskih zanyatij po programmirovaniyu s ispol'zovaniem onlajn-platformy YAndeks.Kontest / YU. A. Larina, O. B. Lavrovskaya // Aktual'nye problemy sovershenstvovaniya vysshego obrazovaniya : Tezisy dokladov XВИ Vserossijskoj nauchno-metodicheskoj konferencii, YAroslavl', 28–29 marta 2024 goda. – YAroslavl': Obschestvo s ogranichennoj otvetstvennost'yu “Filigran”, 2024. – S. 341-343. – EDN ACPWMG.
13. Borremans, A. D. Metodologii postroeniya biznes-arhitektury predpriyatiya / A. D. Borremans, A. A. Mulishova // Sovremennye voprosy ustojchivogo razvitiya obschestva v epohu transformacionnyh processov : Sbornik materialov В Mezhdunarodnoj nauchno-prakticheskoj konferencii, Moskva, 31 yanvarya 2023 goda. – Moskva: Obschestvo s ogranichennoj otvetstvennost'yu "Izdatel'stvo ALEF", 2023. – S. 171-176.
14. Synbulatova, A. T. Analiz i sravnenie metodologij po modelirovaniyu arhitektury predpriyatiya / A. T. Synbulatova // Beneficiar. – 2021. – № 90. – S. 28-32.
15. Skripkin K.G. Vliyanie vneshnej sredy na organizacionnyj dizajn obrazovatel'nogo uchrezhdeniya: instrumenty analiza // Sovremennye informacionnye tehnologii i IT-obrazovanie. 2016. №3-2.URL: https://cyberleninka.ru/article/n/vliyanie-vneshney-sredy-na-organizatsionnyy-dizayn-obrazovatelnogo-uchrezhdeniya-instrumenty-analiza
16. Sapozhnikov A. YU. Upravlenie znaniyami na primere mashinostroitel'nogo predpriyatiya i VUZa / A. YU. Sapozhnikov, G. G. Kulikov, A. A. Kuznecov, M. V. YUrlov // Vestnik YUzhno-Ural'skogo gosudarstvennogo universiteta. Seriya: Komp'yuternye tehnologii, upravlenie, radioelektronika. – 2022. – T. 22, № 2. – S. 148-157. – DOI 10.14529/ctcr220214.
17. Knyshov, V. A. Арчимате kak sredstvo opisaniya arhitektury predpriyatiya / V. A. Knyshov, A. V. Svischev // Moya professional'naya kar'era. – 2023. – T. 3, № 48. – S. 24-29.
18. Voronova O.V., Il'in I.V. ADAPTACIYA ADM METODA STANDARTA TOGAF K RAZRABOTKE I VNEDRENIYU ARHITEKTURNYH REShENIJ V SFERE SETEVOGO  FMCG-RITEJLA // Ekonomika i upravlenie. 2019. №7 (165). URL: https://cyberleninka.ru/article/n/adaptatsiya-adm-metoda-standarta-togaf-k-razrabotke-i-vnedreniyu-arhitekturnyh-resheniy-v-sfere-setevogo-fmcg-riteyla 
19. Kuznecov Aleksandr Andreevich, Sapozhnikov Aleksej YUr'evich, Kulikov Gennadij Grigor'evich ARHITEKTURA INFORMACIONNOJ PODSISTEMY ORGANIZACII METAMODELI ZNANIJ V PREDMETNO-ORIENTIROVANNOJ PROEKTNOJ OBLASTI (NA PRIMERE OBRAZOVATEL'NO-PROIZVODSTVENNOJ SREDY) // Vestnik UGATU = Vestnik UGATU. 2022. №4 (98). URL: https://cyberleninka.ru/article/n/arhitektura-informatsionnoy-podsistemy-organizatsii-metamodeli-znaniy-v-predmetno-orientirovannoy-proektnoy-oblasti-na-primere
20. Bradul, N. V. Arhitekturnye podhody v upravlenii informatizaciej obrazovatel'nogo uchrezhdeniya / N. V. Bradul // Menedzher. – 2019. – T. 1, № 1(87). – S. 114-120.
21. Chto novogo v TOGAF 10? [Elektronnyj resurs] // onlajn-zhurnal “Direktor informacionnoj sluzhby - Vestnik cifrovoj transformacii”, izdatel'stvo "Otkrytye sistemy"  URL: https://cio.osp.ru/articles/010722-Chto-novogo-v-TOGAF-10 
22. ArchiMate® 3.2 Specification // Oficial'nyj sajt Specifikaciya Archimate ot konsorciuma The Open Group. URL: https://pubs.opengroup.org/architecture/archimate3-doc/
23. TOGAF ADM Tutorial // Oficial'nyj sajt Visual Paradigm. URL: https://www.visual-paradigm.com/guide/togaf/togaf-adm-tutorial/
24. ArchiMate-model of education IT-infrastructure // GitHub Pages free hosting. URL: https://edu-it-infrastructure.github.io/archi/?view=id-7e9c0ae71df44933945985915082f25d
25. Mihajlov, A.V. Otkrytyj proekt dlya resheniya uchebnyh zadach programmnoj inzhenerii / Mihajlov A. V. // Sbornik materialov II studencheskoj nauchno-prakticheskoj konferencii im. L.L. Lyubimova, Redakcionno-izdatel'skij otdel NIU VSHE – Perm', 2024. – S. 37-43. URL: https://perm.hse.ru/editorial_publishing/Lyubimov_Conference2
