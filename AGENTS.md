<skills_system priority="1">

## Available Skills

<!-- SKILLS_TABLE_START -->
<usage>
When users ask you to perform tasks, check if any of the available skills below can help complete the task more effectively.

How to use skills:
- Invoke: Bash("openskills read <skill-name>")
- The skill content will load with detailed instructions
- Base directory provided in output for resolving bundled resources

Usage notes:
- Only use skills listed in <available_skills> below
- Do not invoke a skill that is already loaded in your context
</usage>

<available_skills>

<skill>
<name>conductor-setup</name>
<description>Scaffolds the project and sets up the Conductor environment. Use this for project initialization.</description>
<location>project</location>
</skill>

<skill>
<name>conductor-track</name>
<description>Plans a new track (Feature/Bug), generates spec.md and plan.md, and updates the registry.</description>
<location>project</location>
</skill>

<skill>
<name>conductor-implement</name>
<description>Executes the tasks defined in a track's plan following the TDD implementation loop.</description>
<location>project</location>
</skill>

<skill>
<name>conductor-maintenance</name>
<description>Displays project status summaries and manages git-aware reverts of tasks or phases.</description>
<location>project</location>
</skill>

</available_skills>
<!-- SKILLS_TABLE_END -->

</skills_system>