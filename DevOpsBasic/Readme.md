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
### Agent
* It is a software that takes all the tasks in the pipeline and executes everything serially such as Test, Build, Publish, UAT, Switch.
* **Switch** is the action of asking `Approval` that is permissions.