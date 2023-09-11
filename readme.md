# Test mermaid
[https://mermaid.js.org/syntax/flowchart.html]

```mermaid
flowchart TB

  subgraph Processing
    direction TB
    gha("GHA
      workflow") <-- "(2) workflow trigger" -->env["Environment
    Prod"]
  end

  psmod("📘 Powershell Module") <-. From Artifactoy .-> gha
  env <-- "(3) Api Calls" --> dg("Central")

  subgraph Artifact
    direction TB
    gha -- "(4) Artifact Download" ----> dcert("Cert")
  end

  repo(("Git Repo")) -- "(1)" ----> gha
```
