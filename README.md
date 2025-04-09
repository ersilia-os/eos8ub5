# Projections against Coconut

This tool performs PCA, UMAP and tSNE projections taking the Coconut natural products database as a chemical space of reference. The Ersilia Compound Embeddings are used as descriptors. Four PCA components and two UMAP and tSNE components are returned.

This model was incorporated on 2024-11-10.

## Information
### Identifiers
- **Ersilia Identifier:** `eos8ub5`
- **Slug:** `chemical-space-projections-coconut`

### Domain
- **Task:** `Representation`
- **Subtask:** `Projection`
- **Biomedical Area:** `Any`
- **Target Organism:** `Not Applicable`
- **Tags:** `Embedding`

### Input
- **Input:** `Compound`
- **Input Dimension:** `1`

### Output
- **Output Dimension:** `8`
- **Output Consistency:** `Fixed`
- **Interpretation:** Coordinates of 2D projections, namely PCA, UMAP and tSNE.

Below are the **Output Columns** of the model:
| Name | Type | Direction | Description |
|------|------|-----------|-------------|
| pca_1 | float |  | First principal component projected on the COCONUT chemical space represented with Ersilia Embeddings |
| pca_2 | float |  | Second principal component projected on the COCONUT chemical space represented with Ersilia Embeddings |
| pca_3 | float |  | Third principal component projected on the COCONUT chemical space represented with Ersilia Embeddings |
| pca_4 | float |  | Fourth principal component projected on the COCONUT chemical space represented with Ersilia Embeddings |
| umap_1 | float |  | First UMAP dimension projected on the COCONUT chemical space represented with Ersilia Embeddings |
| umap_2 | float |  | Second UMAP dimension projected on the COCONUT chemical space represented with Ersilia Embeddings |
| tsne_1 | float |  | First t-SNE dimension projected on the COCONUT chemical space represented with Ersilia Embeddings |
| tsne_2 | float |  | Second t-SNE dimension projected on the COCONUT chemical space represented with Ersilia Embeddings |


### Source and Deployment
- **Source:** `Local`
- **Source Type:** `Internal`
- **DockerHub**: [https://hub.docker.com/r/ersiliaos/eos8ub5](https://hub.docker.com/r/ersiliaos/eos8ub5)
- **Docker Architecture:** `AMD64`, `ARM64`
- **S3 Storage**: [https://ersilia-models-zipped.s3.eu-central-1.amazonaws.com/eos8ub5.zip](https://ersilia-models-zipped.s3.eu-central-1.amazonaws.com/eos8ub5.zip)

### Resource Consumption


### References
- **Source Code**: [https://github.com/ersilia-os/compound-embedding](https://github.com/ersilia-os/compound-embedding)
- **Publication**: [https://jcheminf.biomedcentral.com/articles/10.1186/s13321-020-00478-9](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-020-00478-9)
- **Publication Type:** `Peer reviewed`
- **Publication Year:** `2021`
- **Ersilia Contributor:** [miquelduranfrigola](https://github.com/miquelduranfrigola)

### License
This package is licensed under a [GPL-3.0](https://github.com/ersilia-os/ersilia/blob/master/LICENSE) license. The model contained within this package is licensed under a [GPL-3.0-or-later](LICENSE) license.

**Notice**: Ersilia grants access to models _as is_, directly from the original authors, please refer to the original code repository and/or publication if you use the model in your research.


## Use
To use this model locally, you need to have the [Ersilia CLI](https://github.com/ersilia-os/ersilia) installed.
The model can be **fetched** using the following command:
```bash
# fetch model from the Ersilia Model Hub
ersilia fetch eos8ub5
```
Then, you can **serve**, **run** and **close** the model as follows:
```bash
# serve the model
ersilia serve eos8ub5
# generate an example file
ersilia example -n 3 -f my_input.csv
# run the model
ersilia run -i my_input.csv -o my_output.csv
# close the model
ersilia close
```

## About Ersilia
The [Ersilia Open Source Initiative](https://ersilia.io) is a tech non-profit organization fueling sustainable research in the Global South.
Please [cite](https://github.com/ersilia-os/ersilia/blob/master/CITATION.cff) the Ersilia Model Hub if you've found this model to be useful. Always [let us know](https://github.com/ersilia-os/ersilia/issues) if you experience any issues while trying to run it.
If you want to contribute to our mission, consider [donating](https://www.ersilia.io/donate) to Ersilia!
