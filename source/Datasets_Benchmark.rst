Benchmark data sets
===================


Summary table
-------------

.. _table:

========  =========================  ========  ================  ====================================  ==============================  ====================
Year      Ref.                       No.       Short desc.       Target                                Background                      Instrument
========  =========================  ========  ================  ====================================  ==============================  ====================
2014      [#14OpenSWATH]_            1         SGS               422 SIS peptides                      None / yeast / HeLa             TTOF 5600
2015      [#15DIAUmpire]_            1         UPS1              UPS1                                  None                            TTOF 5600
..                                   2         UPS2              UPS2                                  None                            TTOF 5600
..                                   3         UPS2 spike        UPS2                                  Tryptic E. coli                 TTOF 5600
2016      [#16LFQBench]_             1         HYE124            Tryptic yeast+ecoli                   Tryptic HeLa                    TTOF 5600+/6600
..                                   2         HYE110            Tryptic yeast+ecoli                   Tryptic HeLa                    TTOF 6600
2017      [#17IPF]_                  1         SynHeavyPhos      579 SIS phosphopeptides               Tryptic HEK293                  TTOF 5600+
2017      [#17HYEC]_                 1         HYEC              Tryptic yeast+ecoli+celegans          Tryptic HeLa                    QE HF
2018      [#18Specter]_              1         SynPhos96         96 NS phosphopeptides                 Tryptic HEK293                  QE HF Plus
2020      [#20dDIAPTM]_              1         MixPhos           Yeast phosphoproteome                 HeLa phosphoproteome            QE HF-X
..                                   2         SynPhos200+       200+ NS phosphopeptides               Yeast phosphoproteome           QE HF-X
..                                   3         Phos-stoich       Partial-dephos yeast phosproteome     HeLa phosphoproteome            QE HF-X
2020      [#20diaPASEF]_             1         HY13 diaPASEF     Tryptic yeast                         Tryptic HeLa                    timsTOF Pro
2021      [#21MaxDIA]_               1         HYE124 diaPASEF   Tryptic yeast+ecoli                   Tryptic HeLa                    timsTOF Pro
2021      [#21DIAGPS]_               1         SynPhos166        166 NS phosphopeptides                Tryptic yeast                   Fusion Lumos
2021      [#21UPS1MultiAcqui]_       1         UPS1 spike        UPS1                                  Tryptic E. coli                 Orbitrap Fusion
2022      [#22MultiHYE]_             1         HYE124            Tryptic yeast+ecoli                   Tryptic K562                    TTOF 5600
..                                   2                                                                                                 TTOF 6600+
..                                   3                                                                                                 Synapt G2-Si
..                                   4                                                                                                 QE HF-X
..                                   5                                                                                                 Synapt XS
..                                   6                                                                                                 timsTOF Pro
2022      [#22PlexDIA]_              1         HYE plexDIA       Tryptic yeast+ecoli                   Tryptic U-937 or Jurkat         QE
2022      [#22Zeno]_                 1         HY12 Zeno         Tryptic yeast                         Tryptic K562                    ZenoTOF 7600
2022      [#22HEBench]_              1         HE 4cond          Tryptic E. coli                       Tryptic human lymph nodes       Orbitrap Eclipse
2023      [#23MYBench]_              1         MY 7cond          Tryptic mouse brain membrane          Tryptic yeast                   QE HF/timsTOF Pro
2023      [#23Immuno]_               1         B57               HLA-B*57:01                           Tryptic HeLa                    Orbitrap Fusion
========  =========================  ========  ================  ====================================  ==============================  ====================

.. note::
   - *Target*
      - SIS: stable isotope-labeled standard (synthetic peptides in all cases)
      - NS: non-labeled standard (synthetic peptides in all cases)


Individuals
-----------

|


OpenSWATH SGS
^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#14OpenSWATH] OpenSWATH enables automated, targeted analysis of data-independent acquisition MS data. 10.1038/nbt.2841

:Authors: Röst et al.
:Year: 2014

:Dataset 1:

======================  =============================================================================================================================
Short name              SWATH-MS Gold Standard (SGS)
Repository ID           PASS00289
MS instrument           TTOF 5600
Acquisition method      25 m/z wide-window SWATH
Target sample           422 SIS peptides
Background sample       Water / yeast BY4741 tryptic digest / HeLa tryptic digest
PTM                     /
Other sample            Biognosys iRT peptides (C18)
Brief design            Pure SIS / SIS + yeast background / SIS + human background. SIS concentration in each sample from 1x to 512x. 3 replicates.
Additional runs         DDA runs for pure SIS peptides
======================  =============================================================================================================================


DIA-Umpire UPS
^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#15DIAUmpire] DIA-Umpire: comprehensive computational framework for data-independent acquisition proteomics. 10.1038/nmeth.3255

:Authors: Tsou et al.
:Year: 2015

:Dataset 1:

======================  =============================================================================================================================
Short name              UPS1
Repository ID           PXD001587
MS instrument           TTOF 5600
Acquisition method      25 m/z wide-window SWATH (long MS1 ion accumulation (250 ms) or not (50 ms))
Target sample           UPS1
Background sample       /
PTM                     /
Other sample            /
Brief design            Pure UPS1. 3 replicates.
Additional runs         /
======================  =============================================================================================================================

:Dataset 2:

======================  =============================================================================================================================
Short name              UPS2
Repository ID           PXD001587
MS instrument           TTOF 5600
Acquisition method      25 m/z wide-window SWATH (long MS1 ion accumulation (250 ms))
Target sample           UPS2
Background sample       /
PTM                     /
Other sample            /
Brief design            Pure UPS2. 3 replicates.
Additional runs         DDA runs for pure UPS2
======================  =============================================================================================================================

:Dataset 3:

======================  =============================================================================================================================
Short name              UPS2 spike-in
Repository ID           PXD001587
MS instrument           TTOF 5600
Acquisition method      25 m/z wide-window SWATH (long MS1 ion accumulation (250 ms) or not (50 ms))
Target sample           UPS2
Background sample       E. coli tryptic digest
PTM                     /
Other sample            /
Brief design            UPS2 + E. coli background. 3 replicates.
Additional runs         /
======================  =============================================================================================================================


LFQBench
^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#16LFQBench] A multicenter study benchmarks software tools for label-free proteome quantification. 10.1038/nbt.3685

:Authors: Navarro et al.
:Year: 2016

:Dataset 1:

======================  =============================================================================================================================
Short name              HYE124
Repository ID           PXD002952
MS instrument           TTOF 5600+ / TTOF 6600
Acquisition method      25 m/z wide-window SWATH / 64 variable wide-window SWATH
Target sample           Tryptic digests of yeast / E. coli
Background sample       HeLa tryptic digest
PTM                     /
Other sample            Biognosys iRT peptides (C18)
Brief design            A: HYE 65/30/5; B: HYE 65/15/20. 3 replicates for each sample.
Additional runs         H/Y/E each has 3 DDA runs.
======================  =============================================================================================================================

:Dataset 2:

======================  =============================================================================================================================
Short name              HYE110
Repository ID           PXD002952
MS instrument           TTOF 6600
Acquisition method      25 m/z wide-window SWATH / 12.5 m/z wide-window SWATH / 32 variable wide-window SWATH / 64 variable wide-window SWATH
Target sample           Tryptic digests of yeast / E. coli
Background sample       HeLa tryptic digest
PTM                     /
Other sample            Biognosys iRT peptides (C18)
Brief design            A: HYE 67/30/3; B: HYE 67/3/30. 3 replicates for each sample.
Additional runs         /
======================  =============================================================================================================================


IPF SIS phosphopeptides
^^^^^^^^^^^^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#17IPF] Inference and quantification of peptidoforms in large sample cohorts by SWATH-MS. 10.1038/nbt.3908

:Authors: Rosenberger et al.
:Year: 2017

:Dataset 1:

======================  =============================================================================================================================
Short name              SynHeavyPhos
Repository ID           PXD004573
MS instrument           TTOF 5600+
Acquisition method      64 variable wide-window SWATH
Target sample           579 synthetic SIS phosphopeptides
Background sample       HEK293 tryptic digest
PTM                     Phosphorylation
Other sample            Biognosys iRT peptides (C18)
Brief design            Synthetic + HEK293 background. Total 13 dilution ratios 1:0, 1:1, …, 1:127. Single injection without replicate.
Additional runs         DDA runs for pure synthetic phosphopeptides. 3 replicates.
======================  =============================================================================================================================


HYEC
^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#17HYEC] Optimization of Experimental Parameters in Data-Independent Mass Spectrometry Significantly Increases Depth and Reproducibility of Results. 10.1074/mcp.RA117.000314

:Authors: Bruderer et al.
:Year: 2017

:Dataset 1:

======================  =====================================================================================================================================================================
Short name              HYEC
Repository ID           PXD005573
MS instrument           QE HF
Acquisition method      Variable wide-window DIA
Target sample           Tryptic digests of Yeast / E. coli / C. Elegans
Background sample       HeLa tryptic digest
PTM                     /
Other sample            Biognosys iRT peptides (C18)
Brief design            1\) Small fold change sample set: H 1:1; Y 1:1.2; E 1.3:1; C 1:1.1. 2) Large fold change sample set: H 1:1; Y 1.6:1; E 1:4; C 1:2. Each sample has 3 replicates.
Additional runs         A DDA library in Spectronaut .kit format is available.
======================  =====================================================================================================================================================================


Specter synthetic phospho
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#18Specter] Specter: linear deconvolution for targeted analysis of data-independent acquisition mass spectrometry proteomics. 10.1038/nmeth.4643

:Authors: Peckner et al.
:Year: 2018

:Dataset 1:

======================  =============================================================================================================================
Short name              SynPhos
Repository ID           PXD006722
MS instrument           QE HF Plus
Acquisition method      56 x 22 m/z inter-cycle overlapping-window DIA (11 m/z shift)
Target sample           96 NS phosphopeptides
Background sample       HEK293 tryptic digest
PTM                     Phosphorylation
Other sample            /
Brief design            NS phosphopeptides + HEK293 background. Total 5 samples with synthetic concentrations from 1x to 16x. 3 replicates.
Additional runs         DDA runs of all five spiked-in samples with 1 injection
======================  =============================================================================================================================


HY phospho / synthetic phospho / Phospho-stoichiometry
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#20dDIAPTM] Rapid and site-specific deep phosphoproteome profiling by data-independent acquisition without the need for spectral libraries. 10.1038/s41467-020-14609-1

:Authors: Bekker-Jensen et al.
:Year: 2020

:Dataset 1:

======================  ===================================================================================================================================================================================================
Short name              Mixed phosphoproteome
Repository ID           PXD014525
MS instrument           QE HF-X
Acquisition method      14 m/z wide-window DIA
Target sample           Ti-IMAC enriched yeast tryptic digest
Background sample       Ti-IMAC enriched HeLa tryptic digest
PTM                     Phosphorylation
Other sample            Biognosys iRT peptides (C18)
Brief design            Tryptic digests of yeast BY4742 and HeLa are mixed in 5 ratios of 0.25:1, 0.5:1, 1:1, 1.5:1, and 2:1, and mixed samples are Ti-IMAC enriched. Each sample has 6 replicates.
Additional runs         In addition to 3 yeast only and 3 HeLa only DIA runs, all DIA runs have their corresponding DDA runs with same injection numbers.
======================  ===================================================================================================================================================================================================

:Dataset 2:

======================  ============================================================================================================================================================================================================================================================================================================================================================================================
Short name              SynPhos200p
Repository ID           PXD014525
MS instrument           QE HF-X
Acquisition method      14 m/z wide-window DIA
Target sample           Multi-source NS phosphopeptides
Background sample       Ti-IMAC enriched yeast tryptic digest
PTM                     Phosphorylation
Other sample            Biognosys iRT peptides (C18)
Brief design            Five sources of synthetic phosphopeptides: JPT (SpikeMix PTM-kit 52 1001098; SpikeMix PTM-kit 54 1001100) and Sigma-Aldrich (MS PhosphoMix 1 Light MSP1L, MS PhosphoMix 2 Light MSP2L, MS PhosphoMix 3 Light MSP3L). All phosphopeptides are mixed and spiked into yeast phosphoproteome in 4 dilution concentrations: 1x, 10x, 100x, and 1000x. Each sample has 3 replicates.
Additional runs         All DIA runs have their corresponding DDA runs with same injection numbers.
======================  ============================================================================================================================================================================================================================================================================================================================================================================================

:Dataset 3:

======================  ===============================================================================================================================================================================================================================================================================================================================================
Short name              Phospho-stoichiometry
Repository ID           PXD014525
MS instrument           QE HF-X
Acquisition method      14 m/z wide-window DIA
Target sample           Ti-IMAC enriched yeast tryptic digest with or without phosphatase treatment
Background sample       Ti-IMAC enriched HeLa tryptic digest
PTM                     Phosphorylation
Other sample            Biognosys iRT peptides (C18)
Brief design            After yeast tryptic digest was Ti-IMAC enriched, half was phosphatase treated while another half was mock treated. Two treated samples are mixed and spiked into HeLa tryptic phosphoproteome background, and formed expected phosphorylation stoichiometry of 1%, 10%, 50%, 90%, and 99%. Each final sample has 5 replicates.
Additional runs         All DIA runs have their corresponding DDA runs with same injection numbers.
======================  ===============================================================================================================================================================================================================================================================================================================================================


HY13 diaPASEF
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#20diaPASEF] diaPASEF: parallel accumulation-serial fragmentation combined with data-independent acquisition. 10.1038/s41592-020-00998-0

:Authors: Meier et al.
:Year: 2020

:Dataset 1:

======================  =============================================================================================================================
Short name              HY13 diaPASEF
Repository ID           PXD017703 (ftp://ftp.pride.ebi.ac.uk/pride/data/archive/2020/12/PXD017703)
MS instrument           timsTOF Pro
Acquisition method      diaPASEF 16 scans
Target sample           Yeast tryptic digest
Background sample       HeLa tryptic digest
PTM                     /
Other sample            /
Brief design            A: H/Y 200/45; B: H/Y 200/15. 3 replicates
Additional runs         Fractionated yeast and HeLa samples are analyzed by ddaPASEF.
======================  =============================================================================================================================


HYE124 diaPASEF
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#21MaxDIA] MaxDIA enables library-based and library-free data-independent acquisition proteomics. 10.1038/s41587-021-00968-7

:Authors: Sinitcyn et al.
:Year: 2021

:Dataset 1:

======================  ===========================================================================================================================================================================================================
Short name              HYE124 timsTOF
Repository ID           PXD022589
MS instrument           timsTOF Pro
Acquisition method      diaPASEF 16 scans
Target sample           Tryptic digests of Yeast / E. coli
Background sample       HeLa tryptic digest
PTM                     /
Other sample            Biognosys iRT peptides (C18)
Brief design            A: HYE 65/30/5; B: HYE 65/15/20. Triplicate injections for each sample.
Additional runs         ddaPASEF runs for three species individually. Sample of each species are off-line fractionated to 5 fractions, and two injections are performed for each fraction. Stored in PXD022582.
======================  ===========================================================================================================================================================================================================


DIA-GPS 166 NS phosphopeptides
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#21DIAGPS] A data-independent acquisition-based global phosphoproteomics system enables deep profiling. 10.1038/s41467-021-22759-z

:Authors: Kitata et al.
:Year: 2021

:Dataset 1:

======================  =================================================================================================================================================================
Short name              SynPhos166
Repository ID           PXD019797
MS instrument           Fusion Lumos
Acquisition method      10 m/z wide-window DIA
Target sample           166 NS phosphopeptides
Background sample       Yeast tryptic digest
PTM                     Phosphorylation
Other sample            Biognosys iRT peptides (C18)
Brief design            NS phosphopeptides + yeast background. Total 5 samples with synthetic phosphopeptide concentrations from 1x to 20x. 3 replicates.
Additional runs         3 DDA runs and 3 DIA runs of pure synthetic phosphopeptides.
======================  =================================================================================================================================================================


UPS1 Orbi multiple acquisition methods
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#21UPS1MultiAcqui] Extensive and Accurate Benchmarking of DIA Acquisition Methods and Software Tools Using a Complex Proteomic Standard. 10.1021/acs.jproteome.1c00490

:Authors: Gotti et al.
:Year: 2021

:Dataset 1:

======================  =====================================================================================================================================================================================
Short name              UPS1 spike-in
Repository ID           PXD026600
MS instrument           Orbitrap Fusion
Acquisition method      8 m/z wide-window / 15 m/z wide-window / 8 m/z inter-cycle overlapping window (4 m/z shift) / 8 m/z and 15 m/z variable wide-window
Target sample           UPS1
Background sample       E. coli tryptic digest
PTM                     /
Other sample            Biognosys iRT peptides (C18)
Brief design            UPS1 + E. coli background. Total 8 samples with UPS1 concentrations from 1x to 500x. 3 replicates.
Additional runs         48 DDA runs for 48 fractionated E. coli samples and 1 DDA run for UPS1+E. coli sample
======================  =====================================================================================================================================================================================


HYE124 multiple instruments and acquisition methods
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#22MultiHYE] A comprehensive LFQ benchmark dataset on modern day acquisition strategies in proteomics. 10.1038/s41597-022-01216-6

:Authors: Van Puyvelde et al.
:Year: 2022

:Dataset 1:

======================  =================================================================================================================================================================
Short name              HYE124-5600
Repository ID           PXD028735
MS instrument           TTOF 5600
Acquisition method      64 variable wide-window SWATH
Target sample           Tryptic digests of Yeast / E. coli
Background sample       Human K562 tryptic digest
PTM                     /
Other sample            Biognosys iRT peptides (C18)
Brief design            A: HYE 65/30/5; B: HYE 65/15/20. 
Additional runs         1\) 3 DDA runs for each species, resulted in total 9 runs. 2\) 8 narrow-window DIA injections with 2 m/z window size.
======================  =================================================================================================================================================================

:Dataset 2:

======================  =================================================================================================================================================================
Short name              HYE124-6600
Repository ID           PXD028735
MS instrument           TTOF 6600+
Acquisition method      1\) 99 variable windowed SWATH. 2) Scanning SWATH 5 m/z window (1 m/z Q1 bin).
Target sample           Tryptic digests of Yeast / E. coli
Background sample       Human K562 tryptic digest
PTM                     /
Other sample            Biognosys iRT peptides (C18)
Brief design            A: HYE 65/30/5; B: HYE 65/15/20. 
Additional runs         1\) 3 DDA runs for each species, resulted in total 9 runs. 2\) 8 narrow-window scanning SWATH injections with 1 m/z window size (0.2 m/z Q1 bin).
======================  =================================================================================================================================================================

:Dataset 3:

======================  =================================================================================================================================================================
Short name              HYE124-G2Si
Repository ID           PXD028735
MS instrument           Synapt G2-Si
Acquisition method      UDMS\ :sup:`E`
Target sample           Tryptic digests of Yeast / E. coli
Background sample       Human K562 tryptic digest
PTM                     /
Other sample            Biognosys iRT peptides (C18)
Brief design            A: HYE 65/30/5; B: HYE 65/15/20. 
Additional runs         3 DDA runs for each species, resulted in total 9 runs.
======================  =================================================================================================================================================================

:Dataset 4:

======================  =================================================================================================================================================================
Short name              HYE124-HFX
Repository ID           PXD028735
MS instrument           QE HF-X
Acquisition method      8 m/z inter-cycle overlapping-window DIA (4 m/z shift)
Target sample           Tryptic digests of Yeast / E. coli
Background sample       Human K562 tryptic digest
PTM                     /
Other sample            Biognosys iRT peptides (C18)
Brief design            A: HYE 65/30/5; B: HYE 65/15/20. 
Additional runs         1\) 3 DDA runs for each species, resulted in total 9 runs. 2\) 8 narrow-window DIA injections with 4 m/z inter-cycle overlapping windows (2 m/z shift).
======================  =================================================================================================================================================================

:Dataset 5:

======================  =================================================================================================================================================================
Short name              HYE124-XS
Repository ID           PXD028735
MS instrument           Synapt XS
Acquisition method      SONAR
Target sample           Tryptic digests of Yeast / E. coli
Background sample       Human K562 tryptic digest
PTM                     /
Other sample            Biognosys iRT peptides (C18)
Brief design            A: HYE 65/30/5; B: HYE 65/15/20. 
Additional runs         1\) 3 DDA runs for each species, resulted in total 9 runs. 2\) 8 narrow-window SONAR injections.
======================  =================================================================================================================================================================


:Dataset 6:

======================  =================================================================================================================================================================
Short name              HYE124-timsTOF
Repository ID           PXD028735
MS instrument           timsTOF Pro
Acquisition method      diaPASEF 16 scans
Target sample           Tryptic digests of Yeast / E. coli
Background sample       Human K562 tryptic digest
PTM                     /
Other sample            Biognosys iRT peptides (C18)
Brief design            A: HYE 65/30/5; B: HYE 65/15/20. 
Additional runs         3 ddaPASEF runs for each species, resulted in total 9 runs.
======================  =================================================================================================================================================================


HYE plexDIA
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#22PlexDIA] Increasing the throughput of sensitive proteomics by plexDIA. 10.1038/s41587-022-01389-w

:Authors: Derks et al.
:Year: 2022

:Dataset 1:

======================  ==============================================================================================================================================================
Short name              plexDIA HYE124/063/066
Repository ID           PXD029531 (ftp://massive.ucsd.edu/v01/MSV000089093)
MS instrument           QE
Acquisition method      5 MS1-inserted 25 variable wide-window DIA / 40 variable wide-window DIA
Target sample           Tryptic digests of Yeast / E. coli
Background sample       Human tryptic digest (U-937 or Jurkat)
PTM                     /
Other sample            /
Brief design            A: non-labeled E. coli 20%, yeast 15%, U-937 65%; B: mTRAQ4 E. coli 5%, yeast 30%, U-937 65%; C: mTRAQ8 E. coli 30%, yeast 5%, Jurkat 65%
Additional runs         All DIA runs have their corresponding DDA runs with same injection numbers.
======================  ==============================================================================================================================================================


HY12 Zeno SWATH
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#22Zeno] High-throughput proteomics of nanogram-scale samples with Zeno SWATH MS. 10.7554/eLife.83947

:Authors: Wang et al.
:Year: 2022

:Dataset 1:

======================  =============================================================================================================================
Short name              HY12 Zeno SWATH
Repository ID           PXD036786 (ftp://ftp.pride.ebi.ac.uk/pride/data/archive/2022/12/PXD036786)
MS instrument           ZenoTOF 7600
Acquisition method      85 variable windowed DIA (6-10 m/z window size)
Target sample           Yeast tryptic digest
Background sample       K562 tryptic digest
PTM                     /
Other sample            /
Brief design            A: HY 30/35; B: HY 30/17.5. Each sample has 3 replicates.
Additional runs         /
======================  =============================================================================================================================


HE 4 conditions Orbi
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#22HEBench] Benchmarking of analysis strategies for data-independent acquisition proteomics using a large-scale dataset comprising inter-patient heterogeneity. 10.1038/s41467-022-30094-0

:Authors: Fröhlich et al.
:Year: 2022

:Dataset 1:

======================  ===================================================================================================================================================================================================================================================================================================================================================================================
Short name              HE4Cond
Repository ID           EGAD00010002223 (request required)
MS instrument           Orbitrap Eclipse
Acquisition method      8 m/z inter-cycle overlapping-window DIA (4 m/z shift)
Target sample           E. coli tryptic digest
Background sample       92 tryptic digests from 92 human lymph nodes
PTM                     /
Other sample            Biognosys iRT peptides (C18)
Brief design            Human tissue samples are from 92 different individuals, and 4 groups are formed with 23 samples in each. 4 groups have different amounts of spiked E. coli digest: no E. coli as control, 1:25, 1:12, and 1:6. Each sample is injected once and total 92 DIA data were acquired.
Additional runs         1\) From each group, 3 samples are picked, and all 12 samples are mixed into one. The pooled sample is fractionated and fractions are further pooled in groups of two, and 10 pooled samples are acquired by DDA. 2) The pooled samples were also acquired by narrow-window DIA with a 2 m/z isolation window and total 6 injections to cover 400-1000 m/z.
======================  ===================================================================================================================================================================================================================================================================================================================================================================================


MY 7 conditions Orbi+timsTOF
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#23MYBench] Benchmarking commonly used software suites and analysis workflows for DIA proteomics and phosphoproteomics. 10.1038/s41467-022-35740-1

:Authors: Lou et al.
:Year: 2023

:Dataset 1:

======================  ===================================================================================================================================================================================================================================================================================================
Short name              MY7Cond
Repository ID           PXD034709
MS instrument           QE HF / timsTOF Pro
Acquisition method      Variable wide-window DIA / diaPASEF 16 scans
Target sample           Tryptic digest of mouse brain membrane proteome 
Background sample       Yeast tryptic digest
PTM                     /
Other sample            Biognosys iRT peptides (C18)
Brief design            Mouse brain membrane protein digests were spiked into a yeast proteome background in seven defined proportions, yielding one reference and six mixtures with fixed mouse protein ratios relative to the reference: 1:4, 1:2, 2:3, 1:1, 3:2, and 2:1. Each sample is prepared in five replicates.
Additional runs         Mouse and yeast peptide digestions are first offline pre-fractionated to 8 fractions for each. 16 DDA runs and 16 diaPASEF runs are acquired on respective instruments.
======================  ===================================================================================================================================================================================================================================================================================================


Immunopeptidomics
^^^^^^^^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#23Immuno] Benchmarking Bioinformatics Pipelines in Data-Independent Acquisition Mass Spectrometry for Immunopeptidomics. 10.1016/j.mcpro.2023.100515

:Authors: Shahbazy et al.
:Year: 2023

:Dataset 1:

======================  ========================================================================================================================================
Short name              Immunopeptide spike
Repository ID           PXD034539
MS instrument           Orbitrap Fusion
Acquisition method      24 m/z wide-window DIA
Target sample           Immunopeptides isolated and purified from C1R-B*57:01 cells
Background sample       HeLa tryptic digest
PTM                     /
Other sample            Biognosys iRT peptides (C18)
Brief design            Spike immunopeptides into HeLa background in 6 dilution ratios: 1, 0.8, 0.6, 0.4, 0.2, 0. Each sample is acquired for 3 replicates.
Additional runs         HLA-B*57:01 bound peptides are offline pre-fractionated into 9 fractions, and 9 DDA data are acquired.
======================  ========================================================================================================================================

