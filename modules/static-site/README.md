# Módulo: static-site

Crea un bucket S3 configurado como sitio web estático público.

## Uso

```hcl
module "site" {
  source          = "../../modules/static-site"
  bucket_name     = "devsecops-lab-dev-alejandra-perez-2026"
  index_file_path = "./website/index.html"
  environment     = "dev"
}
```

## Variables de entrada

| Nombre | Tipo | Requerida | Descripción |
|---|---|---|---|
| bucket_name | string | sí | devsecops-lab-dev-alejandra-perez-2026|
| index_file_path | string | sí | C:\Users\50378\OneDrive\Escritorio\ESEN\TERCER AÑO\CICLO3-AÑO3\NUBE\devsecops-pipeline-lab\website\index.html|
| environment | string | no (default: dev) | environment = "dev" |
| tags | map(string) | no |  Etiquetas adicionales para todos los recursos del módulo  |

## Salidas

| Nombre | Descripción |
|---|---|
| website_url | Uhttp://devsecops-lab-dev-alejandra-perez-2026.s3-website-us-east-1.amazonaws.com/ |
| bucket_arn | arn:aws:s3:::devsecops-lab-dev-alejandra-perez-2026 |