# YAML language syntax
1. YAML is used to write config files.
2. It is whitespace sensitive language. Indentation matters in YAML.
3. YAML has predefined keywords. 
  - name: define the workflow/job title
  - on: defines triggers (push, PR, schedule)
  - jobs: define jobs their OS, and steps.
  - steps: sequential commands or actions.  
  - run: Shell commands to execute.