# Domain Structure Creator

This Bash script facilitates the creation of a structured domain hierarchy with sub-domains and associated layers. Follow the steps below to use the script:

## Prerequisites
- Ensure that you have Bash installed on your system.
- For macOS insure you have a bash version 4.0 or above 

## Instructions

1. *Download the Script:*
   - Obtain the script ( data_domain_structure_creator.sh ) file on your machine.

2. *Make the Script Executable:*
   - Open a terminal and navigate to the directory containing the script.
   - Run the following command to make the script executable:
     ```bash
     chmod 777 data_domain_structure_creator.sh
     ```

3. *Run the Script:*
   - Execute the script using the following command:
     ```bash
     ./data_domain_structure_creator.sh
     ```

   - In case of macOS :
     ```bash 
     bash data_domain_structure_creator.sh
     ```
    
     
4. *Input Domain Information:*
   - Enter the main domain name when prompted.
   - Specify the number of sub-domains you want to create.

5. *Sub-Domain and Layer Configuration:*
   - For each sub-domain, provide a name.
   - For each sub-domain, choose layers to include by entering the corresponding numbers.
     - Available layers: "11_landing," "12_bf," "13_sq," "14_DQ," "15_DATAMART," "16_DQ_MART."
     - To finish layer selection, type 'exit.'

6. *View the Result:*
   - Once the script completes, it will display a success message along with the created domain name.

## Example Usage:
- Main domain: `consumers`
- Number of sub-domains: `2`
  - Sub-domain 1: `membership`
    - Layers: `11`, `12`, `14`
  - Sub-domain 2: `prospect`
    - Layers: `12`, `13`, `15`

- The resulting directory structure would be:
  ```bash
    consumers_domain
    ├── 11_domian
    │   ├── 12_bf
    │   │   └── schema.yml
    │   └── 14_DQ
    │       └── schema.yml
    └── prospect_domian
        ├── 12_bf
        │   └── schema.yml
        ├── 13_sq
        │   └── schema.yml
        └── 15_DATAMART
            └── schema.yml
  ```