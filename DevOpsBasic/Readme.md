# DevOps
* It is a **ProManTo** word that is combination of Development and Operational
* `PETULA`
* Development 
    1. Plan 
    2. Execution 
    3. Test
* Operational 
    1. UAT (User Acceptance Testing) -> it is a temporary server where customent can execute there and verify everything
    2. Live -> after successful UAT and deploy it into Live server
    3. Assistance
* Why we go for devOps is, once development is complete they given the product to operational team then during their work may be **configuration file** not supporting the production environment or some **dll** files won't support, in these cases operational team blame development team and development blame that's their mistake (operational team).
* DevOps is a **`philosophy`** where both development team and operational team work together instead of blaming each other to deliver smooth product to the customer.
* Sometimes testing is tested by dev team and in some other cases it was done by QA team.
* After development team, we need to give the project to operational team in between we need to **build** the code by using **Pipelines**.
* Once the code is going into the pipeline, packages are install, and run the code, then it will some outputs in the form of **dll**, **exe** or some other form.
* These Pipeline outputs are called as **Artifacts**.
* These artifacts are given as input to the **UAT**.
* After support engineers assist the product then give back the **feedback** to the board again (Planning).
* Pipeline consists of Test, Build, Publish, UAT and switch.
---------------------------------------------------------
### Agent
* It is a Machine which has CPU, RAM and agent software that takes all the tasks in the pipeline and executes everything serially such as Test, Build, Publish, UAT, Switch.
* **Switch** is the action of asking `Approval` that is permissions.
* There are three types of agents 
    1. Hosted agents which was given by azure
    2. Self hosted agents -> free and we can run all our pipeline in this pool.
    3. Azure virtual agents
* Create our own `self hosted` agent in the agent pool.
* Then go inside and click new agent then we need to download the agent and extract that in our local system.
* We need to do some configuration as to connect the `local server` with the `remote pipeline` which is in azure.
* Execute the `.\config.cmd` command.
* For that first need to copy paste our `Organization name` from the azure.
* For authentication we need to create **Personal Access Token (PAT)** from our organization and paste it here in the local system.
* For creation of PAT token, just give `Agent pool` scope to **Read and write** that's it.
* Then it will ask for create **_work** folder to store all the works.
* Then execute the agent by `.\run.cmd` command.

----------------------------------------------------------------------
## YAML
* YAML is a data serialization format to store Configuration information.
* That is how to install packages, how to build and publish so all configuration information were stored in YAML.
* It is a **Name value based** and s**pace inteded based** and main purpose is efficient for **human readable**.