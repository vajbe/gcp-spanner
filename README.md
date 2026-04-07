# GCP Spanner Experiments

This repository contains my personal scratchpad and experiments for playing around with Google Cloud Spanner locally.

## Setup

Start the local Spanner emulator (which automatically creates a dummy instance and database):
```bash
docker-compose up -d
```

## Connecting via CLI

Connect to the local database to run SQL commands using the `spanner-cli`:
```powershell
$env:SPANNER_EMULATOR_HOST="localhost:9010" ; spanner-cli -p local-project -i local-instance -d local-db
```

*Note: The emulator runs entirely in memory. Restarting the docker container will permanently delete all tables and data.*
