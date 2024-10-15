## Agent Api

This repo contains the code for running an agent-api and supports 2 environments:

1. **dev**: A development environment running locally on docker
2. **prd**: A production environment running on AWS ECS

## Setup Workspace

1. [Install uv](https://docs.astral.sh/uv/#getting-started): `curl -LsSf https://astral.sh/uv/install.sh | sh`

> from the `agent-api` dir:

2. Install workspace and activate the virtual env:

```sh
./scripts/install.sh
source .venv/bin/activate
```

3. Setup workspace:

```sh
phi ws setup
```

4. Copy `workspace/example_secrets` to `workspace/secrets`:

```sh
cp -r workspace/example_secrets workspace/secrets
```

5. Optional: Create `.env` file:

```sh
cp example.env .env
```

## Run Agent Api locally

1. Install [docker desktop](https://www.docker.com/products/docker-desktop)

2. Set OpenAI Key

Set the `OPENAI_API_KEY` environment variable using

```sh
export OPENAI_API_KEY=sk-***
```

**OR** set in the `.env` file

3. Start the workspace using:

```sh
phi ws up
```

Open [localhost:8000/docs](http://localhost:8000/docs) to view the FastAPI docs.

4. Stop the workspace using:

```sh
phi ws down
```

## Next Steps:

- [Run the Agent Api on AWS](https://docs.phidata.com/templates/agent-api/run-aws)
- Read how to [manage the development application](https://docs.phidata.com/how-to/development-app)
- Read how to [manage the production application](https://docs.phidata.com/how-to/production-app)
- Read how to [add python libraries](https://docs.phidata.com/how-to/python-libraries)
- Read how to [format & validate your code](https://docs.phidata.com/how-to/format-and-validate)
- Read how to [manage secrets](https://docs.phidata.com/how-to/secrets)
- Add [CI/CD](https://docs.phidata.com/how-to/ci-cd)
- Add [database tables](https://docs.phidata.com/how-to/database-tables)
- Read the [Agent Api guide](https://docs.phidata.com/templates/agent-api)
