# Gmatic

### Solanum Lycopersicum

#### 1. gene annotation file
```
awk '{if($3=="mRNA"){print $0}}' ITAG3.2_gene_models.gff|cut -f 9-100 |awk 'BEGIN{FS=";";OFS="\t"}{print $2,$5}' |sed 's/Note=//g'|sed 's/Parent=gene://g'|sed 's/\.[1-9]//1d'|less -S > SL3.0.anno.tsv
```
