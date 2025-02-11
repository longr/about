---
title: How to make a workflow RO-crate
redirect_from: /how-to-make-a-workflow-ro-crate/
---

More info about workflow RO-crate specification can be found in our [Workflow-RO-Crate](/Workflow-RO-Crate/) section.

## 1. Using the WorkflowHub website

The most convenient way to make a workflow RO-crate at this moment is by making use of WorkflowHub capabilities. The website is able to generate RO-crates based on an uploaded/referenced workflow file and some general metadata that is requested through a form.  After the workflow is [registered](/docs/registering-a-workflow) for more info about this topic) it is possible to download the RO-crate with the download button. 

The generated RO-crate, basically a zip file, will contain these elements:

- **JSONLD file**: JSONLD serving machine-readable metadata including: 
  - Author
  - Contents and structure
  - Project
  - Original URL
  - License
  - Publisher
  - Date Published
  - creativeWorkStatus
  - Programming Language
  - Based on
  
  The metadata properties are based on the [BioSchemas workflow profile](https://bioschemas.org/profiles/Workflow)  .

- **HTML file**: A web page serving the metadata in a human-readable way.
  - Original URL
  - Author (creators)
  - License
  - Contents

- **Main Workflow file**: The workflow file itself, if uploaded.

- **Main Workflow Diagram (optional)**: A diagram visualizing the steps in the workflow, if uploaded or generated from CWL.

- **Main Workflow CWL Description (optional)**: This file can be included if supplied by the user.

## 2. Making one offline yourself

We are working on a python package at this moment to wrap your own RO-crates. This will allow you to not be bounded by the file limitations of the WorkflowHub website (workflow + CWL abstract and/or diagram), and will make it possible to automate the RO-Crate generation.
The python package can be found in [ResearchObject/ro-crate-py](https://github.com/ResearchObject/ro-crate-py).
