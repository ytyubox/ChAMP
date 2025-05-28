## ✅ R studio 成功 library("ChAMP") 安裝流程
環境：
1. macOS 15.4
2. R language 4.1.1 from https://cran.r-project.org/src/base/R-4/
3. R Studio 2025.05.0+496（2025.05.0+496） `brew install --cask rstudio`

### ChAMP 安裝 Flow

1. 重複使用 `library("ChAMP")` 檢查是否安裝完成
2. 查看錯誤訊息，得知缺少 package，如 `there is no package called ’THE_PACKAGE’`
3. 使用 BiocManager::install("THE_PACKAGE") 嘗試
4. 可能會失敗，改用 BiocManager::install("THE_PACKAGE", type="binary") 嘗試

## 常見問題

1. ❌ Error: package or namespace load failed for 'ChAMP' in loadNamespace(j <- i[[1L]], c(lib.loc, .libPaths()), versionCheck = vI[[j]]): there is no package called 'GO.db'
  ✅ 使用 `BiocManager::install("GO.db")`
2. ❌ `Warning message: package 'kpmt' is not available for Bioconductor version '3.14'`
  ✅ 使用 `BiocManager::install("kpmt", type="binary")`
3. ❌ `Warning messages: package(s) not installed when version(s) same as or greater than current; use force = TRUE to re-install: 'org.Hs.eg.db'`
  ✅ 使用 `BiocManager::install("org.Hs.eg.db", ask=FALSE, force=TRUE)`

## 指令記錄 `savehistory(PATHTOSAVE)`

### 2025/5/28

```R
if (!requireNamespace("BiocManager", quietly = TRUE))
  install.packages("BiocManager")

BiocManager::install("ChAMP")
library("ChAMP")

BiocManager::install("bumphunter")
library("ChAMP")

BiocManager::install("doRNG")
library("ChAMP")

BiocManager::install("RSQLite")
library("ChAMP")

BiocManager::install("httr")
library("ChAMP")

BiocManager::install("KernSmooth")
library("ChAMP")

BiocManager::install("progress")
library("ChAMP")

BiocManager::install("mclust")
library("ChAMP")

BiocManager::install("base64")
library("ChAMP")

BiocManager::install("ChAMP", dependencies=TRUE)
library("ChAMP")

BiocManager::install("readr")
library("ChAMP")

BiocManager::install("jpeg")
library("ChAMP")

BiocManager::install("interp")
BiocManager::install("interp")
library("ChAMP")

BiocManager::install("Hmisc")
library("ChAMP")

BiocManager::install("Hmisc", type="binary")
library("ChAMP")

BiocManager::install("shiny", type="binary")
library("ChAMP")

BiocManager::install("IlluminaHumanMethylation450kanno.ilmn12.hg19", type="binary")
library("ChAMP")

BiocManager::install("IlluminaHumanMethylation450kanno.ilmn12.hg19")
library("ChAMP")

BiocManager::install("IlluminaHumanMethylationEPICanno.ilm10b4.hg19")
library("ChAMP")

BiocManager::install("org.Hs.eg.db")
BiocManager::install("org.Hs.eg.db", ask=FALSE)
BiocManager::install("org.Hs.eg.db", ask=FALSE, force=TRUE)
library("ChAMP")

BiocManager::install("IlluminaHumanMethylationEPICmanifest", ask=FALSE, force=TRUE)
library("ChAMP")

BiocManager::install("DT", ask=FALSE, force=TRUE)
library("ChAMP")

BiocManager::install("IlluminaHumanMethylation450kmanifest", ask=FALSE, force=TRUE)
library("ChAMP")

BiocManager::install("nleqslv", ask=FALSE, force=TRUE)
library("ChAMP")

BiocManager::install("fastICA", ask=FALSE, force=TRUE)
library("ChAMP")

BiocManager::install("plotly", ask=FALSE, force=TRUE)
BiocManager::install("ChAMP", ask=FALSE, force=TRUE)
library("ChAMP")

BiocManager::install("GO.db", ask=FALSE, force=TRUE)
library("ChAMP")

BiocManager::install("geneLenDataBase", ask=FALSE, force=TRUE)
library("ChAMP")

library("ChAMP")

BiocManager::install("kpmt", ask=FALSE, force=TRUE)
library("ChAMP")

library("ChAMP")

BiocManager::install("kpmt", ask=FALSE, force=TRUE)
BiocManager::install("kpmt", type="binary")
library("ChAMP")
packageVersion("ChAMP")
[1] '2.24.0'
```

![success load library](./success%20load.png)
