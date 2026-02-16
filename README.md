# What is Spec-Driven Development?

Spec-Driven Development **flips the script** on traditional software development. For decades, code has been king — specifications were just scaffolding we built and discarded once the "real work" of coding began. Spec-Driven Development changes this: **specifications become executable**, directly generating working implementations rather than just guiding them.

Let's start with the Lab!!!

### Step 1: Astral’s uv installer script - install uv (not required if you already have it installed) 

Make sure you have the right path where you want to create your project later (typically: C:\Users\FirstName_LastName\source\Dev\Projects\...)

Copy the following prompt to the github copilot chat (allow proposed steps and actions by Github Copilot):

```bash
irm https://astral.sh/uv/install.ps1 | iex
```


### Step 2: Install pre-requisites Specify CLI

Choose your preferred installation: 

#### Install git (if not already installed)

Please visit https://git-scm.com/install/windows and install accordingly


#### Install Specify CLI

Run directly without installing. Copy the prompt bellow to github copilot:

```bash
uvx --from git+https://github.com/github/spec-kit.git specify init <PROJECT_NAME>
```

**Note:**

- If you need more information how spec kit is built and how it works please use following link: https://github.com/github/spec-kit

### Step 3: You will be asked to provide a project name

```bash
HxG_Demo_SchedulingApp
```


### Step 4: Open "focus terminal" in the Github Copilot chat. 

You will find it directly in the chat where you executed the prompt in step 2, after the sub step called "planned project naming as "HxG_Demo_SchedulingApp". Choose your AI assistant using your keyboard to navigate to --> copilot (Github Copilot) and press enter


### Step 5: Remain in the focus terminal 

You now get asked to choose script type. Navigate with your keyboard to --> ps (pwerShell) and press enter


### Step 6: Now go to file in VS Code 

open folder e.g. "C:\Users\FirstName_LastName\source\Dev\Projects\...\HxG_Demo_SchedulingApp" to set the right path


### Step 7: Custom Agents

In this step we create custom agents.

#### Create new .md file in the .github\agents folder

1.a) Create a new file with the name
```bash
HxG_ideation_demoschedulingapp.agent.md
```
1.b) Copy the code from https://github.com/amrikhasler/Hexagon-TechDays26-Github-Copilot-Lab-Microsoft/blob/main/ideation_demoschedulingapp.agent.md?plain=1 to the newly created HxG_ideation_demoschedulingapp.agent.md

1.c) Alternative (not recommended due to longer reasoning time): If you have access to a researcher agent e.g. M365 Copilot Reasercher run the following prompt and copy the outcome to HxG_ideation_demoschedulingapp.agent.md:
```bash
Role: You are a product + technical researcher tasked with defining an MVP design and architecture for a lightweight “work assignment & scheduling” application.
Goal: Produce a practical blueprint for a new app that lets a user schedule/dispatch work to other users. The app must be super simple, it can be based on blazor. For demo purposes it should run locally and should leverage local memory or storage if needed: scheduling “requirements,” assigning the “best resource” based on availability/skills, and a visual “schedule board” experience.
```

2.a) Create a new file with the name
```bash
HxG_PrincipalReviewer.agent.md
```
2.b) Copy the code from https://github.com/amrikhasler/Hexagon-TechDays26-Github-Copilot-Lab-Microsoft/blob/main/PrincipalReviewer.agent.md?plain=1 to the newly created HxG_PrincipalReviewer.agent.md


3.a) Create a new file with the name 
```bash
HxG_SecurityOperations.agent.md
```
3.b) Copy the code from https://github.com/amrikhasler/Hexagon-TechDays26-Github-Copilot-Lab-Microsoft/blob/main/SecurityOperations.agent.md?plain=1 to the newly created HxG_SecurityOperations.agent.md


### Step 8:  Establish project principles

Launch your AI assistant in the project directory. The `/speckit.*` commands are available in the assistant.

Use the **`/speckit.constitution`** command to create your project's governing principles and development constitution and guidelines that will guide all subsequent development.

```bash
/speckit.constitution Fill in constitution leveraging ideation_demoschedulingapp.agent.md also create principles focused on code quality, testing standards, user experience consistency, and performance requirements
```

**Note:**

- please check and follow the steps Github Copilot is executing and allow to execute proposed commands or prompts
- you can either use **`/speckit.constitution`** to leverage agent or select in the Github Copilot prompt window the right agent under "set agent"

```bash
Fill in constitution leveraging ideation_demoschedulingapp.agent.md also create principles focused on code quality, testing standards, user experience consistency, and performance requirements
```
  
- here we also leverage the ideation_demoschedulingapp.agent which is considering the research content done via M365 Copilot Researcher


### Step 9: Create the specifications

Use the **`/speckit.specify`** command to describe what you want to build. Focus on the what and why, not the tech stack.

```bash
/speckit.specify Create specification for a simple scheduling app running local on port 8080 using local memory or storage but having a state of the art front end and backend (if needed) considering using blazor for the application.
```

**Note:**

- please check and follow the steps Github Copilot is executing and allow to execute proposed commands or prompts
- you can either use **`/speckit.specify`** to leverage agent or select in the Github Copilot prompt window the right agent under "set agent"

```bash
Create specification for a simple scheduling app running local on port 8080 using local memory or storage but having a state of the art front end and backend (if needed) considering using blazor for the application.
```


### Step 10: Create a technical implementation plan

Use the **`/speckit.plan`** command to provide your tech stack and architecture choices.

```bash
/speckit.plan create a technical implementation plan for the application using blazor
```

**Note:**

- please check and follow the steps Github Copilot is executing and allow to execute proposed commands or prompts
- you can either use **`/speckit.plan`** to leverage agent or select in the Github Copilot prompt window the right agent under "set agent"

```bash
create a technical implementation plan for the application using blazor
```


### Step 11: Break down into tasks

Use **`/speckit.tasks`** to create an actionable task list from your implementation plan.

```bash
/speckit.tasks create an actionable task list from your implementation plan.
```

**Note:**

- please check and follow the steps Github Copilot is executing and allow to execute proposed commands or prompts
- you can either use **`/speckit.tasks`** to leverage agent or select in the Github Copilot prompt window the right agent under "set agent"

```bash
create an actionable task list from your implementation plan.
```


### Step 12: Check project consistency 

Use **`/speckit.analyze`** to check the entire project regarding concisteny

```bash
/speckit.analyze Run a project analysis for consistency
```

**Note:**

- please check and follow the steps Github Copilot is executing and allow to execute proposed commands or prompts
- you can either use **`/speckit.analyze`** to leverage agent or select in the Github Copilot prompt window the right agent under "set agent"

```bash
Run a project analysis for consistency
```

### Step 13: Execute implementation

Use **`/speckit.implement`** to execute all tasks and build your feature according to the plan.

```bash
/speckit.implement execute all tasks and build your feature according to the plan. Remain basic and demo purposed. do not over complexify and make the app running local using local storage
```
**Note:**

- please check and follow the steps Github Copilot is executing and allow to execute proposed commands or prompts
- you can either use **`/speckit.implement`** to leverage agent or select in the Github Copilot prompt window the right agent under "set agent"

```bash
execute all tasks and build your feature according to the plan. Remain basic and demo purposed. do not over complexify and make the app running local using local storage
```

### Step 14: Review the application code 

Use **`/HxG_PrincipalReviewer`** to review the built application regarding code architecture, error handling patterns, API design, etc. 

```bash
HxG_PrincipalReviewer Review the scheduling app we built today. Focus on:
- Code architecture and organization
- Error handling patterns
- API design best practices
- React component structure
- Any potential bugs or issues
```

**Note:**

- please check and follow the steps Github Copilot is executing and allow to execute proposed commands or prompts
- you can either use **`/HxG_PrincipalReviewer`** to leverage agent or select in the Github Copilot prompt window the right agent under "set agent"

```bash
Review the scheduling app we built today. Focus on:
- Code architecture and organization
- Error handling patterns
- API design best practices
- React component structure
- Any potential bugs or issues
```
- This agent can be used for any future project or context. For each project you can individually adjust code and focus areas to match priorities


### Step 15: SecOps Check for the application 

Use **`/HxG_SecurityOperations`** to check and review the built application regarding vulnerabilities, injections risks, authentication and authorization issues, exposure etc. 

```bash
/HxG_SecurityOperations Review the scheduling app we built today. Focus on:
- Input validation vulnerabilities
- Storage injection or injection risks
- XSS vulnerabilities in the frontend
- Authentication/authorization issues
- Sensitive data exposure
- OWASP Top 10 concerns
```

**Note:**

- please check and follow the steps Github Copilot is executing and allow to execute proposed commands or prompts
- you can either use **`/HxG_SecurityOperations`** to leverage agent or select in the Github Copilot prompt window the right agent under "set agent"

```bash
Review the scheduling app we built today. Focus on:
- Input validation vulnerabilities
- Storage injection or injection risks
- XSS vulnerabilities in the frontend
- Authentication/authorization issues
- Sensitive data exposure
- OWASP Top 10 concerns
```
- This agent can be used for any future project or context. For each project you can individually adjust code and focus areas to match priorities
