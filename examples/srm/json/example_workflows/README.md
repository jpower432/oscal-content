# Example Scenarios

> Note: The source diagram is located [here](https://github.com/usnistgov/OSCAL/issues/2012#issuecomment-2250898533)

## Scope

IaaS and PaaS Cloud Service Providers

*Not explored here - Responsibility at the statement level*

## Diagram Subset 1

- OSCAL SSP x3
- OSCAL SRM

```mermaid
graph LR
  subgraph IaaS
    CSP1_SSP("CSP1 SSP")
  end

  subgraph PaaS
    CSP2_SSP("CSP2 SSP")
    Agency1_SSP("Agency 1 SSP")
  end

  CSP1_SSP -- SRM --> CSP2_SSP
  CSP2_SSP -- SSP --> Agency1_SSP
```

## Diagram Subset 2

- OSCAL SSP x3
- OSCAL SRM
- OSCAL Component Definitions

```mermaid
graph LR
  subgraph IaaS
    CSP1_SSP("CSP1 SSP")
    Agency2_SSP1("Agency 2 SSP 1")
  end

  subgraph PaaS
    Agency2_SSP2("Agency 2 SSP 2")
  end

  CSP1_SSP -- CDef --> Agency2_SSP1
  Agency2_SSP1 -- SRM --> Agency2_SSP2
```