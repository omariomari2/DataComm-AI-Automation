# DataComm automation exercises

An attempt to automate order processing and customer reporting.
This repository contains work from a Forage job simulation.

The Python code checks customer records, checks stock, and records order outcomes.
Provider interfaces separate the workflow from email, customer, and inventory services.

## Run locally

Use Python 3.
Run these commands from the repository directory:

```sh
python run_agent_poc.py
python TEST_CASES.py
```

The first command processes three sample orders with mock providers.
It records four messages in memory and reduces ITEM001 stock from 50 to 49.
It does not send real email.

The second command runs three existing export tests.

## Current limits

The order workflow uses local data and mock services.
It does not connect to Salesforce, Google Sheets, or a live inbox.
It does not use a language model to process orders.

The earlier proposal describes intended benefits.
Its timing and accuracy targets are not measured results.

## Details

- [Workflow implementation](order_bot.py)
- [Provider interfaces](interfaces.py)
- [Mock services](mocks.py)
- [Customer data processing](process_data.py)
- [Original technical proposal](technical_spec.md)

