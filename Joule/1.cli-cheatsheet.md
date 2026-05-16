# Joule Studio CLI - Developer Cheat Sheet


## Main CLI Documentation

https://help.sap.com/docs/joule/joule-development-guide-ba88d1ec6a1b442098863d577c19b0c0/joule-studio-cli-commands


---

# 1. Installation & Setup

## Install Latest Version

```bash
npm install -g @sap/joule-studio-cli
```

## Install Specific Version

```bash
npm install -g @sap/joule-studio-cli@<version>
```

## Update CLI

```bash
npm install -g @sap/joule-studio-cli --force
```

## Uninstall CLI

```bash
npm uninstall -g @sap/joule-studio-cli
```

> ⚠️ Run `joule logout` before uninstalling if you want to clear locally stored credentials/configuration.

## Verify Installation

```bash
joule -V
```

OR

```bash
joule --version
```

---

# 2. Help & Debugging

## Show Help

```bash
joule --help
```

## Enable Debug Logs

```bash
joule [command] -d
```

OR

```bash
joule [command] --debug
```

## Monochrome Output

```bash
joule [command] --no-color
```

---

# 3. Authentication Commands

## Login

```bash
joule login
```

## Login Using Default IDP

```bash
joule login --default-idp
```

## Login Using SSO Passcode

```bash
joule login --sso-passcode
```

## Login Using Environment Variables

```bash
joule login --use-env
```

OR

```bash
joule login --use-env <path>
```

### Supported Environment Variables

```env
JOULE_API_URL=
JOULE_USERNAME=
JOULE_PASSWORD=
JOULE_AUTH_URL=
JOULE_CLIENT_ID=
JOULE_CLIENT_SECRET=
JOULE_AUTH_SESSION=
JOULE_DEFAULT_IDP=
```

## Enable Password Storage

```bash
joule login --store-password
```

## Use Unsecure Storage

```bash
joule login --unsecure-storage
```

> ⚠️ NOT recommended.

## Logout

```bash
joule logout
```

## Check Login Status

```bash
joule status
```

---

# 4. Compile & Deployment Commands

## Basic Compile

```bash
joule compile
```

## Compile Specific Folder

```bash
joule compile <source_folder> <target_folder>
```

## Hide Warnings

```bash
joule compile --hide-warnings
```

## Set Batch Size

```bash
joule compile -b 10
```

## Basic Deploy

```bash
joule deploy
```

## Deploy Assistant

```bash
joule deploy ./my_assistant -n <assistant_name>
```

## Deploy Specific Config

```bash
joule deploy ./my_assistant/da.sapdas.yaml -n <assistant_name>
```

## Compile + Deploy Together

```bash
joule deploy --compile ./my_assistant
```

## Deploy Using Precompiled Capabilities

```bash
joule deploy ./my_assistant --daars-input-dir ./my_daar_folder
```

## Update Deployed Assistant

```bash
joule update <assistant_name> --capability-file <file_path>
```

---

# 5. Assistant Management Commands

## List Assistants

```bash
joule list
```

## Sort Assistants

```bash
joule list --sort name
```

## Get Assistant Details

```bash
joule get <assistant_name>
```

## Get Capability Details

```bash
joule get <assistant_name> -c <capability_name>
```

## Launch Assistant

```bash
joule launch <assistant_name>
```

## Delete Assistant

```bash
joule delete <assistant_name>
```

## Remove Capability

```bash
joule remove <assistant_name> --capability <namespace>:<capability_name>
```

---

# 6. Linting & Validation

## Run Linter

```bash
joule lint
```

## Lint with JSON Output

```bash
joule lint -f json:result.json
```

## Show Only Errors

```bash
joule lint --severity-level error
```

## Lint Specific Folder/File

```bash
joule lint <folder_or_file>
```

---

# 7. Most Common Development Workflow

## Initial Setup

```bash
npm install -g @sap/joule-studio-cli
joule login
joule status
```

## Daily Development Workflow

```bash
joule compile
joule lint
joule deploy
```

## Recommended Fast Workflow

```bash
joule deploy --compile ./my_assistant
```

## Troubleshooting Workflow

```bash
joule status
joule compile -d
joule deploy -d
```

---

# 8. Important Notes

- Custom capabilities must use `joule.ext` namespace.
- Use `lint` before deployment.
- `status` is first command during troubleshooting.
- Compile generates `.daar` artifacts.
- Avoid `--unsecure-storage` unless necessary.

