# Joule Studio CLI - Developer Cheat Sheet

## Main CLI Documentation

https://help.sap.com/docs/joule/joule-development-guide-ba88d1ec6a1b442098863d577c19b0c0/joule-studio-cli-commands

<br>

## Daily Dev Commands

| Command |
| :--- |
| `joule compile` |
| `joule lint` |
| `joule deploy` |

<br><br>

---


# 1. Installation & Setup

| Action | Command | Notes |
| :--- | :--- | :--- |
| Install Latest Version | ```bash\nnpm install -g @sap/joule-studio-cli\n``` | Recommended setup |
| Install Specific Version | ```bash\nnpm install -g @sap/joule-studio-cli@<version>\n``` | Use for project-specific versions |
| Update CLI | ```bash\nnpm install -g @sap/joule-studio-cli --force\n``` | Force updates latest version |
| Uninstall CLI | ```bash\nnpm uninstall -g @sap/joule-studio-cli\n``` | Run `joule logout` before uninstall |
| Verify Installation | ```bash\njoule -V\n``` | OR `joule --version` |

<br><br>

---

# 2. Help & Debugging

| Action | Command | Usage |
| :--- | :--- | :--- |
| Show Help | ```bash\njoule --help\n``` | List all commands |
| Enable Debug Logs | ```bash\njoule [command] -d\n``` | Troubleshooting |
| Debug Alternative | ```bash\njoule [command] --debug\n``` | Same as `-d` |
| Disable Colors | ```bash\njoule [command] --no-color\n``` | Useful for logs/CI |

<br><br>

---

# 3. Authentication Commands

| Action | Command | Notes |
| :--- | :--- | :--- |
| Login | ```bash\njoule login\n``` | Standard login |
| Login Using Default IDP | ```bash\njoule login --default-idp\n``` | Uses configured IDP |
| Login Using SSO Passcode | ```bash\njoule login --sso-passcode\n``` | Browser-based authentication |
| Login Using Environment Variables | ```bash\njoule login --use-env\n``` | Supports env-based auth |
| Login Using Env File | ```bash\njoule login --use-env <path>\n``` | Load env from file |
| Store Password | ```bash\njoule login --store-password\n``` | Stores credentials securely |
| Unsecure Storage | ```bash\njoule login --unsecure-storage\n``` | Avoid unless necessary |
| Logout | ```bash\njoule logout\n``` | Ends current session |
| Check Status | ```bash\njoule status\n``` | First troubleshooting step |

---

## Supported Environment Variables

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

<br><br>

---

# 4. Compile & Deployment Commands

| Action | Command | Notes |
| :--- | :--- | :--- |
| Basic Compile | ```bash\njoule compile\n``` | Generates `.daar` artifacts |
| Compile Specific Folder | ```bash\njoule compile <source_folder> <target_folder>\n``` | Custom paths |
| Hide Warnings | ```bash\njoule compile --hide-warnings\n``` | Cleaner output |
| Set Batch Size | ```bash\njoule compile -b 10\n``` | Custom batch processing |
| Basic Deploy | ```bash\njoule deploy\n``` | Standard deployment |
| Deploy Assistant | ```bash\njoule deploy ./my_assistant -n <assistant_name>\n``` | Deploy specific assistant |
| Deploy Specific Config | ```bash\njoule deploy ./my_assistant/da.sapdas.yaml -n <assistant_name>\n``` | Deploy using config file |
| Compile + Deploy | ```bash\njoule deploy --compile ./my_assistant\n``` | Recommended workflow |
| Deploy Precompiled Capabilities | ```bash\njoule deploy ./my_assistant --daars-input-dir ./my_daar_folder\n``` | Uses precompiled `.daar` |
| Update Assistant | ```bash\njoule update <assistant_name> --capability-file <file_path>\n``` | Update deployed assistant |

<br><br>

---

# 5. Assistant Management Commands

| Action | Command | Notes |
| :--- | :--- | :--- |
| List Assistants | ```bash\njoule list\n``` | View all assistants |
| Sort Assistants | ```bash\njoule list --sort name\n``` | Sort output |
| Get Assistant Details | ```bash\njoule get <assistant_name>\n``` | Assistant details |
| Get Capability Details | ```bash\njoule get <assistant_name> -c <capability_name>\n``` | Specific capability info |
| Launch Assistant | ```bash\njoule launch <assistant_name>\n``` | Open assistant |
| Delete Assistant | ```bash\njoule delete <assistant_name>\n``` | Remove assistant |
| Remove Capability | ```bash\njoule remove <assistant_name> --capability <namespace>:<capability_name>\n``` | Remove capability |

<br><br>

---

# 6. Linting & Validation

| Action | Command | Notes |
| :--- | :--- | :--- |
| Run Linter | ```bash\njoule lint\n``` | Validate project |
| JSON Output | ```bash\njoule lint -f json:result.json\n``` | Export lint results |
| Show Only Errors | ```bash\njoule lint --severity-level error\n``` | Cleaner output |
| Lint Specific File/Folder | ```bash\njoule lint <folder_or_file>\n``` | Targeted validation |

<br><br>

---


# 7. Important Notes

| Topic | Notes |
| :--- | :--- |
| Namespace | Custom capabilities should use `joule.ext` |
| Validation | Run `lint` before deployment |
| Troubleshooting | Start with `joule status` |
| Compile Output | Generates `.daar` artifacts |
| Security | Avoid `--unsecure-storage` unless necessary |
| Recommended Workflow | `deploy --compile` is most practical |
