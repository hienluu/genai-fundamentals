## Example Prompts for Each Pattern

### Input Semantics
| Ask for Input Pattern |
|--------|
|From now on, translate anything I write into a series emojis. Ask me for the first thing to translate. Ask me for the first task and don't add any preamble or postamble statements|
| From now on, translate anything I write into a series of sounds and actions from a dog that represent the dogs reaction to what I write. Ask me for the first task and don't add any preamble or postamble statements |

| Meta Language Pattern |
|--------|
|I would like to plan a vacation. I would like you to list interesting things to do in places that I will pass through. When I say “CityA,3->CityB,2”, I mean that my route will go from CityA to CityB and that I will stay 3 days in CityA and 2 days in CityB.|


### Output Customization
| Persona Pattern |
|--------|
|Act as a skeptic that is well-versed in computer science. Whatever I tell you, provide a skeptical and detailed response There is a concern that AI is going to replace everyone’s job|
|You are going to pretend to be a Linux terminal for a computer that has been compromised by an attacker. When I type in a command, you are going to output the corresponding text that the Linux terminal would produce.|

| Audience Persona Pattern |
|--------|
|Explain large language model and how they work for me.  Assume that I am a freshman in high school and have a short attention span|
|Explain large language model and how they work for me.  Assume that I only accept explanation in math|
|Explain large language model and how they work for me.  Assume that I am [historical figure name]|


| Template #1 |
|--------|
|I am going to give you a template for your output. CAPITALIZED WORDS are my placeholders. Fill in the placeholders with your output.  Please make sure to preserve the overall formatting of the template.  My template is:<br>\*\*\*\*Question\*\*\*\* QUESTION<br>\*\*\*\*Answer:\*\*\*\* ANSWER<br>I will now provide the data to format in the next prompt and you will create ten questions using the template. |
|Instruction: now go to a wiki page, copy a section of text and paste in the prompt|

| Template #2 |
|--------|
|I am going to give you a template for your output. CAPITALIZED WORDS are my placeholders. Fill in the placeholders with your output.<br>Please make sure to preserve the overall formatting of the template.  My template is:<br><br>### Bio:  &lt;NAME&gt;<br>****ExecutiveSummary:****  &lt;ONE SENTENCE SUMMARY&gt;<br>****Full Description:****  &lt;ONE PARAGRAPH SUMMARY&gt;<br>I will now provide the data to format in the next prompt and you will create ten questions using the template. |
|Instruction: now go to a wiki page of of a famous figure, copy a few paragraphs and paste in the prompt|

| Recipe Pattern |
|--------|
|I would like to purchase a house. I know that I need to perform steps make an offer and close on the house. Provide a complete sequence of steps for me. Fill in any missing steps.|
|I would like to drive to NYC from Nashville. I know that I want to go through Asheville, NC on the way and that I don't want to drive more than 300 miles per day. Provide a complete sequence of steps for me. Fill in any missing steps.|

| Outline Expansion Pattern |
|--------|
|Act as an outline expander. Generate a bullet point outline based on the input that I give you and then ask me for which bullet point<br>you should expand on.  Create a new outline for the bullet point that I select. At the end, ask me for what bullet point to expand next.<br><br>Ask me for what to outline|

### Ineternaction Patterns
| Menu Actions Pattern #1|
|--------|
|Act as an outline expander. Generate a bullet point outline based on the input that I give you and then ask me for which bullet point you should expand on.  Create a new outline for the bullet point that I select. At the end, ask me for what bullet point to expand next.<br>Whenever I type “write &lt;bullet point&gt; &lt;paragraph&gt;”, you will write content for the selected bullet point &lt;bullet point&gt;. You will write &lt;paragraph&gt; of text. Whenever I type just “&lt;bullet point&gt;” you will expand that bullet point.  At the end, it is very important that you will ask me for the next action.<br><br>Ask me for what to outline|

| Menu Actions Pattern #2|
|--------|
|Whenever I type: "add FOOD", you will add FOOD to my grocery list and update my estimated grocery bill. Whenever I type "remove FOOD", you will remove FOOD from my grocery list and update my estimated grocery bill. Whenever I type "list", you show me the grocery list. Whenever I type "save" you will list alternatives to my added FOOD to save money. At the end, you will ask me for the next action. <br><br>Ask me for the first action|

| Flipped Interaction Pattern|
|--------|
|Ask me questions about my weight loss goals until you have sufficient information to propose a fitness training program for me. When you have enough information, show me the fitness training program.<br><br>Ask me the first question.|

| Game Play Pattern|
|--------|
|Let’s play a game about prompt engineering.  You are going to give me a simple task that can be accomplished via prompting you. All your tasks should have a reasoning or programming component to them, however they shouldn’t require writing code.<br><br>I will try to write a prompt to you to solve the task.  You will give me the output of my prompt and then tell me how well it solved the task.  You will ask me a question, wait for my response, and then ask me another question after tell me how I did.<br><br>Ask me the first question|

| Game Play Pattern|
|--------|
|I want you to act as my Machine Learning Interviewer. Conduct my technical interview for the Junior Machine Learning Engineer position. Please ask me a series of questions to evaluate my knowledge and skills in machine learning, and provide feedback on my responses unless I ask you to stop.<br><br>Let’s start with the first question|


### Prompt Improvement
| Question Refinement Pattern|
|--------|
|Whenever I ask a question, suggest a better question and ask me if I would like use it instead.|
|Instruction: after the prompt, type in Should I go to the University of Washington?|

| The Alternative Approaches Pattern|
|--------|
|From now on, if there are alternative ways to accomplish the same thing, list the best alternate approaches. Compare and contrast the alternatives and ask me which one I want to use.|
|For every prompt I give you, If there are alternative ways to word a prompt that I give you, list the best alternate wordings . Compare/contrast the pros and cons of each wording and ask me which one to use.|

###  Error Identification
| Error Identification  |
|--------|
|Example|
