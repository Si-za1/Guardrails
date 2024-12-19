# About Project
Implementation of basic guardrails approaches via guardrails AI, using RAIL and pydantic approach to use the guard.


# Guardrails AI

This project demonstrates the implementation of basic Guardrails approaches using Guardrails AI. Guardrails AI is a tool that helps in applying various safety checks and validation mechanisms for AI models, such as detecting PII (Personally Identifiable Information) and toxic language.

## Table of Contents
1. [Introduction](#introduction)
2. [Installation](#installation)
3. [Configuration](#configuration)
4. [Custom validators](#custom-validators)
4. [Using Validators](#using-validators)

## Introduction

This project leverages Guardrails AI to implement basic safety measures for your AI models. You can use this setup to ensure that your models follow predefined safety rules and avoid generating harmful content, such as personal information or toxic language.

## Installation

### Prerequisites

- Python 3.7 or higher
- A working internet connection for downloading the necessary packages and dependencies.

### Step 1: Install Guardrails AI

You can install the `guardrails-ai` Python package using pip:

```bash
pip install guardrails-ai
```

### Step 2: Create a Guardrails AI Account

1. Go to [Guardrails AI](https://www.guardrails.ai/) and create an account.
2. After signing up, generate your Guardrails Hub token.

### Step 3: Configure Guardrails AI on Your Terminal

Once you have the Guardrails Hub token, configure it in your terminal:

```bash
guardrails configure
```

This will prompt you to input your Guardrails Hub token.

# Validator implementation 
You can also use this custom validator in your model input processing to ensure your desired output. As in this project, we have ensured any food ingredient input is vegan-friendly.

#### Basic Guardrails Implementation
In addition to using pre-built validators, you can also create your own custom validators with Guardrails. 

Here's a preview of how to implement a custom validator that checks if a food ingredient is vegan:

**Preview:** You can create a custom validator by defining a class that inherits from Validator. The `validate()` method checks if a given value is in a list of non-vegan 
ingredients. If the ingredient is not vegan, it provides a fix by suggesting a vegan alternative.


For example, you might validate food ingredients like "milk" or "butter," and if found, replace them with vegan-friendly substitutes like "soy milk" or "margarine." 

``` bash
This is done using the PassResult and FailResult classes to indicate whether the validation passed or failed.
```

The full implementation of such a custom validator would look similar to this:

```bash
from guardrails.validators import Validator, register_validator, ValidationResult, PassResult, FailResult
```

## Using Validators

Guardrails offers a variety of pre-built validators that you can use to safeguard your AI models. Below are some example validators you can install and use:

### Example Validators:

- **Detect PII (Personally Identifiable Information)**:
  ```bash
  guardrails hub install hub://guardrails/detect_pii
  ```

- **Detect Toxic Language**:
  ```bash
  guardrails hub install hub://guardrails/toxic_language
  ```

You can install any other validator in a similar manner by searching the Guardrails Hub.

### Step 4: Using the Validators

Once you've installed the desired validators, you can apply them to your model or system, ensuring that your AI adheres to the safety guidelines defined by these validators.




### Key Sections:

1. **Introduction**: Describes what the project is about and the purpose of Guardrails AI.
2. **Installation**: Provides detailed steps to install the Guardrails AI package and set up the environment.
3. **Configuration**: Explains how to configure Guardrails on the terminal with your Guardrails Hub token.
4. **Using Validators**: Gives examples of how to install and use custom validators, validators from guardrails AI to safeguard AI systems.

