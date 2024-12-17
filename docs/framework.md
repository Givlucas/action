# Introduction
Action is an experimental task / documentation framework that uses
directed acyclic meta graphs (DAMG) to organise tasks based on their 
dependancies on others. These graphs, which we will call "action graphs", 
break down the relationship between what actions need to be completed 
to create the desired results. As well as providing a framework for 
keeping track of what actions need to be done Action seeks to keep track 
of the why. By enforcing a documentation structure for each action, details 
about the why and how decisions were made and excuted allows teams to aduit 
the result of their efforts in an agile way. Aditionally Action provides
a rigid structure for describe the current progress state of an action.

# The Action Graph
Action uses a directed acyclic meta graph to define temporal relationships
between tasks. Each node in the graph represents a task or "action". Each 
action has its "inputs" and its "outputs". Outputs can be defined as what
is changed or is created during an action. Inputs are what actions need to be
done before a action can be completed. Edges in graph represent the linking
between an output an input. For example lets say you have a action
node to write a paper. An input for that action might be a literature review.
The action graph is said to be a "Meta graph" because each action node can 
contain its own action graph related specific to its task. This enables a 
cleaner break down of a project.

# The Documentation
The action graph would be usefull on its own, but without a way of defining
what an action should do / did do, it would be easy to loose track of whats 
going on. For this reason Action defines a "White paper" document that occompanies
each task which is broken down into five sections.

1. Title - Action to be preformed
2. Statement of action - Why of action
3. Statement of inputs - other actions relied on
4. Statement of specifications. What Attributes outputs of the action should have
5. Statement of design - Precise directions on how the action will be done. 
  Think methods from a lab. 
  Sections:
	2. Design - directions for the action (Method)
	3. Outputs - for the action (results)
6. Analysis of impact - Did this action have the expected impact on the project?

Additionally Action defines six stages of development that describes which section
of the white paper should be completed during the stage. 

1. Discovery - Identify problem to be solved and record scope of problem if applicable, 
  explore solutions, tools, and possible hangups.
	- Outputs: Title, Statement of specifications, Statement of Action, Statement of inputs 
    generic notes
2. Design - Create a clear and detailed explanation / algorithm for process. 
  Pick the tools you will use.
	- Outputs: Statement of design, Statement of outputs
3. Implement - Implement according to design. Do not alter in this stage.
	- Outputs: outputs
4. Test - verify that action meets specifications from the design step
	- Outputs: tests on outputs
5. Document - User guide, action comments if not present and or a white paper / section on 
  action functionality. What impact does solution have
	- Outputs: User guide (optional), Analysis of impact
6. Publish - publish outputs of actions and documentation to appropriate location

# The Workflow
Each stage describes the current state of a node. The state of the action progresses
forward, but you can revert to any lower state at any time. However once reverted to
a lower state you cannot skip forward and must re-evalute each associated section of 
the white paper.

Each node starts in the discovery phase. This allows you to outline what the action is, (Title)
why the action needs to be accomplished (Statement of action), add in any known inputs
(Statement of inputs), and any know specifications ( Statement of specifications). 
At this stage you might discover you needs to create some new action to support the current. 
This allows you to work backwards creating a graph that describes what needs to be done to complete your task.

If a task is very complex you can create a seperate action graph for that node.
This allows you to sperate concerns and keep the parent graph from being polluted 
with tasks unique to one specifc action.

# Example
Lets say your goal is create a research paper, you could outline the steps you want 
to accomplish using action. First, you would create a action node for "Write research 
paper". Staring in the "Discovery" phase your goal is to identify what exactly needs 
to be completed, why it needs to be completed and learn about the scope of the problem. 
For our example we might fill our white paper out like this

- Title: Write a research paper
- Statment of action: We need to write a paper detailing our reseach on \[BLANK\]
- Statement of inputs:
1. Literature review
2. Experimentation & data

We will skip detailing the input action nodes for brevity, assume they have been completed. 
During this phase we might also do some research on paper layouts 
and standardizations to support our design in the next phase. If we already have an idea
of some qualities our action should have we should detail them in the "Statement of
Specifications"

Next we would enter the "Design" phase. Here we can layout an outline of our paper, what
tools we will be using to write the paper and what standards we will be using. Things like
did we use LaTex or word? Did we use APA or some other standard. We would also describe
what exactly the output of this action will be. In our case it would be something like 
"A research paper on \[BLANK\] written in \[BLANK\] using \[Blank\]".

Now that our design is done we switch over to the "implenetation" phase. Here we would
actually write the paper following our design from the previous phase.
Next we would enter the "Design" phase. Here we can layout an outline of our paper, what
tools we will be using to write the paper and what standards we will be using. Things like
did we use LaTex or word? Did we use APA or some other standard. We would also describe
what exactly the output of this action will be. In our case it would be something like 
"A research paper on \[BLANK\] written in \[BLANK\] using \[Blank\]".

Now that our design is done we switch over to the "implenetation" phase. Here we would
actually write the paper following our design from the previous phase.

Not all phases apply exactly to all tasks. In this case the "testing" phase, would more
be having our peers review our paper. If they offer up an suggestions or changes we could
revert to the design stage and then move forward into implement and repeat till
it passes our tests.

Next we would be in the "Documentation" phase. This might be compiling experimental data to 
be shared along with the paper.

Then we can finally move on to the "Publish" phase. Here we would submit out paper to a journal
or proffesor or simply post it online for others to access. This stage focuses on making the output
avaible for the audience or userbase.
