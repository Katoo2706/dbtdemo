# Run DBT in dev environment
> #TODO: Create `.env` file from `.env.example` before running DBT in development

## Initial
Install packages
```bash
# cd dbt-claim-extraction

pip3 install -r requirements.txt
```

Load environment variables from .env file
```bash
export $(grep -v '^#' .env | xargs)
```

Health-check (Optional `--target dev` flag)
```bash
dbt debug
```

## Run
Run transformation step for dev
```bash
dbt run
```