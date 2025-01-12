# Project README

## Overview
This project is designed to generate and send payloads for customer data to an external endpoint. The system dynamically constructs payloads using modular components for identity, personal details, and subscriptions.

---

## Features
- **Dynamic Payload Generation:** Modular and reusable classes for constructing payload components.
- **Environment-Specific Configuration:** Endpoint and sandbox names are configurable using environment variables.
- **Scalability:** Easily extendable for additional data components in the payload.

---

## Requirements

- Python 3.8+
- Jupyter Notebook (optional for testing and demonstration)
- JSON data file for input

---

## Setup

### Step 1: Clone the Repository
```bash
git clone <repository-url>
cd <repository-directory>
```

### Step 2: Set Up Environment Variables
Export environment variables for your shell session:
```bash
export POST_URL="<your_post_url>"
export SANDBOX_NAME="<your_sandbox_name>"
.....
.....
```

Alternatively, you can define these variables in a shell script and source them:
```bash
source your_env_script.sh
```

### Step 3: Install Dependencies
Install any necessary Python libraries (if applicable):
```bash
pip install -r requirements.txt
```

Or only install directly using
```bash
pip install requests
```

---

## Usage

### Input File
Ensure the `users_data.json` file exists in the project root directory. This file should contain user data in JSON format.

### Run the Project
Run the Python script or Jupyter Notebook to generate and send payloads.

**Example (using Python script):**
Not created a python project, so import this as jupyter notebook

**Example (using Jupyter Notebook):**
1. Launch the notebook:
   ```bash
   jupyter notebook
   ```
2. Open the appropriate notebook file and run the cells.

---

## Key Classes

### 1. `IdentityData`
Generates identity-related information such as email, phone, and user ID.

### 2. `Person`
Generates personal details such as name, birth date, gender, etc.

### 3. `Subscription`
Generates subscription-related details like SKU, payment status, and subscriber information.

### 4. `XDMEntity`
Combines the identity, personal details, and subscription data into a unified entity.

### 5. `XDMPayloadGenerator`
Constructs the final payload and manages header and body sections for API submission.

---

## Configuration

- **`POST_URL`**: Target URL for submitting payloads.
- **`SANDBOX_NAME`**: Name of the sandbox environment.
.... and other env variables
---

## Example Workflow

1. Load user data from `users_data.json`.
2. Construct components (`IdentityData`, `Person`, and `Subscription`) for each user.
3. Create an `XDMEntity` instance combining the components.
4. Use `XDMPayloadGenerator` to generate the final payload.
5. Submit the payload to the target endpoint.

---

## Troubleshooting

### Environment Variables Not Detected
Ensure you have correctly exported the variables in the same shell session or sourced the appropriate script.

### Payload Validation Errors
Double-check the structure and values in your JSON input file. Ensure they conform to the expected format.

---

## Extending the Project
- Add new data components by creating additional classes.
- Update `XDMEntity` to include the new components.
- Modify `XDMPayloadGenerator` if new headers or body fields are required.

---

## Contact
For questions or support, contact [Your Name] at [anshulchoudhary1790@gmail.com].
