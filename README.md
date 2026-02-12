# 🤔 What is Spec-Driven Development?

Spec-Driven Development **flips the script** on traditional software development. For decades, code has been king — specifications were just scaffolding we built and discarded once the "real work" of coding began. Spec-Driven Development changes this: **specifications become executable**, directly generating working implementations rather than just guiding them.

Let's start with the Lab!!!

## Step 1: Astral’s uv installer script - install uv (not required if you already have it installed) 

Make sure you have the right path where you want to create your project later (typically: C:\Users\FirstName_LastName\source\Dev\Projects\...)

Copy the following prompt to the github copilot chat (allow proposed steps and actions by Github Copilot):

```bash
irm https://astral.sh/uv/install.ps1 | iex
```


## Step 2: Install Specify CLI

Choose your preferred installation: 

### Option A) One-time Usage (Recommended for this Lab)

Run directly without installing. Copy the prompt bellow to github copilot:

```bash
uvx --from git+https://github.com/github/spec-kit.git specify init <PROJECT_NAME>
```

### Option B) Persistent Installation 

Install once and use everywhere:

```bash
uv tool install specify-cli --from git+https://github.com/github/spec-kit.git
```

Then use the tool directly. Copy the prompt bellow to github copilot:

```bash
# Create new project
specify init <PROJECT_NAME>

# Or initialize in existing project
specify init . --ai claude
# or
specify init --here --ai claude

# Check installed tools
specify check
```

To upgrade Specify, see the [Upgrade Guide](./docs/upgrade.md) for detailed instructions. Quick upgrade:

```bash
uv tool install specify-cli --force --from git+https://github.com/github/spec-kit.git
```


## Step 3: You will be asked to provide a project name: 

```bash
HxG_Demo_SchedullingApp
```


## Step 4: Open "focus terminal" in the Github Copilot chat. 

You will find it directly in the chat where you executed the prompt in step 2, after the sub step called "planned project naming as "HxG_Demo_SchedullingApp". Choose your AI assistant using your keyboard to navigate to --> copilot (Github Copilot) and press enter


## Step 5: Remain in the focus terminal 

You now get asked to choose script type. Navigate with your keyboard to --> ps (pwerShell) and press enter


## Step 6: Now go to file in VS Code 

open folder e.g. "C:\Users\FirstName_LastName\source\Dev\Projects\...\HxG_Demo_SchedullingApp" to set the right path


## Step 7: Custom Agents

In this step we create custom agents.

### Option A) Create new .md file in the .github\agents folder

1.a) Create a new file with the name
```bash
HxG_ideation_demoschedulingapp.agent.md
```
1.b) Copy the code from https://github.com/amrikhasler/Hexagon-TechDays26-Github-Copilot-Lab-Microsoft/blob/main/ideation_demoschedulingapp.agent.md to the newly created HxG_ideation_demoschedulingapp.agent.md

2.a) Create a new file with the name
```bash
HxG_PrincipleReviewer.agent.md
```
2.b) Copy the code from https://github.com/amrikhasler/Hexagon-TechDays26-Github-Copilot-Lab-Microsoft/blob/main/PrincipleReviewer.agent.md to the newly created HxG_PrincipleReviewer.agent.md

3.a) Create a new file with the name 
```bash
HxG_SecurityOperations.agent.md
```
3.b) Copy the code from https://github.com/amrikhasler/Hexagon-TechDays26-Github-Copilot-Lab-Microsoft/blob/main/SecurityOperations.agent.md to the newly created HxG_PrincipleReviewer.agent.md



## Step 3:  Establish project principles

Launch your AI assistant in the project directory. The `/speckit.*` commands are available in the assistant.

Use the **`/speckit.constitution`** command to create your project's governing principles and development constitution and guidelines that will guide all subsequent development.

```bash
/speckit.constitution Fill in constitution leveraging ideation_demoschedulingapp.agent.md also create principles focused on code quality, testing standards, user experience consistency, and performance requirements
```

**Note::**

- you can either use **`/speckit.constitution`** to leverage agent or select in the Github Copilot prompt window the right agent under "set agent"
- here we also leverage the ideation_demoschedulingapp.agent which is considering the research content done via M365 Copilot Researcher 
