# 4HYDRO's Open community Sharing Code
### Description
4DHydro is a project funded by ESA which aims to provide a study of selected geospatial and climate data to improve the understanding, 
observation and monitoring of the availability of water resources planet earth. 
This GitHub project has been created to collect the metadata of the EO, LSM or Insitu data involved in this study, 

## Function
- Centralizing the collection of metadata from all consortium partners
- Possibly open up the metadata contribution to other contributors at the end of the project.
- Verify the validity and consistency of metadata according to project specifications.
- Create a STAC catalog from this metadata, which will be automatically updated when new metadata is added.

![workflow_diagram.png](docs%2Fworkflow_diagram.png)

## How to contribute to Catalog

It's quite simple: you will have to fill in the metadata corresponding to your data in a set of CSV files
(the STAC catalog will be created automatically).
We strongly encourage you to read this note from WP3 [metadata.docx - UFZ Cloud](https://nc.ufz.de/s/QpKy8TrQp9ykkaN?path=/WP3&openfile=154855067&dir=undefined)
in order to fully understand the information that will be provided. 


![metadata_class_diagram.png](docs%2Fmetadata_class_diagram.png)

## Prerequisites

To be able to contribute to the catalogue, you need to have these tools installed:
- Have Git installed (https://git-scm.com/)
- Have a GitHub account in order to participate in the project (https://github.com/)
- Be registered on the project as a contributor. If not, please fill in your information here [ufz cloud ](https://nc.ufz.de/s/QpKy8TrQp9ykkaN?dir=undefined&path=%2FWP3&openfile=156241690) to be added.
- A CSV editor (https://www.editcsvonline.com) 

## How update/add metadata on STAC catalogue 

- Clone 4DHydro GitHub project on your local workspace 
```bash
git clone https://github.com/okoko-cs/4dhydro-open-science-catalog-metadata.git 
cd 4dhydro-open-science-catalog-metadata
```
After cloning the project locally, you should have these files 

![project_files.png](docs%2Fproject_files.png)

- Create your work space
```bash
git checkout –b <consortium>/metadata # example: git checkout -b csgroup/metadata
```
Nb: (replace <consortium> by name of the consortium ex: git checkout –b csgroup/metadata) 

If you have already created your workspace, and you wish to add new data to the CSV template, don't forget to update your workspace with the main branch of a project using the command:
```bash
git pull origin main # retrieves the latest updates from the main branch
git merge main # transfers updates to your branch
```
- Edit CSV metadata Templates

Go to your workspace 4dhydro-open-science-catalog-metadata/csv you will see these different files then edit them in the following order: 
    - EO Missions.csv 
    - Themes.csv 
    - Variables.csv
    - Products.csv
    - WP5_Tier2_Products.csv
    - Processes.csv
  
Open files with Excel or any software that supports csv to edit template and add yours metadata.
example Edit EO Missions.csv for adding new metadata relating to the missions from which the products are derived
I suggest this link for easy editing of CSV (https://www.editcsvonline.com/)

![csv_template_sample.png](docs%2Fcsv_template_sample.png)

After filling, save the file in csv format, and do the same for the other csv files.  
Make sure that the files are saved in CSV format with the "," character as the separator.

- Commit your progress

```bash
git add csv
git commit –m "<commit message>" # example: git commit -m "add new ground water product"
```
- Push your data on this remote repository

```bash
git  push origin <consortium>/metadata # example: git push origin csgroup/metadata
```
![push_commit_sample.png](docs%2Fpush_commit_sample.png)

when you submit your data to the git repository, a validation phase will be carried out to check that you have filled in the templates correctly. if this phase has been validated, you can continue to the next stage, otherwise an e-mail will be sent to you to alert you that the validation phase has failed.

![view_push_commit.png](docs%2Fview_push_commit.png)

- Create a pull request on GitHub repository 

Once your data has been submitted to the GitHub, a merge request will be made for your data to be published on the project's catalogue. To do this, go to the project's GitHub repository. 

https://github.com/okoko-cs/4dhydro-open-science-catalog-metadata -> pull requests -> new pull request 

![create_pr_1.png](docs%2Fcreate_pr_1.png)
![create_pr_2.png](docs%2Fcreate_pr_2.png)

for more: [create a pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)

## CATALOG VIEW 
when the merge request is created, an administrator will be responsible for confirming that the merge request has been considered and that the data has been published in the catalogue https://opensciencedata.4dhydro.eu 

 