Windowed DIA
============

Summary
-------------

.. _table:

=====================================  ==========  ========  ========  =============  =============  ============  ==============
Name                                   Pub date    Scan per cycle      Window size (m/z)             MS2 window features
-------------------------------------  ----------  ------------------  ----------------------------  ----------------------------
..                                     ..          MS1       MS2       Acquired       Demul.         Consecutive   Overlap (m/z)
=====================================  ==========  ========  ========  =============  =============  ============  ==============
DIA [#DIA]_                            2004 Sep.   0         100       10             /              T             none
PAcIFIC [#PAcIFIC]_                    2009 July   0         10        2.5            /              T             margin (1)
XDIA [#XDIA]_                          2010 Jan.   1         60        20             /              T             margin (1)
FT-ARM [#FTARM]_                       2012 Jan.   0         5         100            /              T             none
SWATH [#SWATH]_                        2012 Jan.   1         32        25             /              T             margin (1)
MSX [#MSX]_                            2013 June   0/2       20        20             4              random        none
WiSIM-DIA [#WiSIMDIA]_                 2014        3         51        12             /              T             none
pSMART [#pSMART]_                      2014 Sep.   5         110       5,10,20        /              T             margin (1)
HRM [#HRM]_                            2015 Feb.   1         19        24-222         /              T             margin (2)
SONAR [#SONAR]_                        2017 Sep.   200\*     200\*     24             2.5            T             scanning Q1
μDIA [#μDIA]_                          2018 July   1         120       9              3              T             one-third (3)
Staggered DIA [#StaggeredDIA]_         2018 Dec.   2         20        20             10             T             one-half (10)
RTwinDIA [#RTwinDIA]_                  2019 May    1         40        5              /              T             none
DIA-FAIMS [#DIAFAIMS]_                 2020 Feb.   1         49        13.7           /              T             margin (1)
PulseDIA [#PulseDIA]_                  2020 Sep.   1         24        5-29/11-71     /              reg. inter.   margin (1)
PASS-DIA [#PASSDIA]_                   2020 Oct.   5         75        2              /              T             none
HRMS1-DIA [#HRMS1DIA]_                 2020 Oct.   3         54        15             /              T             none
BoxCarmax [#BoxCarmax]_                2021 Feb.   1         30        10             2.5            reg. inter.   margin (1)
Scanning SWATH [#ScanningSWATH]_       2021 Mar.   0         250\*     10             2              T             scanning Q1
BoxCar DIA [#BoxCarDIA]_               2021 July   4         24        20-583         /              reg. inter.   margin (1)
Zeno SWATH [#ZenoSWATH]_               2022 Nov.   1         85        6-10           /              T             margin (1)
Narrow-window DIA [#NarrowwindowDIA]_  2023        1         300       2              /              T             none
=====================================  ==========  ========  ========  =============  =============  ============  ==============

.. note::
   - *Pub date*
      - the date the method was publicly released by publisher
      - *WiSIM-DIA* is released as a Thermo Application Note
      - *Narrow-window DIA* is currently a pre-print
   - *Scan per cycle*
      - Number of finally recorded scans for MS1 or MS2 in one cycle
      - *SONAR* and *Scanning SWATH* are annotated by the numbers of bins at Q1 level
   - Window size (m/z)
      - *Acquired* is the real window size defined in acquisition settings for instrument, and the overlapped size is eliminate (e.g. if 21 m/z widnow size is used to ensure a 1 m/z overlap within adjacent windows, its effective size is 20 m/z)
      - *Demul.* is the computationally demultiplexed window size (so-called `demultiplexing region` in [#StaggeredDIA]_)
   - MS2 window features
      - *Consecutive* indicates if the MS2 windows in a cycle are defined in a continous manner (reg. inter. means regular interval)
      - *Fixed* indicates if all MS2 windows have the same size
      - *Overlap* indicates how the adjacent MS2 windows overlapped (though the adjacent windows might be not consecutive)
   - All window sizes included in this document have margin overlap subtracted


Individuals
-----------

|

DIA
^^^

back to table_

:Reference: 

.. [#DIA] Automated approach for quantitative analysis of complex peptide mixtures from tandem mass spectra. 10/dm8rm4

======================  =============================================================================================================================
Full name               Data-Independent Acquisition
Authors                 John D Venable et al.
Lab & Company           Yates Lab
Publication date        2004, Sep.
MS instrument           LTQ
MS1 spectra per cycle   0
MS2 spectra per cycle   100
MS2 window size         10 m/z
Demultiplexing region   /
Covered mass range      400-1400 m/z
Injection times         1
Cycle time              ~35 s
MS2 window features     Consecutive & fixed window size & non-overlapping windows
======================  =============================================================================================================================

- Vanilla DIA scheme, with no MS1 scans, and a fixed 10 m/z window runs on pre-defined m/z range in a cycle without overlap.


PAcIFIC
^^^^^^^

back to table_

:Reference: 

.. [#PAcIFIC] Precursor Acquisition Independent From Ion Count: How to Dive Deeper into the Proteomics Ocean. 10.1021/ac900888s
.. [#PAcIFIC2] Faster, Quantitative, and Accurate Precursor Acquisition Independent From Ion Count. 10.1021/ac103079q

======================  =============================================================================================================================
Full name               Precursor Acquisition Independent From Ion Count
Authors                 Alexandre Panchaud et al.
Lab & Company           Goodlett Lab
Publication date        2009 July
MS instrument           LTQ Orbitrap XL
MS1 spectra per cycle   0
MS2 spectra per cycle   100
MS2 window size         10 m/z
Demultiplexing region   /
Covered mass range      400-1400 m/z
Injection times         1
Cycle time              ~35 s
MS2 window features     Consecutive & fixed window size & margin-overlapping windows (1 m/z)
======================  =============================================================================================================================

- 2.5 m/z window, and a 1 m/z overlap between adjacent windows.
- The first MS2 scan in the first injection starts from a center mass of 401 m/z, and the last MS2 scan in last injection has a center mass of 1403.5 m/z.
- Requires ~67 injections and ~5 days to finish the acquisition for one sample in 2009 on a LTQ Orbitrap XL instrument, and the effiency is improved to ~2 days with a faster LTQ Orbitrap Velos in 2011.


XDIA
^^^^

back to table_

:Reference: 

.. [#XDIA] XDIA: improving on the label-free data-independent analysis. 10.1093/bioinformatics/btq031

======================  ===================================================================================================================================
Full name               extended DIA
Authors                 Paulo C. Carvalho et al.
Lab & Company           Yates Lab
Publication date        2010, Jan.
MS instrument           LTQ-Orbitrap XL (+ETD)
MS1 spectra per cycle   1
MS2 spectra per cycle   60
MS2 window size         20 m/z
Demultiplexing region   /
Covered mass range      400-1000 m/z
Injection times         1
Cycle time              /
MS2 window features     Consecutive & fixed window size & margin-overlapping windows (1 m/z) & two scans for each window (one for ETD, one for ETD+CID)
======================  ===================================================================================================================================

- Each acquisition window is scaned twice, by using ETD in the first scan and followed by ETD+CAD in the second scan for ion dissociation.


FT-ARM
^^^^^^

back to table_

:Reference: 

.. [#FTARM] Accurate Peptide Fragment Mass Analysis: Multiplexed Peptide Identification and Quantification. 10.1021/pr2008175

======================  =============================================================================================================================
Full name               Fourier Transform-All Reaction Monitoring
Authors                 Chad R. Weisbrod et al.
Lab & Company           Bruce Lab
Publication date        2012, Jan.
MS instrument           LTQ-FT and LTQ Orbitrap
MS1 spectra per cycle   0
MS2 spectra per cycle   5
MS2 window size         100 m/z
Demultiplexing region   /
Covered mass range      500-1000 m/z
Injection times         1
Cycle time              ~5.45 s
MS2 window features     Consecutive & fixed window size & non-overlapping windows
======================  =============================================================================================================================


SWATH
^^^^^

back to table_

:Reference: 

.. [#SWATH] Targeted data extraction of the MS/MS spectra generated by data-independent acquisition: a new concept for consistent and accurate proteome analysis. 10.1074/mcp.O111.016717

======================  ===================================================================================================================================
Full name               Sequential Window Acquisition of all THeoretical (mass spectra)
Authors                 Ludovic C. Gillet et al.
Lab & Company           Aebersold Lab
Publication date        2012, Jan.
MS instrument           TripleTOF 5600
MS1 spectra per cycle   1
MS2 spectra per cycle   32
MS2 window size         25 m/z
Demultiplexing region   /
Covered mass range      400-1200 m/z
Injection times         1
Cycle time              ~3.3 s
MS2 window features     Consecutive & fixed window size & margin-overlapping windows (1 m/z)
======================  ===================================================================================================================================


MSX
^^^

:Reference: 

.. [#MSX] Multiplexed MS/MS for improved data-independent acquisition. 10.1038/nmeth.2528

======================  ===================================================================================================================================
Full name               MSX
Authors                 Jarrett D Egertson et al.
Lab & Company           MacCoss Lab
Publication date        2013, June
MS instrument           Q Exactive
MS1 spectra per cycle   0 (or 2 for MS1 quantification)
MS2 spectra per cycle   20 (5 discrete sub-windows in each scan)
MS2 window size         20 m/z (5 * 4 m/z sub-window for ion accumulation)
Demultiplexing region   4 m/z
Covered mass range      500-900 m/z
Injection times         1
Cycle time              ~3.5 s
MS2 window features     5 sub-windows in each scan are randomly picked & fixed window size & non-overlapping windows
======================  ===================================================================================================================================

- Actual center position of Q1 in the first 4 m/z segment is 502.4783 m/z with a window width of 4.002 m/z, agreeing with m/z distribution of precursor residue combinations.


WiSIM-DIA
^^^^^^^^^

back to table_

:Reference: 

.. [#WiSIMDIA] Large-scale targeted protein quantification using wide selected-ion monitoring data-independent acquisition. Thermo Scientific Application Note 600
.. [#WiSIMDIA2] Application of wide selected-ion monitoring data-independent acquisition to identify tomato fruit proteins regulated by the CUTIN DEFICIENT2 transcription factor. 10.1002/pmic.201500450

======================  ===================================================================================================================================
Full name               Wide Selected-Ion Monitoring DIA
Authors                 Reiko Kiyonami et al.
Lab & Company           Thermo Fisher Scientific GmbH
Publication date        2014
MS instrument           Orbitrap Fusion Tribrid
MS1 spectra per cycle   3
MS2 spectra per cycle   51
MS2 window size         12 m/z
Demultiplexing region   /
Covered mass range      400-1004 m/z
Injection times         1
Cycle time              ~3.6 s
MS2 window features     Consecutive & fixed window size & non-overlapping windows
======================  ===================================================================================================================================

- MS2 scans are performed in ion trap in parallel with MS1 scan in Orbitrap


pSMART
^^^^^^

back to table_

:Reference: 

.. [#pSMART] Hybrid data acquisition and processing strategies with increased throughput and selectivity: pSMART analysis for global qualitative and quantitative analysis. 10.1021/pr5003017

======================  ===================================================================================================================================
Full name               pSMART
Authors                 Amol Prakash et al.
Lab & Company           Thermo Fisher Scientific GmbH
Publication date        2014, Sep.
MS instrument           Q Exactive
MS1 spectra per cycle   5
MS2 spectra per cycle   110
MS2 window size         5 m/z window for 400-800 m/z, 10 m/z window for 800-1000 m/z, 20 m/z window for 1000-1200 m/z
Demultiplexing region   /
Covered mass range      400-1200 m/z
Injection times         1
Cycle time              ~26 s
MS2 window features     Consecutive & variable window sizes & margin-overlapping windows (1 m/z)
======================  ===================================================================================================================================

- In each cycle, 5 HR/AM MS1 spectra are acquired every ~5 s.


HRM
^^^^^^^^^

back to table_

:Reference: 

.. [#HRM] Extending the Limits of Quantitative Proteome Profiling with Data-Independent Acquisition and Application to Acetaminophen-Treated Three-Dimensional Liver Microtissues. 10.1074/mcp.M114.044305

======================  ===================================================================================================================================
Full name               Hyper Reaction Monitoring
Authors                 Roland Bruderer et al.
Lab & Company           Biognosys AG
Publication date        2015, Feb.
MS instrument           Q Exactive
MS1 spectra per cycle   1
MS2 spectra per cycle   19
MS2 window size         Variable (24-222 m/z)
Demultiplexing region   /
Covered mass range      400-1220 m/z
Injection times         1
Cycle time              ~3.5 s
MS2 window features     Consecutive & variable window sizes & margin-overlapping windows (2 m/z)
======================  ===================================================================================================================================


SONAR
^^^^^^^^^

back to table_

:Reference: 

.. [#SONAR] Scanning Quadrupole Data-Independent Acquisition, Part A: Qualitative and Quantitative Characterization. 10.1021/acs.jproteome.7b00464

======================  ===================================================================================================================================
Full name               SONAR
Authors                 M. Arthur Moseley et al.
Lab & Company           Waters Corporation
Publication date        2017, Sep.
MS instrument           Xevo G2-XS
MS1 spectra per cycle   200
MS2 spectra per cycle   200
MS2 window size         24 m/z
Demultiplexing region   2.5 m/z
Covered mass range      400-900 m/z
Injection times         1
Cycle time              ~1 s
MS2 window features     Consecutive & fixed window size & intra-overlapping windows (21.5 m/z at Q1 bin level)
======================  ===================================================================================================================================


μDIA
^^^^^^^^^

back to table_

:Reference: 

.. [#μDIA] Micro-Data-Independent Acquisition for High-Throughput Proteomics and Sensitive Peptide Mass Spectrum Identification. 10.1021/acs.analchem.8b01026

======================  ===================================================================================================================================
Full name               microDIA
Authors                 Michael R. Heaven et al.
Lab & Company           Norris Lab
Publication date        2018, July
MS instrument           impact II
MS1 spectra per cycle   1
MS2 spectra per cycle   120
MS2 window size         9 m/z
Demultiplexing region   3 m/z
Covered mass range      400-1115 m/z
Injection times         1
Cycle time              ~3.4 s
MS2 window features     Consecutive & fixed window size & intra-overlapping windows (3 m/z)
======================  ===================================================================================================================================


Staggered DIA
^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#StaggeredDIA] Chromatogram libraries improve peptide detection and quantification by data independent acquisition mass spectrometry. 10.1038/s41467-018-07454-w
.. [#StaggeredDIA2] Improving Precursor Selectivity in Data-Independent Acquisition Using Overlapping Windows. 10.1007/s13361-018-2122-8

======================  ===================================================================================================================================
Full name               microDIA
Authors                 Brian C. Searle et al.
Lab & Company           MacCoss Lab
Publication date        2018, Dec.
MS instrument           Q Exactive
MS1 spectra per cycle   2
MS2 spectra per cycle   20
MS2 window size         20 m/z
Demultiplexing region   10 m/z
Covered mass range      490-900 m/z
Injection times         1
Cycle time              ~2.5 s
MS2 window features     Consecutive & fixed window size & inter-overlapping windows (10 m/z)
======================  ===================================================================================================================================

- In two-step cycles, odd-numbered cycle covers 500-900 m/z and even-numbered cycle covers 490-890 m/z.


RTwinDIA
^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#RTwinDIA] Assessing the Relationship Between Mass Window Width and Retention Time Scheduling on Protein Coverage for Data-Independent Acquisition. 10.1007/s13361-019-02243-1

======================  ===================================================================================================================================
Full name               RT windowed DIA
Authors                 Wenxue Li et al.
Lab & Company           Liu Lab
Publication date        2019, May
MS instrument           Orbitrap Fusion Lumos
MS1 spectra per cycle   1
MS2 spectra per cycle   40
MS2 window size         5 m/z
Demultiplexing region   /
Covered mass range      400-1000 m/z
Injection times         1
Cycle time              ~3.2 s
MS2 window features     Consecutive & fixed window size & non-overlapping windows
======================  ===================================================================================================================================

- MS1 covers 350-1650 m/z. MS2 in 3 blocks: 400-600 m/z for RT range 0-50%; 600-800 m/z for RT range 50-75%; 800-1000 m/z for RT range 75-100%.


DIA-FAIMS
^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#DIAFAIMS] A Compact Quadrupole-Orbitrap Mass Spectrometer with FAIMS Interface Improves Proteome Coverage in Short LC Gradients. 10.1074/mcp.TIR119.001906

======================  ===================================================================================================================================
Full name               DIA-FAIMS
Authors                 Dorte B. Bekker-Jensen et al.
Lab & Company           Olsen Lab
Publication date        2020, Feb.
MS instrument           Orbitrap Exploris 480
MS1 spectra per cycle   1
MS2 spectra per cycle   49
MS2 window size         13.7 m/z (15k2s method)
Demultiplexing region   /
Covered mass range      361-1032.3 m/z (15k2s method)
Injection times         1
Cycle time              ~2.3 s (15k2s method)
MS2 window features     Consecutive & fixed window size & margin-overlapping windows (1 m/z)
======================  ===================================================================================================================================


PulseDIA
^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#PulseDIA] PulseDIA: Data-Independent Acquisition Mass Spectrometry Using Multi-Injection Pulsed Gas-Phase Fractionation. 10.1021/acs.jproteome.0c00381

======================  ===================================================================================================================================
Full name               PulseDIA
Authors                 Xue Cai et al.
Lab & Company           Guo Lab
Publication date        2020, Sep.
MS instrument           Q Exactive HF
MS1 spectra per cycle   1
MS2 spectra per cycle   24
MS2 window size         Variable 5-29 m/z for 4 injections, and variable 11-71 m/z for 2 injections
Demultiplexing region   /
Covered mass range      400-1200 m/z
Injection times         2-5
Cycle time              ~2 s
MS2 window features     Discrete & variable window size & margin-overlapping windows (1 m/z)
======================  ===================================================================================================================================

- Each cycle has 1 MS1 scan and 24 MS2 scans. MS1 covers 390-1210 m/z, and MS2 from all injections covers 400-1200 m/z.
- The MS2 covered 800 m/z are split into 24 segments, in which 20 segments with 20 m/z width cover 400-800 m/z, and the other 4 segments cover 800-860, 860-940, 940-1060, 1060-1200 m/z.
- Each segment is equally divided into n parts, where n is the injection number, and 1 m/z overlap is added when determining the window size.
- Four window schemes are defined: 2-injection has window sizes of 11, 31, 41, 61, and 71 m/z; 3-injection has window sizes of 8, 21, 28, 41, and 48 m/z; 4-injection has window sizes of 6, 16, 21, 31, and 36 m/z; 5-injection has window sizes of 5, 13, 17, 25, and 29 m/z.


PASS-DIA
^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#PASSDIA] PASS-DIA: a data-independent acquisition approach for discovery studies. 10.1021/acs.analchem.0c02513

======================  ===================================================================================================================================
Full name               Precursor ion And Small Slice-DIA
Authors                 Dong-Gi Mun et al.
Lab & Company           Pandey Lab
Publication date        2020, Oct.
MS instrument           Q Exactive HF
MS1 spectra per cycle   5
MS2 spectra per cycle   75
MS2 window size         2 m/z
Demultiplexing region   /
Covered mass range      350-1400 m/z
Injection times         7
Cycle time              /
MS2 window features     Consecutive & fixed window size & non-overlapping windows
======================  ===================================================================================================================================

- Each injection covers 150 m/z. Each cycle has 75 MS2 scans with a fixed 2 m/z window size, and MS1 scan is acquired per 15 MS2 scans.


HRMS1-DIA
^^^^^^^^^^

back to table_

:Reference: 

.. [#HRMS1DIA] Standardization and harmonization of distributed multi-center proteotype analysis supporting precision medicine studies. 10.1038/s41467-020-18904-9

======================  ===================================================================================================================================
Full name               High-Resolution MS1-based quantitative DIA
Authors                 Yue Xuan et al.
Lab & Company           Thermo Fisher Scientific GmbH
Publication date        2020, Oct.
MS instrument           Q Exactive HF
MS1 spectra per cycle   3
MS2 spectra per cycle   54
MS2 window size         15 m/z
Demultiplexing region   /
Covered mass range      400-1210 m/z
Injection times         1
Cycle time              ~5.23 s
MS2 window features     Consecutive & fixed window size & non-overlapping windows
======================  ===================================================================================================================================

- Each cycle comprises 3 MS1 full scans and 54 sequential MS2 scans. MS1 full scans are inserted before the 1st, 18th, 35th MS2 scans. Each MS1 full scan covers whole mass range of 400-1210 m/z.


BoxCarmax
^^^^^^^^^^

back to table_

:Reference: 

.. [#BoxCarmax] BoxCarmax: A High-Selectivity Data-Independent Acquisition Mass Spectrometry Method for the Analysis of Protein Turnover and Complex Samples. 10.1021/acs.analchem.0c04293

======================  ===================================================================================================================================
Full name               BoxCarmax
Authors                 Barbora Salovska et al.
Lab & Company           Liu Lab
Publication date        2021, Feb.
MS instrument           Orbitrap Fusion Lumos
MS1 spectra per cycle   1
MS2 spectra per cycle   30
MS2 window size         10 m/z (4 * 2.5 m/z sub-windows)
Demultiplexing region   /
Covered mass range      357-1197 m/z
Injection times         4
Cycle time              ~2.8 s
MS2 window features     Discrete & fixed window size & margin-overlapping windows (1 m/z)
======================  ===================================================================================================================================


Scanning SWATH
^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#ScanningSWATH] Ultra-fast proteomics with Scanning SWATH. 10.1038/s41587-021-00860-4

======================  ===================================================================================================================================
Full name               Scanning SWATH
Authors                 Christoph B. Messner et al.
Lab & Company           Ralser Lab
Publication date        2021, Mar.
MS instrument           TripleTOF 6600
MS1 spectra per cycle   0
MS2 spectra per cycle   250
MS2 window size         10 m/z
Demultiplexing region   2 m/z
Covered mass range      400-900 m/z
Injection times         1
Cycle time              ~0.52s (5 min gradient), ~0.31s (1 min gradient), ~0.28s (0.5 min gradient)
MS2 window features     Consecutive & fixed window size & intra-overlapping windows (8 m/z at Q1 bin level)
======================  ===================================================================================================================================


BoxCar DIA
^^^^^^^^^^

back to table_

:Reference: 

.. [#BoxCarDIA] MaxDIA enables library-based and library-free data-independent acquisition proteomics. 10.1038/s41587-021-00968-7

======================  ===================================================================================================================================
Full name               BoxCar DIA
Authors                 Pavel Sinitcyn et al.
Lab & Company           Cox Lab
Publication date        2021, July
MS instrument           Orbitrap Fusion Lumos
MS1 spectra per cycle   4
MS2 spectra per cycle   24
MS2 window size         Variable (20-583 m/z)
Demultiplexing region   /
Covered mass range      350-1650 m/z
Injection times         1
Cycle time              ~3.3 s
MS2 window features     Consecutive & variable window size & margin-overlapping windows (1 m/z)
======================  ===================================================================================================================================

- "BoxCar DIA" instrument settings were extracted from "20201006_LU1_DaIt_Aurora5_HEK1_BOXCAR_SWATH_2ul.raw" from PXD022589 accompanying with MaxDIA paper.
- Each cycle has 1 MS1 full scan, 3 tSIM scans, and 24 MS2 scans sequentially arranged. MS1 full scan covers 350-1650 m/z. 3 tSIM scans are interspersed with each other like those in BoxCar DDA, start from 350-385, 384-412, and 411-434 m/z, respectively, and end at 898-966, 965-1068, 1067-1650 m/z, respectively.


Zeno SWATH
^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#ZenoSWATH] High-throughput proteomics of nanogram-scale samples with Zeno SWATH MS. 10.7554/eLife.83947

======================  ===================================================================================================================================
Full name               Zeno SWATH
Authors                 Ziyue Wang et al.
Lab & Company           Ralser Lab
Publication date        2022 Nov.
MS instrument           ZenoTOF 7600
MS1 spectra per cycle   1
MS2 spectra per cycle   85
MS2 window size         6-10 m/z
Demultiplexing region   /
Covered mass range      400-903 m/z
Injection times         1
Cycle time              /
MS2 window features     Consecutive & variable window size & margin-overlapping windows (1 m/z)
======================  ===================================================================================================================================


Narrow-window DIA
^^^^^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#NarrowwindowDIA] Narrow-window DIA: Ultra-fast quantitative analysis of comprehensive proteomes with high sequencing depth. 10.1101/2023.06.02.543374

======================  ===================================================================================================================================
Full name               Narrow-window DIA
Authors                 Ulises H. Guzman et al.
Lab & Company           Olsen Lab
Publication date        2023
MS instrument           Orbitrap Astral
MS1 spectra per cycle   1
MS2 spectra per cycle   300
MS2 window size         2 m/z
Demultiplexing region   /
Covered mass range      380-980 m/z
Injection times         1
Cycle time              /
MS2 window features     Consecutive & fixed window size & non-overlapping windows
======================  ===================================================================================================================================

