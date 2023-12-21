DIA data analysis
==============================

Overall summary
---------------

.. _table:

=================================================  ==========  ===================  ==============  ==============  ==============  ========
Name                                               Pub date    Dev stat             Stra.           x-first         Interface       Acce.
=================================================  ==========  ===================  ==============  ==============  ==============  ========
Ion Accounting [#IonAccounting]_                   2009 Mar.   /                    R               /               /               C
ETISEQ [#ETISEQ]_                                  2009 Aug.   Not                  R               /               C               F
DeMux [#DeMux]_                                    2009 Dec.   /                    R               /               /               R
Skyline [#Skyline]_                                2010 Apr.   Active               L               C               C & G           O
FT-ARM [#FTARM]_                                   2012 Jan.   Not                  S/L             S               C & G           F
Spectronaut [#Spectronaut]_                        2013        Active               R,L             C               C & G           C
OpenSWATH [#OpenSWATH]_                            2014 Mar.   Active               L               C               C & G           O
DIANA [#DIANA]_                                    2014 Oct.   Not                  L               C               C               O
DIA-Umpire [#DIAUmpire]_                           2015 Jan.   Active               R,L             /,C             C & G           O
SWATHProphet [#SWATHProphet]_                      2015 Feb.   Not                  L               C               C               O
Group-DIA  [#GroupDIA]_                            2015 Oct.   Not                  R,L             /,C             C               O
MSPLIT-DIA  [#MSPLITDIA]_                          2015 Nov.   Not                  L               S               C               F
PECAN (Walnut) [#PECAN]_                           2017 Aug.   Active               S               S               C & G           O
Specter [#Specter]_                                2018 Apr.   Not                  L               S               C               O
EncyclopeDIA [#EncyclopeDIA]_                      2018 Dec.   Active               L               S               C & G           O
DeepNovo-DIA [#DeepNovoDIA]_                       2018 Dec.   Not                  D               C               C               O
PEAKS [#PEAKS]_                                    2018        Active               S,L,D           N               C & G           C
DIA-NN [#DIANN]_                                   2019 Nov.   Active               L               C               C & G           F
DIA tensor [#DIAT]_                                2020 Oct.   Not                  I               /               C               F
MaxDIA [#MaxDIA]_                                  2021 July   Active               L               C               C & G           F
DIAmeter [#DIAmeter]_                              2021 July   Active               S               S               C               O
FIGS [#FIGS]_                                      2021 July   Not                  L               S               C               O
mstc [#mstc]_                                      2021 July   Not                  I               /               C               O
CsoDIAq [#CsoDIAq]_                                2021 Sep.   Active               L               S               C & G           O
DreamDIA\ :sup:`XMBD` [#DreamDIAXMBD]_             2021 Oct.   Not                  L               C               C               O
Dear-DIA\ :sup:`XMBD` [#DearDIAXMBD]_              2023 June   Active               R               /               C & G           F
MSFragger-DIA [#MSFraggerDIA]_                     2023 July   Active               S               S               C & G           F
=================================================  ==========  ===================  ==============  ==============  ==============  ========

.. note::
   - *Pub date (publication date)*: the date the tool was publicly released by publisher
      - *Spectronaut* is noted by its public release date (first publication was in 2015 [#Spectronaut]_)
      - *PEAKS* is noted by the date it supported the analysis of DIA data (PEAKS X in 2018)
      - *MSFragger-DIA* is noted by its related publication date (and the function has been available in 2020)
   - *Dev stat (development status)*
      - Active: has update of any type in last one year (e.g. response of question from authors on GitHub issues, document update, bug fix, and feature update)
      - Not: not active
      - *PECAN* is re-implemented as Walnut and is being maintained and upgraded
   - *Stra. (analysis strategies)* (note: some functions for analysis of other data type, like DDA, are not included)
      - R: spectra reconstruction
      - S: sequence-based search
      - L: library-based search
      - D: de novo sequencing
      - I: sequencing-independent
   - *x-first (spectrum-/chromatogram-first analysis approaches)*
      - S: spectrum-first
      - C: chromatogram-first
      - N: unknown
      - /\: 
      - *DIA-Umpire* and *Group-DIA* work for two functions\: 1. spectra reconstruction, which belongs to neither approach; 2. targeted re-extraction for quantification, which has a chromatogram-first approach
      - *DeepNovo-DIA* works for de novo sequencing
   - (User) interface
      - C: command line interface (CLI)
      - G: graphical user interface (GUI) 
      - Note\: the following software get their GUI support from accompanying tools or platforms -- OpenSWATH\: TOPPAS, GALAXY; DIA-Umpire\: FragPipe; PECAN (Walnut)\: EncyclopeDIA; MSFragger-DIA\: FragPipe
   - *Acce. (accessibility)*
      - C: commercial
      - F: free access
      - O: open source (whilst, free access)
      - R: need request from authors
      - N: not mentioned in the paper

|

Individuals
-----------

|

Ion Accounting
^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#IonAccounting] Database searching and accounting of multiplexed precursor and product ion spectra from the data independent analysis of simple and complex peptide mixtures. 10.1002/pmic.200800564

======================  =============================================================================================================================
Full name               Ion Accounting
Authors                 Guo-Zhong Li et al.
Lab & Company           Waters Corporation
Publication date        2009 Mar.
Analysis strategies     Spectra reconstruction and seqeunce-based search on extracted precursor-fragment ion pairs
======================  =============================================================================================================================

:Function: spectra reconstruction + seqeunce-based search

======================  =============================================================================================================================
Pre-processing          Ion detection based on 2D-convolution
Ion grouping criteria   Apex RT
Fragment assignment     One-to-multi (reassigned according to matching quality in sequence-based search step)
======================  =============================================================================================================================


ETISEQ
^^^^^^

back to table_

:Reference: 

.. [#ETISEQ] ETISEQ - an algorithm for automated elution time ion sequencing of concurrently fragmented peptides for mass spectrometry-based proteomics. 10.1186/1471-2105-10-244

======================  =============================================================================================================================
Full name               Elution Time Ion Sequencing
Authors                 Jason WH Wong et al.
Lab & Company           Wong Lab
Publication date        2009 Aug.
Analysis strategies     Spectra reconstruction
======================  =============================================================================================================================

:Function: spectra reconstruction

======================  =============================================================================================================================
Pre-processing          Potential contaminant signal removing
Ion grouping criteria   PCC and cross-correlation lag
Fragment assignment     1. One-to-multi; 2. unmatched fragments are assigned to all precursor
======================  =============================================================================================================================


DeMux
^^^^^

back to table_

:Reference: 

.. [#DeMux] Deconvolution of Mixture Spectra from Ion-Trap Data-Independent-Acquisition Tandem Mass Spectrometry. 10.1021/ac901801b

======================  =============================================================================================================================
Full name               DeMux
Authors                 Marshall Bern et al.
Lab & Company           MacCoss Lab
Publication date        2009 Dec.
Analysis strategies     Spectra reconstruction
======================  =============================================================================================================================

:Function: spectra reconstruction

======================  =============================================================================================================================
Pre-processing          Coarse spectral binning
Ion grouping criteria   (No precursor requirement) correlation between m/z bins in MS2 spectral map
Fragment assignment     One-to-multi, but the cluster center (seed) is dropped in each iteration
======================  =============================================================================================================================


Skyline
^^^^^^^

back to table_

:Reference: 

.. [#Skyline] Skyline: an open source document editor for creating and analyzing targeted proteomics experiments. 10.1093/bioinformatics/btq054
.. [#Skyline2] A framework for installable external tools in Skyline. 10.1093/bioinformatics/btu148
.. [#Skyline3] Multiplexed peptide analysis using data-independent acquisition and Skyline. 10.1038/nprot.2015.055
.. [#Skyline4] Using Skyline to Analyze Data-Containing Liquid Chromatography, Ion Mobility Spectrometry, and Mass Spectrometry Dimensions. 10.1007/s13361-018-2028-5
.. [#Skyline5] The Skyline ecosystem: Informatics for quantitative mass spectrometry proteomics. 10.1002/mas.21540

======================  =============================================================================================================================
Full name               Skyline
Home page               https://skyline.ms/project/home/software/Skyline/begin.view
Source code             https://github.com/ProteoWizard/pwiz
Programming language    C#
Authors                 Brendan X. MacLean et al.
Lab & Company           MacCoss Lab
Publication date        2010 Apr.
Analysis strategies     Library-based search
======================  =============================================================================================================================

:Function: Library-based search

======================  =============================================================================================================================
Analysis approach       Chromatogram-first
Minimum scoring unit    Peak group
Scoring model           (mProphet) linear classifier; (Avant-Garde) combination of sub-scores with fixed parameters
======================  =============================================================================================================================


FT-ARM
^^^^^^

back to table_

:Reference: 

.. [#FTARM] Accurate Peptide Fragment Mass Analysis: Multiplexed Peptide Identification and Quantification. 10.1021/pr2008175

======================  =============================================================================================================================
Full name               FT-ARM
Home page               https://brucelab.gs.washington.edu/FT-ARM/index.html
Authors                 Chad R. Weisbrod et al.
Lab & Company           Bruce Lab
Publication date        2012 Jan.
Analysis strategies     Sequence-/Library-based search
======================  =============================================================================================================================

:Function: Sequence-/Library-based search

======================  =============================================================================================================================
Analysis approach       Spectrum-first
SSM score               Dot product
Used prior information  (optional) fragmentation pattern
======================  =============================================================================================================================


Spectronaut
^^^^^^^^^^^

back to table_

:Reference: 

.. [#Spectronaut] Extending the Limits of Quantitative Proteome Profiling with Data-Independent Acquisition and Application to Acetaminophen-Treated Three-Dimensional Liver Microtissues. 10.1074/mcp.M114.044305

Introduced PTM scoring in version 13:

.. [#Spectronaut2] Rapid and site-specific deep phosphoproteome profiling by data-independent acquisition without the need for spectral libraries. 10.1038/s41467-020-14609-1

======================  =============================================================================================================================
Full name               Spectronaut
Home page               https://biognosys.com/software/spectronaut
Programming language    C#
Authors                 Roland Bruderer et al.
Lab & Company           Biognosys AG
Release date            2013
Analysis strategies     Spectra reconstruction and sequence-based search on pseudo spectra; Library-based search
======================  =============================================================================================================================


OpenSWATH
^^^^^^^^^

back to table_

:Reference: 

.. [#OpenSWATH] OpenSWATH enables automated, targeted analysis of data-independent acquisition MS data. 10.1038/nbt.2841

======================  =============================================================================================================================
Full name               OpenSWATH
Home page               http://openswath.org
Source code             https://github.com/OpenMS/OpenMS
Programming language    C++ & Python
Authors                 Hannes L. Röst et al.
Lab & Company           Aebersold Lab & Röst Lab
Publication date        2014 Mar.
Analysis strategies     Library-based search
======================  =============================================================================================================================

:Function: Library-based search

======================  =============================================================================================================================
Analysis approach       Chromatogram-first
Minimum scoring unit    Peak group
Scoring model           (PyProphet) XGBoost
======================  =============================================================================================================================


DIANA
^^^^^

back to table_

:Reference: 

.. [#DIANA] DIANA-algorithmic improvements for analysis of data-independent acquisition MS data. 10.1093/bioinformatics/btu686

======================  =============================================================================================================================
Full name               DIANA
Home page               https://proteomics.immunoprot.lth.se
Programming language    Scala & Python
Authors                 Johan Teleman et al.
Lab & Company           Levander Lab
Publication date        2014 Oct.
Analysis strategies     Library-based search
======================  =============================================================================================================================

:Function: Library-based search

======================  =============================================================================================================================
Analysis approach       Chromatogram-first
Minimum scoring unit    Peak group
Scoring model           (PyProphet) XGBoost
======================  =============================================================================================================================


DIA-Umpire
^^^^^^^^^^

back to table_

:Reference: 

.. [#DIAUmpire] DIA-Umpire: comprehensive computational framework for data-independent acquisition proteomics. 10.1038/nmeth.3255
.. [#DIAUmpire2] Untargeted, spectral library-free analysis of data-independent acquisition proteomics data generated using Orbitrap mass spectrometers. 10.1002/pmic.201500526

======================  =============================================================================================================================
Full name               DIA-Umpire
Home page               https://diaumpire.nesvilab.org
Source code             https://github.com/Nesvilab/DIA-Umpire
Programming language    Java
Authors                 Chih-Chiang Tsou et al.
Lab & Company           Nesvizhskii Lab
Publication date        2015 Jan.
Analysis strategies     Spectra reconstruction; library-based search
======================  =============================================================================================================================

:Function: spectra reconstruction

======================  =============================================================================================================================
Pre-processing          Interpolation and unimodal peak splitting
Ion grouping criteria   1. summed mass of two fragments equals to precursor mass; 2. precursor-fragment PCC rank and apex RT
Fragment assignment     One-to-multi
======================  =============================================================================================================================


SWATHProphet
^^^^^^^^^^^^

back to table_

:Reference: 

.. [#SWATHProphet] Automated Validation of Results and Removal of Fragment Ion Interferences in Targeted Analysis of Data-independent Acquisition Mass Spectrometry (MS) using SWATHProphet. 10.1074/mcp.O114.044917

======================  =============================================================================================================================
Full name               SWATHProphet
Home page               http://tools.proteomecenter.org/wiki/index.php?title=Software:SWATHProphet
Source code             https://sourceforge.net/projects/sashimi/files/
Programming language    Perl
Authors                 Andrew Keller et al.
Lab & Company           Moritz Lab
Publication date        2015 Feb.
Analysis strategies     Library-based search
======================  =============================================================================================================================

:Function: Library-based search

======================  =============================================================================================================================
Analysis approach       Chromatogram-first
Minimum scoring unit    Peak group
Scoring model           mProphet-like linear classifier
======================  =============================================================================================================================


Group-DIA
^^^^^^^^^

back to table_

:Reference: 

.. [#GroupDIA] Group-DIA: analyzing multiple data-independent acquisition mass spectrometry data files. 10.1038/nmeth.3593

======================  =============================================================================================================================
Full name               Group-DIA
Home page               http://yuanyueli.github.io/group-dia/
Source code             https://github.com/YuanyueLi/group-dia
Programming language    C++
Authors                 Yuanyue Li et al.
Lab & Company           Han Lab
Publication date        2015 Oct.
Analysis strategies     Spectra reconstruction; library-based search
======================  =============================================================================================================================

:Function: spectra reconstruction

======================  =============================================================================================================================
Pre-processing          Cross-run spectra alignment
Ion grouping criteria   k-means-based precursor-fragment clustering
Fragment assignment     One-to-one and high precursor-fragment correlation-first
======================  =============================================================================================================================


MSPLIT-DIA
^^^^^^^^^^

back to table_

:Reference: 

.. [#MSPLITDIA] MSPLIT-DIA: sensitive peptide identification for data-independent acquisition. 10.1038/nmeth.3655

======================  =============================================================================================================================
Full name               MSPLIT-DIA
Home page               http://proteomics.ucsd.edu/software-tools/msplit-dia
Source code             /
Programming language    Java
Authors                 Jian Wang et al.
Lab & Company           Bandeira Lab
Publication date        2015 Nov.
Analysis strategies     Library-based search
======================  =============================================================================================================================

:Function: Library-based search

==========================  =============================================================================================================================
Analysis approach           Spectrum-first
SSM score                   Cosine similarity
Used prior information      Fragmentation pattern; (optional) RT
Peak-picking of shared m/z  High quality-first by SSM similarity
==========================  =============================================================================================================================


PECAN (Walnut)
^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#PECAN] PECAN: library-free peptide detection for data-independent acquisition tandem mass spectrometry data. 10.1038/nmeth.4390

======================  =============================================================================================================================
Full name               PECAN (Walnut in Encyclopedia platform)
Home page               Walnut: https://bitbucket.org/searleb/encyclopedia/wiki/Home; PECAN: https://bitbucket.org/maccosslab/pecan/wiki/Home
Source code             Walnut: https://bitbucket.org/searleb/encyclopedia/src; PECAN: https://bitbucket.org/maccosslab/pecan/src
Programming language    Walnut: Java; PECAN: Python
Authors                 Ying S. Ting et al. (re-implemented by Brian C. Searle in Encyclopedia platform)
Lab & Company           MacCoss Lab
Publication date        2017 Aug.
Analysis strategies     Sequence-based search
======================  =============================================================================================================================

:Function: Sequence-based search

======================  =============================================================================================================================
Analysis approach       Spectrum-first
SSM score               Background score-subtracted dot product
Matching restriction    Reduce fragment matching importance based on frequency
======================  =============================================================================================================================


Specter
^^^^^^^

back to table_

:Reference: 

.. [#Specter] Specter: linear deconvolution for targeted analysis of data-independent acquisition mass spectrometry proteomics. 10.1038/nmeth.4643

======================  =============================================================================================================================
Full name               Specter
Home page               https://github.com/rpeckner-broad/Specter
Source code             https://github.com/rpeckner-broad/Specter
Programming language    Python
Authors                 Ryan Peckner et al.
Lab & Company           Jaffe Lab
Publication date        2018 Apr.
Analysis strategies     Library-based search
======================  =============================================================================================================================

:Function: Library-based search

======================  =============================================================================================================================
Analysis approach       Spectrum-first
SSM score               Coefficients of linear combination of library spectra
Used prior information  Fragmentation pattern; RT
======================  =============================================================================================================================


EncyclopeDIA
^^^^^^^^^^^^

back to table_

:Reference: 

.. [#EncyclopeDIA] Chromatogram libraries improve peptide detection and quantification by data independent acquisition mass spectrometry. 10.1038/s41467-018-07454-w
.. [#EncyclopeDIA2] Generating high quality libraries for DIA MS with empirically corrected peptide predictions. 10.1038/s41467-020-15346-1

======================  =============================================================================================================================
Full name               EncyclopeDIA
Home page               https://bitbucket.org/searleb/encyclopedia/wiki/Home
Source code             https://bitbucket.org/searleb/encyclopedia/src
Programming language    Java
Authors                 Brian C. Searle et al.
Lab & Company           MacCoss Lab & Searle Lab
Publication date        2018 Dec.
Analysis strategies     Library-based search
======================  =============================================================================================================================

:Function: Library-based search

======================  =============================================================================================================================
Analysis approach       Spectrum-first
SSM score               product of summed correlation-weighted dot products and the factorial of the number of matched ions
Used prior information  Fragmentation pattern; RT
======================  =============================================================================================================================


DeepNovo-DIA
^^^^^^^^^^^^

back to table_

:Reference: 

.. [#DeepNovoDIA] Deep learning enables de novo peptide sequencing from data-independent-acquisition mass spectrometry. 10.1038/s41592-018-0260-3

======================  =============================================================================================================================
Full name               DeepNovo-DIA
Home page               https://github.com/nh2tran/DeepNovo-DIA
Source code             https://github.com/nh2tran/DeepNovo-DIA
Programming language    Python
Authors                 Ngoc Hieu Tran et al.
Lab & Company           Li Lab
Publication date        2018 Dec.
Analysis strategies     De novo sequencing
======================  =============================================================================================================================


PEAKS
^^^^^

back to table_

:Reference: 

.. [#PEAKS] PEAKS: powerful software for peptide de novo sequencing by tandem mass spectrometry. 10.1002/rcm.1196
.. [#PEAKS2] A streamlined platform for analyzing tera-scale DDA and DIA mass spectrometry data enables highly sensitive immunopeptidomics. 10.1038/s41467-022-30867-7

======================  =============================================================================================================================
Full name               PEAKS
Home page               https://www.bioinfor.com/peaks-software
Authors                 Bin Ma et al.
Lab & Company           Bioinformatics Solutions Inc
Support date            2018
Analysis strategies     Sequence-based search; library-based search; de novo sequencing
======================  =============================================================================================================================


DIA-NN
^^^^^^

back to table_

:Reference: 

Original:

.. [#DIANN] DIA-NN: neural networks and interference correction enable deep proteome coverage in high throughput. 2020. 10.1038/s41592-019-0638-x

Introduced new analysis strategies for identification, scoring, and quantification of Scanning SWATH data:

.. [#DIANN2] Ultra-fast proteomics with Scanning SWATH. 2021. 10.1038/s41587-021-00860-4

Introduced the PTM scoring function with ubiquitinome DIA data as examples:

.. [#DIANN3] Time-resolved in vivo ubiquitinome profiling by DIA-MS reveals USP7 targets on a proteome-wide scale. 2021. 10.1038/s41467-021-25454-1

Introduced the integration of DIA-NN with FragPipe platform, and the analysis details for diaPASEF data:

.. [#DIANN4] dia-PASEF data analysis using FragPipe and DIA-NN for deep proteomics of low sample amounts. 2022. 10.1038/s41467-022-31492-0

Introduced new analysis strategies for identification, scoring, and quantification of plexDIA data (non-isobaric label):

.. [#DIANN5] Increasing the throughput of sensitive proteomics by plexDIA. 2023. 10.1038/s41587-022-01389-w

Introduced QuantUMS for improved quantification:

.. [#DIANN6] QuantUMS: uncertainty minimisation enables confident quantification in proteomics. 2023. 10.1101/2023.06.20.545604

======================  =============================================================================================================================
Full name               DIA-NN
Home page               https://github.com/vdemichev/diann
Source code             https://github.com/vdemichev/diann
Programming language    C++
Authors                 Vadim Demichev et al.
Lab & Company           Ralser Lab & Demichev Lab
Publication date        2019 Nov.
Analysis strategies     Library-based search
======================  =============================================================================================================================

:Function: Library-based search

======================  =============================================================================================================================
Analysis approach       Chromatogram-first
Minimum scoring unit    One best peak
Scoring model           linear classifier and fully-connected neural network
======================  =============================================================================================================================


DIA tensor
^^^^^^^^^^

back to table_

:Reference: 

.. [#DIAT] Phenotype Classification using Proteome Data in a Data-Independent Acquisition Tensor Format. 2020. 10.1021/jasms.0c00254

======================  =============================================================================================================================
Full name               DIA tensor
Home page               https://github.com/guomics-lab/DIAtensor
Source code             https://github.com/guomics-lab/DIAtensor
Programming language    Python
Authors                 Fangfei Zhang et al.
Lab & Company           Guo Lab
Publication date        2020 Oct.
Analysis strategies     Sequencing-independent
======================  =============================================================================================================================


MaxDIA
^^^^^^^^

back to table_

:Reference: 

.. [#MaxDIA] MaxDIA enables library-based and library-free data-independent acquisition proteomics. 2021. 10.1038/s41587-021-00968-7

======================  =============================================================================================================================
Full name               MaxDIA
Home page               https://maxquant.org/
Programming language    C#
Authors                 Pavel Sinitcyn et al.
Lab & Company           Cox Lab
Publication date        2021 July
Analysis strategies     Library-based search
======================  =============================================================================================================================

:Function: Library-based search

======================  =============================================================================================================================
Analysis approach       Chromatogram-first
Minimum scoring unit    Peak group
Scoring model           XGBoost
======================  =============================================================================================================================


DIAmeter
^^^^^^^^

back to table_

:Reference: 

.. [#DIAmeter] DIAmeter: matching peptides to data-independent acquisition mass spectrometry data. 2021. 10.1093/bioinformatics/btab284

======================  =============================================================================================================================
Full name               DIAmeter
Home page               http://crux.ms/
Source code             https://github.com/crux-toolkit/crux-toolkit
Programming language    C++
Authors                 Yang Young Lu et al.
Lab & Company           Noble Lab
Publication date        2021 July
Analysis strategies     Sequence-based search
======================  =============================================================================================================================

:Function: Sequence-based search

======================  =============================================================================================================================================
Analysis approach       Spectrum-first
SSM score               XCorr
Matching restriction    1. Maximum PSMs per charge state per spectrum; 2. PSM reduction based on combined sub-scores compared to PSM with highest primary score
======================  =============================================================================================================================================


FIGS
^^^^

back to table_

:Reference: 

.. [#FIGS] FIGS: Featured Ion-Guided Stoichiometry for Data-Independent Proteomics through Dynamic Deconvolution. 10.1021/acs.jproteome.1c00438

======================  =============================================================================================================================
Full name               FIGS
Home page               https://github.com/FangYan-USTC/FIGS
Source code             https://github.com/FangYan-USTC/FIGS
Programming language    Python
Authors                 Yan Fang et al.
Lab & Company           Zeng Lab
Publication date        2021 July
Analysis strategies     Library-based search
======================  =============================================================================================================================

:Function: Library-based search

======================  =============================================================================================================================
Analysis approach       Spectrum-first
SSM score               Coefficients of linear combination of library spectra
Used prior information  Fragmentation pattern; RT
======================  =============================================================================================================================


mstc
^^^^

back to table_

:Reference: 

.. [#mstc] On the feasibility of deep learning applications using raw mass spectrometry data. 2021. 10.1093/bioinformatics/btab311

======================  =============================================================================================================================
Full name               mass_spec_trans_coding
Home page               https://github.com/PhosphorylatedRabbits/mass_spec_trans_coding
Source code             https://github.com/PhosphorylatedRabbits/mass_spec_trans_coding
Programming language    Python
Authors                 Joris Cadow et al.
Lab & Company           Martínez Lab
Publication date        2021 July
Analysis strategies     Sequencing-independent
======================  =============================================================================================================================


CsoDIAq
^^^^^^^

back to table_

:Reference: 

.. [#CsoDIAq] CsoDIAq Software for Direct Infusion Shotgun Proteome Analysis. 10.1021/acs.analchem.1c02021

======================  =============================================================================================================================
Full name               CsoDIAq
Home page               https://github.com/CCranney/CsoDIAq
Source code             https://github.com/CCranney/CsoDIAq
Programming language    Python
Authors                 Caleb W. Cranney and Jesse G. Meyer
Lab & Company           Meyer Lab
Publication date        2021 Sep.
Analysis strategies     Library-based search
======================  =============================================================================================================================

:Function: Library-based search

======================  =============================================================================================================================
Analysis approach       Spectrum-first
SSM score               Cosine similarity
Used prior information  Fragmentation pattern
======================  =============================================================================================================================


DreamDIA\ :sup:`XMBD`
^^^^^^^^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#DreamDIAXMBD] Deep representation features from DreamDIA\ :sup:`XMBD` improve the analysis of data-independent acquisition proteomics. 2021. 10.1038/s42003-021-02726-6

======================  =============================================================================================================================
Full name               DreamDIA\ :sup:`XMBD`
Home page               https://github.com/xmuyulab/DreamDIA-XMBD
Source code             https://github.com/xmuyulab/DreamDIA-XMBD
Programming language    Python
Authors                 Mingxuan Gao et al.
Lab & Company           Han Lab & Yu Lab
Publication date        2021 Oct.
Analysis strategies     Library-based search
======================  =============================================================================================================================

:Function: Library-based search

======================  =============================================================================================================================
Analysis approach       Chromatogram-first
Minimum scoring unit    Raw XICs
Scoring model           LSTM neural network and XGBoost
======================  =============================================================================================================================


Dear-DIA\ :sup:`XMBD`
^^^^^^^^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#DearDIAXMBD] Dear-DIA\ :sup:`XMBD`: Deep Autoencoder Enables Deconvolution of Data-Independent Acquisition Proteomics. 2023. 10.34133/research.0179

======================  =============================================================================================================================
Full name               Dear-DIA\ :sup:`XMBD`
Home page               https://github.com/jianweishuai/Dear-DIA-XMBD
Source code             /
Programming language    C++
Authors                 Qingzu He et al.
Lab & Company           Jianwei Shuai Lab & Jiahuai Han Lab
Publication date        2023 June
Analysis strategies     Spectra reconstruction
======================  =============================================================================================================================

:Function: spectra reconstruction

======================  =============================================================================================================================
Pre-processing          Latent representation extraction of fragment XICs via a VAE model
Ion grouping criteria   k-means-based fragment representation clustering and CNN calculated fragment peak group similarity
Fragment assignment     One-to-One
======================  =============================================================================================================================


MSFragger-DIA
^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#MSFraggerDIA] Analysis of DIA proteomics data using MSFragger-DIA and FragPipe computational platform. 2023. 10.1038/s41467-023-39869-5

======================  =============================================================================================================================
Full name               MSFragger-DIA
Home page               https://msfragger.nesvilab.org & https://github.com/Nesvilab/MSFragger
Programming language    Java
Authors                 Fengchao Yu et al.
Lab & Company           Nesvizhskii Lab
Publication date        2023 July (function available in 2020)
Analysis strategies     Sequence-based search
======================  =============================================================================================================================

:Function: Sequence-based search

======================  =============================================================================================================================================
Analysis approach       Spectrum-first
SSM score               MSFragger hyperscore
Matching restriction    1. Maximum PSMs per spectrum; 2. High PSM score-first signal picking
======================  =============================================================================================================================================
