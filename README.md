# IBM_AI-in-CPIP
Materials and projects from an undergraduate research course on using unstructured data for AI applications to the Chemicals, Petroleum, and Industrial Products (CP&ampIP) industries. 

Interdisciplinary engineering group project under the guidance of and with lectures by various IBM executives. 
The folder contains the technical aspect of the project, which I was responsible for. In particular, I was assigned the role of IBM Watson Tech Lead. 
I have created and developed a polyethylene industry-specific type system in Watson Knowledge Studio for use by Watson Discovery, which was called on by Watson Assistant for help with answering long-tail questions. This involved compiling an industry specific ontology and creating dictionaries corresponding to different entity types based on that ontology for preannotation. It also involved creating a set of relevant entity types and relations between them for use in training (the annotation process), as well as compiling a set of ground truth documents that were descriptive of the type system used. Finally, it involved searching for, compiling, and splitting (into train and test) document sets relevant to the chemicals industry, as well as using them to train and test the machine learning model through annotation. I have also trained Watson Discovery for recognition of relevant documents and passages to retrieve and return to Watson Assistant, as well as designed and created the Watson Assistant dialog, and created the entire necessary entity and intent structure. 

Watson Discovery (enhanced by the WKS ML model) was then integrated with Watson Assistant and Telegram through Nodered for ease of accessiblity to the conversational solution. The following link gives access to the Watson solution:

https://web.telegram.org/#/im?p=@Watson_b_bot

Currently, the solution is capable of answering general short-tail questions about operation of a Polythylene plant, OSHA safety guidelines, process unit specifications, chemical properties and MSDS of chemicals used in production, etc. Some sample questions include:

-What are the unit operation specifications for an autoclave reactor?
-Can you give me the MSDS for High Density Polyethylene?
-What are the OSHA guidelines for eyewash stations?

If the solution cannot understand the question or cannot readily answer it, it calls on Watson Discovery to query and find high-confidence potential answers and delivers them to the user. An example of such a query would be:
-Variants of cross-linking

The project is still in progress, and is constantly being updated and improved. For the final version, check back after May 20th (Final presentation date)!

The structure of the subfolders is as follows:
WA -> Watson Assistant Workspace file
WDS -> Some sample documents uploaded to Discovery for querying
WKS -> Documents -> Documents used for development of the model, the type system as well as creation of preannotation dictionaries; Documents used as training and testing set for training and evaluation of the model
WKS -> Dictionaries -> Preannotation Dictionaries
WKS -> Type System -> Type system file
NodeRed -> NodeRed integration file
