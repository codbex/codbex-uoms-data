# <img src="https://www.codbex.com/icon.svg" width="32" style="vertical-align: middle;"> codbex-uoms-data

## 📖 Table of Contents
* [📦 Data](#-data)
* [🔗 References](#-references)
* [🐳 Local Development with Docker](#-local-development-with-docker)

## 📦 Data 

* [Dimension](https://github.com/codbex/codbex-uoms-data/tree/main/codbex-uoms-data/dimension)
* [Uom](https://github.com/codbex/codbex-uoms-data/tree/main/codbex-uoms-data/uom) 

## 🔗 References

* [Guide for the Use of the International System of Units (SI)](https://physics.nist.gov/cuu/pdf/sp811.pdf)
* [Master List of Unit of Measures](https://help.sap.com/docs/SAP_Predictive_Maintenance_and_Service/a6d34dd348294e6daa2b3a5b601a4838/3471d66aa8c3417ea10b8deea2178f43.html)

## 🐳 Local Development with Docker

When running this project inside the codbex Atlas Docker image, you must provide authentication for installing dependencies from GitHub Packages.
1. Create a GitHub Personal Access Token (PAT) with `read:packages` scope.
2. Pass `NPM_TOKEN` to the Docker container:

    ```
    docker run \
    -e NPM_TOKEN=<your_github_token> \
    --rm -p 80:80 \
    ghcr.io/codbex/codbex-atlas:latest
    ```

⚠️ **Notes**
- The `NPM_TOKEN` must be available at container runtime.
- This is required even for public packages hosted on GitHub Packages.
- Never bake the token into the Docker image or commit it to source control.
