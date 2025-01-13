# Example Scenarios

> Note: The source diagram is located [here](https://github.com/usnistgov/OSCAL/issues/2012#issuecomment-2250898533)

## Diagram Subset Left Side

**Persona** Infrastructure Deployer
**Use Case** Agency1 with two different systems. One is leveraging another.

- OSCAL SSP x3
- OSCAL SRM
- OSCAL Component Definition

```mermaid
graph LR
  subgraph IaaS
    CSP1_SSP("CSP1 SSP/CSP1 FedRAMP SSP")
    Agency1_SSP1("Agency 1 SSP 1")
  end

  subgraph PaaS
    Agency1_SSP2("Agency 1 SSP 2")
  end

  CSP1_SSP -- CDef --> Agency1_SSP1
  Agency1_SSP1 -- SRM --> Agency1_SSP2
```

## Diagram Subset Right Side

**Persona** Infrastructure User and Platform Deployer
**Use Case** A PaaS is leveraging an IaaS authorization

- OSCAL SSP x3
- OSCAL SRM

```mermaid
graph LR
  subgraph IaaS
    CSP1_SSP("CSP1_SSP")
  end

  subgraph PaaS
    CSP2_SSP("CSP2 SSP")
    Agency2_SSP("Agency 2 SSP")
  end

  CSP1_SSP -- SRM --> CSP2_SSP
  CSP2_SSP -- SSP --> Agency2_SSP
```