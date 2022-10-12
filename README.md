<h2 align="center">KiboCommerce, Next.JS & Contentful </h2>

<p align="center">
This is a headless ecommerce starter kit for Import space content using contentful cli<br>
</p>

### Features

- Import space content from existing space 

## Getting Started

1. Follow the below steps provided into "###Import space content" section

### Import space content

## Prerequisites

    Contentful account
    CLI installed on your machine: npm install -g contentful-cli

## Steps - Export

1. Clone github repository
```bash
git clone https://github.com/KiboSoftware/contentful-space.git
```
2. open export "export-source-space.config.json" 
Replace values of spaceId/environmentId/managementToken/deliveryToken 

3. Login to Source/Export Space 
   open your terminal at cloned directory and run this command to log in to the CLI session:

```bash
contentful login  #This command will ask you to open browser & copy access token from browser & paste it on cli.
```
Or 

```bash
contentful login --management-token <management-token> #Settings > API keys > Content management tokens > Generate personal token
```

4. After successful login, run this command to export your space’s content to the “space” folder:
   Syntax
   contentful space export --space-id <space_id> --config “<path_to_export_source-space-config>”

For example:

```bash
contentful space export --space-id lwp********* --config export-source-space.config.json
```

## Steps - Import

1. open export "import-target-space.config.json" 
Replace values of spaceId/managementToken

3. Login to Target/Import Space 
   open your terminal at cloned directory and run below commands to log in to the CLI session:

```bash
contentful logout #This commands will logout from existing session then login to import/target space
contentful login  #This command will ask you to open browser & copy access token from browser & paste it on cli.
```
Or 

```bash
contentful login --management-token <management-token> #Settings > API keys > Content management tokens > Generate personal token
```

4. After successful login, run this command to import your existing space’s content to the import/target space:
   Syntax
   contentful space import --config “<path_to_import_target-space-config>”

For example:

```bash
contentful space import --config import-target-space.config.json
```

## Built with

- CMS - Contentful

## Contributions

All contributions welcome!

```

```
