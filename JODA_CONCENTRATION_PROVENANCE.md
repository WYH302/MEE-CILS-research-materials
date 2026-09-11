# JODA 浓度表来源

公开 `JODA_dataset.zip` 仅含 EEM/NMR/LC-MS 张量，不含论文 Table 1 的设计浓度。运行所用 `data/ucph_eem_data/joda_concentrations/joda_concentrations.csv` 从论文官方补充文件 Additional file 1 的 Table 1 逐行转录；只读取 EEM 可见的前三个化学组分。发布张量含 mixtures 1–26、28、29，不含 mixture 27。

- Europe PMC supplementary API：`https://www.ebi.ac.uk/europepmc/webservices/rest/PMC4117975/supplementaryFiles`
- 补充包 `PMC4117975_supplementary.zip`：878,620 bytes；SHA-256 `11941303BA18842EEDB06AC99DA794B7E4840ACC26E2AE5CB6BC4EA0E91C5A88`
- Additional file 1 PDF `12859_2013_6517_MOESM1_ESM.pdf`：47,119 bytes；SHA-256 `8A1F2D50F65AA4FC1203D32571FFE218D98AAB6A97874875B3A41EF35176554C`
- 转录 CSV：1,027 bytes；SHA-256 `A57EB78A81E5053D113457C9DDDB48457B90F54778AA02EA207C01251F4B7346`

2026-08-04 使用 TeX Live 2026 `pdftotext -layout` 重新抽取 PDF 表格文本，并逐行核对 29×5 个浓度单元；未发现差异。该核对为本地执行者复核，不替代外部独立复核。

该转录属于新独立重跑的输入补全，不是历史实验文件恢复。
