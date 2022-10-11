# Cell atlas of the developing human brain
Data and code related to our manuscript *Comprehensive cell atlas of the first-trimester developing human brain* (Emelie Braun, Miri Danan-Gotthold et al. 2022, in review).

## Preprint (bioRxiv)

(Coming soon)

## Code
We used the [Shoji](https://github.com/linnarsson-lab/shoji) tensor database and the [cytograph-shoji](https://github.com/linnarsson-lab/cytograph-shoji) pipeline.

Code for making many of the figures is available as [Jupyter notebooks](notebooks/README.md)

## Downloads
Metadata per sample: [table_S1.xlsx](https://github.com/linnarsson-lab/developing-human-brain/files/9755355/table_S1.xlsx)

Metadata per cluster: [table_S2.xlsx](https://github.com/linnarsson-lab/developing-human-brain/files/9755350/table_S2.xlsx)

Raw data: [EGAS00001004107](https://ega-archive.org/studies/EGAS00001004107)

Complete processed dataset: [HumanFetalBrainPool.h5](https://storage.googleapis.com/linnarsson-lab-human/HumanFetalBrainPool.h5)

The complete processed dataset is a HDF5 file containing the tensors listed below. The most important tensors are Expression (the expression matrix; sum of spliced and unspliced UMIs), Gene (gene names), Accession (Ensembl accessions), Clusters (cluster labels), Embedding (tSNE), Factors (PCA components), ManifoldIndices (KNN graph edges)and ManifoldWeights (KNN graph edge weights).

<table><tbody><tr><th></th><th>dtype</th><th>rank</th><th>dims</th><th>shape</th><th>(values)</th></tr><tr><td align="left"><strong>Accession</strong></td><td align="left">string</td><td align="left">1</td><td>genes</td><td>59,480</td><td>["pCAG-DsRed2_101-650", "pCS-Cherry-DEST_101-850", "pCAG ···</td></tr><tr><td align="left"><strong>Age</strong></td><td align="left">float32</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>[8.0, 8.0, 8.0, 8.0, 8.0, ...]</td></tr><tr><td align="left"><strong>AnnotationDefinition</strong></td><td align="left">string</td><td align="left">1</td><td>annotations</td><td>51</td><td>["+MPZ", "+EYA1 +ISL1", "+NHLH1", "+MEIS2 +ISL1 +SIX3",  ···</td></tr><tr><td align="left"><strong>AnnotationDescription</strong></td><td align="left">string</td><td align="left">1</td><td>annotations</td><td>51</td><td>["Schwann cell-like (E-SCHWL; +MPZ)", "Otic vesicle of t ···</td></tr><tr><td align="left"><strong>AnnotationName</strong></td><td align="left">string</td><td align="left">1</td><td>annotations</td><td>51</td><td>["E-SCHWL", "HB-OTV", "NBL", "TH-RETN", "CB-PURK", ...]</td></tr><tr><td align="left"><strong>AnnotationPosterior</strong></td><td align="left">float32</td><td align="left">2</td><td>clusters ✕ annotations</td><td>617 ✕ 51</td><td>[[-1.8189894e-12, 6.617445e-24, 1.0, 3.3087225e-24, 3.30 ···</td></tr><tr><td align="left"><strong>CellClass</strong></td><td align="left">string</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>["Erythrocyte", "Erythrocyte", "Erythrocyte", "Erythrocy ···</td></tr><tr><td align="left"><strong>CellCycleFraction</strong></td><td align="left">float32</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>[0.0, 0.0001071352, 0.0, 0.00095663266, 0.0, ...]</td></tr><tr><td align="left"><strong>CellID</strong></td><td align="left">string</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>["10X89_1:AAACGGGAGGCTACGA", "10X89_1:ACGAGGAAGAGCCTAG", ···</td></tr><tr><td align="left"><strong>Chemistry</strong></td><td align="left">string</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>["v2", "v2", "v2", "v2", "v2", ...]</td></tr><tr><td align="left"><strong>Chromosome</strong></td><td align="left">string</td><td align="left">1</td><td>genes</td><td>59,480</td><td>["chrEXTRA", "chrEXTRA", "chrEXTRA", "chrEXTRA", "chrEXT ···</td></tr><tr><td align="left"><strong>Class</strong></td><td align="left">string</td><td align="left">1</td><td>clusters</td><td>617</td><td>["Neuroblast", "Radial glia", "Radial glia", "Glioblast" ···</td></tr><tr><td align="left"><strong>ClusterID</strong></td><td align="left">uint32</td><td align="left">1</td><td>clusters</td><td>617</td><td>[0, 1, 2, 3, 4, ...]</td></tr><tr><td align="left"><strong>Clusters</strong></td><td align="left">uint32</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>[240, 240, 236, 240, 233, ...]</td></tr><tr><td align="left"><strong>Donor</strong></td><td align="left">string</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>["BRC2006", "BRC2006", "BRC2006", "BRC2006", "BRC2006", ...]</td></tr><tr><td align="left"><strong>DoubletFlag</strong></td><td align="left">bool</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>[False, False, False, False, False, ...]</td></tr><tr><td align="left"><strong>DoubletScore</strong></td><td align="left">float32</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>[0.02, 0.02, 0.03, 0.01, 0.02, ...]</td></tr><tr><td align="left"><strong>DropletClass</strong></td><td align="left">uint8</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>[0, 0, 0, 0, 0, ...]</td></tr><tr><td align="left"><strong>Embedding</strong></td><td align="left">float32</td><td align="left">2</td><td>cells ✕ 2</td><td>1,665,937 ✕ 2</td><td>[[22.061909, 11.055673], [23.594717, 10.600938], [25.339 ···</td></tr><tr><td align="left"><strong>End</strong></td><td align="left">string</td><td align="left">1</td><td>genes</td><td>59,480</td><td>["550", "1320", "2090", "3610", "4730", ...]</td></tr><tr><td align="left"><strong>Enrichment</strong></td><td align="left">float32</td><td align="left">2</td><td>clusters ✕ genes</td><td>617 ✕ 59,480</td><td>[[1.0, 1.0, 1.0, 1.0, 1.0, ...], [1.0, 1.0, 1.0, 1.0, 1. ···</td></tr><tr><td align="left"><strong>Expression</strong></td><td align="left">uint16</td><td align="left">2</td><td>cells ✕ genes</td><td>1,665,937 ✕ 59,480</td><td>[[0, 0, 0, 0, 0, ...], [0, 0, 0, 0, 0, ...], [0, 0, 0, 0 ···</td></tr><tr><td align="left"><strong>Factors</strong></td><td align="left">float32</td><td align="left">2</td><td>cells ✕ __</td><td>1,665,937 ✕ 50</td><td>[[-1.5914472, 1.524089, 0.21222332, -4.3109193, -5.85292 ···</td></tr><tr><td align="left"><strong>Gene</strong></td><td align="left">string</td><td align="left">1</td><td>genes</td><td>59,480</td><td>["marker-DsRed", "marker-Cherry", "marker-GFP", "marker- ···</td></tr><tr><td align="left"><strong>GeneNonzeros</strong></td><td align="left">uint32</td><td align="left">1</td><td>genes</td><td>59,480</td><td>[0, 0, 0, 0, 0, ...]</td></tr><tr><td align="left"><strong>GeneTotalUMIs</strong></td><td align="left">uint32</td><td align="left">1</td><td>genes</td><td>59,480</td><td>[0, 0, 0, 0, 0, ...]</td></tr><tr><td align="left"><strong>Linkage</strong></td><td align="left">float32</td><td align="left">2</td><td>__ ✕ 4</td><td>616 ✕ 4</td><td>[[238.0, 239.0, 0.0016231078, 2.0], [237.0, 617.0, 0.002 ···</td></tr><tr><td align="left"><strong>Loadings</strong></td><td align="left">float32</td><td align="left">2</td><td>genes ✕ __</td><td>59,480 ✕ 50</td><td>[[0.0, 0.0, 0.0, 0.0, 0.0, ...], [0.0, 0.0, 0.0, 0.0, 0. ···</td></tr><tr><td align="left"><strong>ManifoldIndices</strong></td><td align="left">uint32</td><td align="left">2</td><td>__ ✕ 2</td><td>40,164,783 ✕ 2</td><td>[[0, 6], [0, 106], [0, 208], [0, 225], [0, 246], ...]</td></tr><tr><td align="left"><strong>ManifoldRadius</strong></td><td align="left">float32</td><td align="left">0</td><td>()</td><td>()</td><td>1.0</td></tr><tr><td align="left"><strong>ManifoldWeights</strong></td><td align="left">float32</td><td align="left">1</td><td>__</td><td>40,164,783</td><td>[0.9746674, 0.9753966, 0.97435904, 0.9760038, 0.98073715 ···</td></tr><tr><td align="left"><strong>MeanAge</strong></td><td align="left">float64</td><td align="left">1</td><td>clusters</td><td>617</td><td>[10.651846331718932, 10.967863210449874, 10.768960981864 ···</td></tr><tr><td align="left"><strong>MeanCellCycle</strong></td><td align="left">float64</td><td align="left">1</td><td>clusters</td><td>617</td><td>[0.002357223176804402, 0.003319249633509612, 0.023186484 ···</td></tr><tr><td align="left"><strong>MeanDoubletScore</strong></td><td align="left">float64</td><td align="left">1</td><td>clusters</td><td>617</td><td>[0.09462042097992746, 0.11769588179965942, 0.19775236498 ···</td></tr><tr><td align="left"><strong>MeanExpression</strong></td><td align="left">float64</td><td align="left">2</td><td>clusters ✕ genes</td><td>617 ✕ 59,480</td><td>[[0.0, 0.0, 0.0, 0.0, 0.0, ...], [0.0, 0.0, 0.0, 0.0, 0. ···</td></tr><tr><td align="left"><strong>MeanTotalUMI</strong></td><td align="left">float64</td><td align="left">1</td><td>clusters</td><td>617</td><td>[5449.63220088626, 5258.164957264958, 7567.301298701311, ···</td></tr><tr><td align="left"><strong>MitoFraction</strong></td><td align="left">float32</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>[0.0, 0.0038568673, 0.008797339, 0.0015943878, 0.0018687 ···</td></tr><tr><td align="left"><strong>NCells</strong></td><td align="left">uint64</td><td align="left">1</td><td>clusters</td><td>617</td><td>[1354, 1170, 770, 1232, 1536, ...]</td></tr><tr><td align="left"><strong>NGenes</strong></td><td align="left">uint32</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>[121, 271, 674, 101, 113, ...]</td></tr><tr><td align="left"><strong>Nonzeros</strong></td><td align="left">uint64</td><td align="left">2</td><td>clusters ✕ genes</td><td>617 ✕ 59,480</td><td>[[0, 0, 0, 0, 0, ...], [0, 0, 0, 0, 0, ...], [0, 0, 0, 0 ···</td></tr><tr><td align="left"><strong>OverallTotalUMIs</strong></td><td align="left">uint64</td><td align="left">0</td><td>()</td><td>()</td><td>13029800607</td></tr><tr><td align="left"><strong>PrevClusters</strong></td><td align="left">uint32</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>[658, 658, 662, 658, 669, ...]</td></tr><tr><td align="left"><strong>Recipe</strong></td><td align="left">string</td><td align="left">1</td><td>__</td><td>2</td><td>["{'InitializeWorkspace': {'from_workspace': 'samples202 ···</td></tr><tr><td align="left"><strong>Region</strong></td><td align="left">string</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>["Telencephalon", "Telencephalon", "Telencephalon", "Tel ···</td></tr><tr><td align="left"><strong>SampleID</strong></td><td align="left">string</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>["10X89_1", "10X89_1", "10X89_1", "10X89_1", "10X89_1", ...]</td></tr><tr><td align="left"><strong>SelectedFeatures</strong></td><td align="left">bool</td><td align="left">1</td><td>genes</td><td>59,480</td><td>[False, False, False, False, False, ...]</td></tr><tr><td align="left"><strong>Sex</strong></td><td align="left">string</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>["", "", "", "", "", ...]</td></tr><tr><td align="left"><strong>Species</strong></td><td align="left">string</td><td align="left">0</td><td>()</td><td>()</td><td>"Homo sapiens"</td></tr><tr><td align="left"><strong>Start</strong></td><td align="left">string</td><td align="left">1</td><td>genes</td><td>59,480</td><td>["1", "571", "1341", "2111", "3631", ...]</td></tr><tr><td align="left"><strong>StdevExpression</strong></td><td align="left">float32</td><td align="left">1</td><td>genes</td><td>59,480</td><td>[0.0, 0.0, 0.0, 0.0, 0.0, ...]</td></tr><tr><td align="left"><strong>Subdivision</strong></td><td align="left">string</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>["Cortex", "Cortex", "Cortex", "Cortex", "Cortex", ...]</td></tr><tr><td align="left"><strong>Subregion</strong></td><td align="left">string</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>["Cortex", "Cortex", "Cortex", "Cortex", "Cortex", ...]</td></tr><tr><td align="left"><strong>Tissue</strong></td><td align="left">string</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>["Cortex", "Cortex", "Cortex", "Cortex", "Cortex", ...]</td></tr><tr><td align="left"><strong>TopLevelCluster</strong></td><td align="left">uint32</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>[25, 25, 25, 25, 25, ...]</td></tr><tr><td align="left"><strong>TotalUMIs</strong></td><td align="left">uint32</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>[4630, 9334, 9321, 3136, 4281, ...]</td></tr><tr><td align="left"><strong>Trinaries</strong></td><td align="left">float32</td><td align="left">2</td><td>clusters ✕ genes</td><td>617 ✕ 59,480</td><td>[[-1.8189894e-12, -1.8189894e-12, -1.8189894e-12, -1.818 ···</td></tr><tr><td align="left"><strong>UnsplicedFraction</strong></td><td align="left">float32</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>[0.3514039, 0.33833298, 0.3174552, 0.32589287, 0.3585611 ···</td></tr><tr><td align="left"><strong>ValidCells</strong></td><td align="left">bool</td><td align="left">1</td><td>cells</td><td>1,665,937</td><td>[True, True, True, True, True, ...]</td></tr><tr><td align="left"><strong>ValidGenes</strong></td><td align="left">bool</td><td align="left">1</td><td>genes</td><td>59,480</td><td>[False, False, False, False, False, ...]</td></tr></tbody></table>
