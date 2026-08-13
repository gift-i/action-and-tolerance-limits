# action-and-tolerance-limits
$\paragraph{} \verb|GI_local_gamma_notebook.ipynb|$ calculates the Action Limits (AL) and Tolerance Limits (TL) for structures in the Prostate scans created on pinnacle, and plots the gamma passing rates (%GP), its mean and median, AL and TL for each structure. $\verb|plotting.ipynb|$ uses the output csv files to replot these histograms as individual images, for easier integration into the report and presentation. 

#### Python Libraries used
$\begin{itemize}
    \item numpy
    \item matplotlib.pyplot
    \item os
    \item scipy.stats
    \item pandas
    \item json
\end{itemize}$


### $\verb|GI_local_gamma_notebook.ipynb| $
$\paragraph{}$ This notebook extracts data from Pat_Eval.json files containing information on the gamma analysis on the structures in Pinnacle prostate scans only, as these PatEval files were downloaded on my device. The PatEval files from the the gamma analysis of the other scans (both rectal and prostate scans from RayStation and the rectal scans from Pinnacle) were were generated on the remote computer and could not be uploaded onto my device. This python note book outputs the following variables as csv files: 
$\begin{itemize}
    \item patients_df and patients_df_2 - tables consisting of the patient ID (anonymised), \%GP and the name or decription of each structure.
    \item structures_df -  a table just like patients_df_2 but does not contain the patient ID (used for plotting)
    \item results_df - contains a column of structures, TL and AL. 
    \item stats_df - contains a column of structures, mean, median and standard deviation for the \%GPs.
    \item histogram plots
\end{itemize}$


### $\verb|plotting.ipynb|$
$\paragraph$ This replots the histogram and also contains a Mann-Whitney U test to compare the two treatment planning systems.


