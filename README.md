# Large-Scale-DEG-Analysis-with-DESeq2-
This R script automates differential expression analysis for up to 100 samples in one execution. It utilizes DESeq2 to process multiple RNA-Seq datasets, identify differentially expressed genes (DEGs), and generate key visualizations.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
  <h2>📌 Features:</h2>
  <ul>
    <li>⚡ <strong>Batch Processing:</strong> Efficiently processes multiple RNA-Seq datasets at once.</li>
    <li>📊 <strong>DEG Analysis:</strong> Uses DESeq2 to identify significant differential expression.</li>
    <li>📈 <strong>Automated Visualizations:</strong> Generates PCA plots for variance and Volcano plots for DEGs.</li>
    <li>🚀 <strong>Parallel Execution:</strong> Optimized to run on multiple cores for faster processing.</li>
  </ul>

  <h2>🛠 Dependencies:</h2>
  <p>To run this script, you will need to install the following R packages:</p>
  <pre>
  install.packages(c("ggplot2", "dplyr"))
  BiocManager::install(c("DESeq2", "BiocParallel", "ggrepel"))
  </pre>

  <h2>📂 File Structure:</h2>
  <pre>
  - parent_dir/
    - subfolder1/
      - metadata.csv
      - count_data.csv
    - subfolder2/
      - metadata.csv
      - count_data.csv
    - ...
  </pre>
  <p>The script expects each subfolder to contain a <code>metadata.csv</code> file and a count data file (CSV format). The count file should contain the RNA-Seq counts, while the metadata file contains sample information such as condition labels (e.g., "HPV" and "Normal").</p>

  <h2>🚀 How It Works:</h2>
  <ol>
    <li>The script processes multiple subfolders containing RNA-Seq data.</li>
    <li>For each subfolder, it reads the <code>metadata.csv</code> and count data CSV files.</li>
    <li>The DESeq2 package is used to perform differential expression analysis.</li>
    <li>PCA and Volcano plots are generated to visualize the variance and DEG results.</li>
    <li>The results, including significant DEGs, are saved as CSV files.</li>
    <li>The script is optimized for parallel execution, allowing it to process datasets faster using multiple CPU cores.</li>
  </ol>

  <h2>📊 Output Files:</h2>
  <ul>
    <li><strong>PCA Plot:</strong> Visual representation of sample variance (saved as PNG).</li>
    <li><strong>Volcano Plot:</strong> Highlights significantly differentially expressed genes (saved as PNG).</li>
    <li><strong>Enhanced Volcano Plot:</strong> Includes labels for significant genes (saved as PNG).</li>
    <li><strong>DEGs File:</strong> A CSV file containing significant DEGs with adjusted p-values < 0.05 (saved as CSV).</li>
  </ul>

  <h2>💡 Key Libraries Used:</h2>
  <ul>
    <li><strong>DESeq2:</strong> A Bioconductor package for differential gene expression analysis.</li>
    <li><strong>dplyr:</strong> For data manipulation and filtering.</li>
    <li><strong>ggplot2:</strong> For generating plots such as PCA and Volcano plots.</li>
    <li><strong>BiocParallel:</strong> For parallel processing to speed up large-scale data analysis.</li>
    <li><strong>ggrepel:</strong> To add labels to Volcano plots, improving readability.</li>
  </ul>

  <h2>📈 Example Output:</h2>
  <img src="PCA_plot_with_variance.png" alt="PCA Plot Example" width="500">
  <img src="volcano_plot.png" alt="Volcano Plot Example" width="500">
  <img src="enhanced_volcano_plot.png" alt="Enhanced Volcano Plot Example" width="500">

</body>
</html>
