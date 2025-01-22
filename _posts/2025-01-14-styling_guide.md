---
layout: post
title: Styling Conventions Make Things Easier 
date: 2025-01-14
description: Personal framework for organizing files and projects
tags: 
categories: 
tabs: true
---


> A foolish consistency is the hobgoblin of little minds.
> — Guido van Rossum


<div class="row mt-3 justify-content-center">
    <div class="col-auto text-center">
        {% include figure.liquid 
        loading="eager" 
        path="assets/img/xkcd_file-names.png" 
        class="img-fluid rounded z-depth-1"
        width="300"
        height="200" %}
    </div>
</div>
<div class="caption">
    xkcd #1459 - Documents
</div>



Naming conventions are a personal framework for organizing work in a way that describes what they contain and how they relate to each other. File naming conventions, for instance, help stay organized as projects grow bigger and quickly identify work files. In a shared or collaborative group file-sharing setting, file naming conventions allow others to  easily navigate through the project. Similarly, coding conventions are programming language-specific guidelines that offer recommendations for writing clean and maintainable code. 

This page documents the guidelines for each of these tasks that I have personally found to be effective. Sticking to certain conventions helps organize my work and reduces downstream (or upstream) complexity when revisiting old projects or creating new ones.


## File Naming

When naming certain files, think about how they may be used in the future. Naming convention may differ based on file types.

### General Principles

1. Use lowercase letters to maintain consistency across systems.
2. Use hyphens (`-`) to separate words for readability.
3. Use underscores (`_`) to separate sections in the file name.
4. Include versioning (`v1`, `v2`, etc.) for iterative changes.
5. Add timestamps in `YYYYMMDD` format for chronological tracking, when necessary.
6. Use consistent extensions (`.md`, `.pdf`, `.jpg`, etc.) to reflect file types.

**Time Format** 
	Use the version date (use ISO 8601 format: YYYYMMDD or YYYY-MM-DD).
	Date formats can be very confusing. Use the standardized format to make sure your files can always be in a chronological order. 


**Delimiters**
- **Hyphens (`-`)**:
	    - Use for separating words within a **single section** of the file name.
	    - Improves readability, especially in filenames intended to describe a concept or a phrase (e.g., `iot-threat-model` or `privacy-engineering`).
- **Underscores (`_`)**:
	    - Use to separate **different sections** of the file name, such as project, functionality, version, or date.
	    - Useful to visually distinguish structural parts of the file name.


### Naming Structure

1. **Programming Projects**
	- **Format**: `<project-name>_<module-or-functionality>_<optional-context>_<version>.<file-extension>`
	- **Examples**:
		    - `network-tool_parser_v1.py` (Python script for a parser in a network tool project)
		    - `iot-security_analysis_v20250117.md` (Analysis for an IoT security project)
		    - `android-privacy_engine-v2.cpp` (C++ implementation of a privacy engine)

2. **Personal Notes**
	- **Research Notes**: `<topic>_<subtopic-or-keywords>_<timestamp>.<file-extension>`
	    - **Examples**:
	        - `blockchain_consensus-algorithms_20250117.md`
	        - `privacy_engineering_general-overview_2025.pdf`
	- **Technology Notes**: `<tech-name>_<context-or-focus>_<timestamp>.<file-extension>`
	    - **Examples**:
	        - `linux_networking_advanced_20250117.md`
	        - `python_asyncio-tutorial_2024.pdf`
	- **Research Statements**: `<statement-topic>_<version>.<file-extension>`
	    - **Examples**:
	        - `security-roadmap_v3.md`
	        - `iot-research-vision_v1.pdf`

 3. **Image Files**
	- **Format**: `<project-or-topic>_<context-or-description>_<timestamp>.<file-extension>`
	- **Examples**:
	    - `android-architecture-diagram_20250117.jpg`
	    - `iot-threat-model_visualization_v2.png`

4. **Miscellaneous Files**
	- Use generic names with descriptive elements and dates for non-categorized items.
	- **Examples**:
	        - `meeting-notes_privacy-research_20250117.md`
	        - `experiment-results_ml-v2_20250117.csv`


<br>

## Code Styling

<br>

> PEP-8 style guide has been an incredibly popular coding convention for Python, and rightfully so. While I personally would love to adopt the same styling for all languages, it is not that straightforward. Since I personally use Python the most I document most guidelines from the PEP-8 styling document. However, it is recommended to follow the style guide for that language.
>
>  
> [Google Style Guides](https://google.github.io/styleguide/) is probably the best resource for this.


<div class="row mt-3 justify-content-center">
    <div class="col-auto text-center">
        {% include figure.liquid 
        loading="eager" 
        path="assets/img/pep8-cheatsheet.png" 
        class="img-fluid rounded z-depth-1"
        %}
    </div>
</div>
<div class="caption">
    Python Code Styling Cheatsheet -- Google Style Guides
</div>


**File and Directory Naming**
1. **File Names**:
	   - Use lowercase letters with underscores to separate words.
	   - Keep file names descriptive but concise.
	   - **Examples**:
	     - `data_parser.py`
	     - `network_utility.py`
	     - `test_iot_security.py`
2. **Directory Names**:
	   - Use lowercase letters with underscores.
	   - Reflect the logical grouping of modules.
	   - **Examples**:
		 - `utils/`
		 - `data_processing/`
		 - `models/`

**Module Naming**
- Follow the same convention as file names: lowercase with underscores.
- Name modules after their primary functionality.
- **Examples**:
	- `data_cleaner.py`
	- `json_handler.py`

**Class Naming**
- Use the **PascalCase** convention (capitalize each word without underscores).
- Class names should be nouns representing objects or entities.
- **Examples**:
	  - `DataParser`
	  - `IoTSecurityAnalyzer`

**Function Naming**
- Use **snake_case** (lowercase with underscores).
- Function names should describe their action or purpose.
- **Examples**:
	- `parse_data()`
	- `validate_credentials()`
	- `get_network_status()`

**Variable Naming**
- Use **snake_case** for variables.
- Variables should be descriptive and indicate their purpose.
- Use short, clear names for local variables.
- **Examples**:
	- `user_input`
	- `file_path`
	- `connection_status`

**Constant Naming**
- Use **UPPERCASE_WITH_UNDERSCORES** for constants.
- Place constants at the top of the module or in a dedicated configuration file.
- **Examples**:
	- `API_KEY`
	- `DEFAULT_TIMEOUT`
	- `MAX_CONNECTIONS`

**Function Arguments**
- Use **snake_case** for argument names.
- Avoid single-character arguments except for standard cases (`i`, `j`, etc.).
- Provide default values where applicable.
- **Examples**:
	- `def connect_to_server(host, port=8080):`
	- `def filter_data(dataset, filter_type='default'):`

**Testing Naming Conventions**
1. **Test Files**:
   - Prefix with `test_` and match the name of the module being tested.
   - **Example**: `test_data_parser.py` tests `data_parser.py`.
2. **Test Functions**:
   - Use `test_` followed by the function or feature being tested.
   - **Examples**:
	- `test_parse_data()`
	- `test_connection_status()`

### General Styling Rules

1. **Indentation**: Use 4 spaces per indentation level.
2. **Line Length**: Limit to 79 characters for code and 72 characters for comments/docstrings.
3. **Imports**:
   - Group imports into three sections:
     1. Standard library imports.
     2. Third-party library imports.
     3. Local application imports.
   - Example:
	```python
	import os
	import sys
	
	import requests
	
	from my_project.utils import helper
	```
4. **Docstrings**:
   - Use triple double quotes (`"""`) for module, class, and function docstrings.
   - Describe the purpose, parameters, and return values.
   - **Example**:
	```python
		 def add_numbers(a, b):
			 """
			 Add two numbers.
		
			 Args:
				 a (int): The first number.
				 b (int): The second number.
		
			 Returns:
				 int: The sum of the two numbers.
			 """
		 return a + b
	```

This naming and styling convention ensures consistency, readability, and maintainability across your programming projects while adhering to PEP 8 standards.

### Source(s):

> 1. [Google Python Style Guide](https://google.github.io/styleguide/pyguide.html#3164-guidelines-derived-from-guidos-recommendations)

