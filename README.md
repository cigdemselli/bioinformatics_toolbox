# bioinformatics_toolbox
R algorithms for common tasks in cancer bioinformatics

**`homologene_id_conversion`**

Provides code for converting mouse gene ids to human gene ids using `Homologene` database. `genes` is a vector of gene symbols or NCBI ids. `db` is Homologene database. Example usage: 
```
mouse2human(genes=genes, db = homologeneData2)
```

**`biomaRt_id_conversion`**

`id_convert` outputs a list of converted gene ids. Accepts 4 arguments: `dataset`, `filt`, `attr`, `id_list`. Example usage:
```
id_list <-  c("4288", "2064", "2099")
id_convert(dataset = "hsapiens_gene_ensembl",
           filt = "entrezgene_id",
           attr = "hgnc_symbol",
           id_list = id_list))
```

**`listfiles_mergeall`**

Outputs a matrix with merged xls files in a directory. An example scenario is when one needs to merge seperate FPKM.xls files from samples run in the same sequencing experiment. 
```
see the file listfiles_mergeall for usage
```


**`hpa_plot`**

Outputs graphs showing the levels of a gene in normal and cancer tissue based on Human Protein Atlas (HPA) database. Accepts 3 arguments: `gene`, `normal`, and `cancer`. Example usage:
```
hpa_plot(gene = "ENSG00000091831", normal = "breast", cancer = "breast cancer")
```
