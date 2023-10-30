PASEF enhanced DIA
==================

Summary
-------------

.. _table:

=================================  ==========  ==============  ===================  =============================
Name                               Pub date    Instrument      Lab & Co.            Window overlap
=================================  ==========  ==============  ===================  =============================
diaPASEF [#diaPASEF]_              2020 June   timsTOF Pro     Mann Lab             None
Synchro-PASEF [#SynchroPASEF]_     2022 Dec.   timsTOF Pro 2   Mann Lab             Intra-/inter-frame
IM-GPF [#IMGPF]_                   2023 Mar.   timsTOF Pro     Collins Lab          None
Slice-PASEF [#SlicePASEF]_         2022        timsTOF Pro 2   Demichev Lab         Inter-cycle
midiaPASEF [#midiaPASEF]_          2022        timsTOF Pro 2   Tenzer Lab           Intra-/inter-frame
=================================  ==========  ==============  ===================  =============================

.. note::
   - *Pub date*
      - the date the method was publicly released by publisher
      - *Slice-PASEF* is a pre-print
      - *midiaPASEF* is a pre-print in 2023 and has a granted patent in 2022
   - *Instrument*
      - initially developped on which instrument
   - *Lab & Co.*
      - lab or company (the last corresponding author)


Individuals
-----------

|

diaPASEF
^^^^^^^^

back to table_

:Reference: 

.. [#diaPASEF] diaPASEF: parallel accumulation-serial fragmentation combined with data-independent acquisition. 10.1038/s41592-020-00998-0

=========================  =============================================================================================================================
Full name                  diaPASEF
Authors                    Florian Meier et al.
Lab & Company              Mann Lab
Publication date           2020, Oct.
MS instrument              timsTOF Pro
=========================  =============================================================================================================================

:Scheme 1: 

=========================  =============================================================================================================================
Name                       16 diaPASEF scans (standard scheme)
Frames per cycle           16 (2 rows)
MS2 spectra per frame      4
Covered m/z range          400-1200 m/z
MS2 window m/z size        25 m/z
Covered IM range (1/K0)    0.6-1.4 Vs/cm\ :sup:`2`
MS2 window IM size (1/K0)  Variable
Injection times            1
Cycle time                 /
MS2 window features        Consecutive & fixed window size & non-overlapping windows
=========================  =============================================================================================================================

:Scheme 2: 

=========================  =============================================================================================================================
Name                       8 diaPASEF scans (high speed scheme)
Frames per cycle           8
MS2 spectra per frame      3
Covered m/z range          400-1200 m/z
MS2 window m/z size        25 m/z
Covered IM range (1/K0)    0.6-1.4 Vs/cm\ :sup:`2`
MS2 window IM size (1/K0)  Variable
Injection times            1
Cycle time                 ~0.9 s
MS2 window features        Consecutive & fixed window size & non-overlapping windows
=========================  =============================================================================================================================

:Scheme 3: 

=========================  =============================================================================================================================
Name                       4 diaPASEF scans (high sensitivity scheme)
Frames per cycle           4
MS2 spectra per frame      4
Covered m/z range          400-1200 m/z
MS2 window m/z size        50 m/z
Covered IM range (1/K0)    0.6-1.4 Vs/cm\ :sup:`2`
MS2 window IM size (1/K0)  Variable
Injection times            1
Cycle time                 /
MS2 window features        Consecutive & fixed window size & non-overlapping windows
=========================  =============================================================================================================================

:Scheme 4: 

=========================  =============================================================================================================================
Name                       Single diaPASEF scan
Frames per cycle           1
MS2 spectra per frame      12
Covered m/z range          300-1200 m/z
MS2 window m/z size        Variable
Covered IM range (1/K0)    0.6-1.4 Vs/cm\ :sup:`2`
MS2 window IM size (1/K0)  Variable
Injection times            1
Cycle time                 /
MS2 window features        Consecutive & variable window sizes & non-overlapping windows
=========================  =============================================================================================================================


Synchro-PASEF
^^^^^^^^^^^^^

back to table_

:Reference: 

.. [#SynchroPASEF] Synchro-PASEF Allows Precursor-Specific Fragment Ion Extraction and Interference Removal in Data-Independent Acquisition. 10.1016/j.mcpro.2022.100489

=========================  =============================================================================================================================
Full name                  Synchro-PASEF
Authors                    Patricia Skowronek et al.
Lab & Company              Mann Lab
Publication date           2022 Dec.
MS instrument              timsTOF Pro 2
=========================  =============================================================================================================================

:Scheme 1: 

=========================  =============================================================================================================================
Name                       1
Frames per cycle           4
MS2 spectra per frame      927 (100 ms TIMS ramp time)
Covered m/z range          335-1270 m/z
MS2 window m/z size        25 m/z
Quadrupole shift m/z       ~0.9 m/z ((1170 - 335) / 927)
Covered IM range (1/K0)    0.7-1.3 Vs/cm\ :sup:`2`
MS2 window IM size (1/K0)  ~7e-4 Vs/cm\ :sup:`2`
Injection times            1
Cycle time                 ~0.56 s
MS2 window features        Consecutive & fixed window size & intra-/inter-frame overlapping windows
=========================  =============================================================================================================================

:Scheme 2: 

=========================  =============================================================================================================================
Name                       2
Frames per cycle           7
MS2 spectra per frame      927 (100 ms TIMS ramp time)
Covered m/z range          335-1275 m/z
MS2 window m/z size        15 m/z
Covered IM range (1/K0)    0.7-1.3 Vs/cm\ :sup:`2`
MS2 window IM size (1/K0)  ~7e-4 Vs/cm\ :sup:`2`
Injection times            1
Cycle time                 ~0.9 s
MS2 window features        Consecutive & fixed window size & intra-/inter-frame overlapping windows
=========================  =============================================================================================================================

:Scheme 3: 

=========================  =============================================================================================================================
Name                       3
Frames per cycle           4
MS2 spectra per frame      927 (100 ms TIMS ramp time)
Covered m/z range          335-1305 m/z
MS2 window m/z size        35 m/z, 25 m/z, 25 m/z, 50 m/z
Covered IM range (1/K0)    0.7-1.3 Vs/cm\ :sup:`2`
MS2 window IM size (1/K0)  ~7e-4 Vs/cm\ :sup:`2`
Injection times            1
Cycle time                 ~0.56 s
MS2 window features        Consecutive & fixed window size (in one frame) & intra-/inter-frame overlapping windows
=========================  =============================================================================================================================


IM-GPF
^^^^^^

back to table_

:Reference: 

.. [#IMGPF] A gas phase fractionation acquisition scheme integrating ion mobility for rapid diaPASEF library generation. 10.1002/pmic.202200038

=========================  =============================================================================================================================
Full name                  IM-GPF
Authors                    Jack Penny et al.
Lab & Company              Collins Lab
Publication date           2023, Mar.
MS instrument              timsTOF Pro
=========================  =============================================================================================================================

:Scheme 1: 

=========================  =============================================================================================================================
Name                       
Frames per cycle           14
MS2 spectra per frame      2
Covered m/z range          400-1200 m/z
MS2 window m/z size        5 m/z
Covered IM range (1/K0)    0.57-1.47 Vs/cm\ :sup:`2`
MS2 window IM size (1/K0)  /
Injection times            7
Cycle time                 /
MS2 window features        Discrete & fixed window size & margin-overlapping windows (1 m/z)
=========================  =============================================================================================================================


Slice-PASEF
^^^^^^^^^^^

back to table_

:Reference: 

.. [#SlicePASEF] Slice-PASEF: fragmenting all ions for maximum sensitivity in proteomics. 10.1101/2022.10.31.514544

=========================  =============================================================================================================================
Full name                  Slice-PASEF
Authors                    Lukasz Szyrwiel et al.
Lab & Company              Demichev Lab
Publication date           2022
MS instrument              timsTOF Pro 2
=========================  =============================================================================================================================

:Scheme 1: 

=========================  =============================================================================================================================
Name                       1-frame (1F)
Frames per cycle           1
MS2 spectra per frame      15
Covered m/z range          400-1000 m/z
MS2 window m/z size        83.74-215.05 m/z
Demultiplexing region m/z  /
Covered IM range (1/K0)    0.75-1.2 Vs/cm\ :sup:`2`
MS2 window IM size (1/K0)  0.03 Vs/cm\ :sup:`2`
Injection times            1
Cycle time                 /
MS2 window features        Consecutive & variable window size & inter-cycle overlapping windows
=========================  =============================================================================================================================

:Scheme 2: 

=========================  =============================================================================================================================
Name                       2-frame (2F)
Frames per cycle           2
MS2 spectra per frame      10
Covered m/z range          400-1000 m/z
MS2 window m/z size        sub-cycle 1: 20.56-162 m/z; sub-cycle 2: 36.55-136.48 m/z; sub-cycle 3: 31.55-128.05 m/z
Demultiplexing region m/z  variable
Covered IM range (1/K0)    0.75-1.2 Vs/cm\ :sup:`2`
MS2 window IM size (1/K0)  0.045 Vs/cm\ :sup:`2`
Injection times            1
Cycle time                 /
MS2 window features        Consecutive & variable window size & inter-cycle overlapping windows
=========================  =============================================================================================================================

:Scheme 3: 

=========================  =============================================================================================================================
Name                       4-frame (4F)
Frames per cycle           4
MS2 spectra per frame      10
Covered m/z range          400-1000 m/z
MS2 window m/z size        sub-cycle 1: 2.75-115.65 m/z; sub-cycle 2: 12.37-105.96 m/z; sub-cycle 3: 19.1-94.2 m/z; sub-cycle 4: 4.82-84.55 m/z
Demultiplexing region m/z  variable
Covered IM range (1/K0)    0.75-1.2 Vs/cm\ :sup:`2`
MS2 window IM size (1/K0)  0.045 Vs/cm\ :sup:`2`
Injection times            1
Cycle time                 /
MS2 window features        Consecutive & variable window size & inter-cycle overlapping windows
=========================  =============================================================================================================================


midiaPASEF
^^^^^^^^^^^

back to table_

:Reference: 

.. [#midiaPASEF] midiaPASEF maximizes information content in data-independent acquisition proteomics. 10.1101/2023.01.30.526204

=========================  =============================================================================================================================
Full name                  **m**\ axmizing **i**\ nformation content in **diaPASEF**
Authors                    Ute Distler et al.
Lab & Company              Tenzer Lab
Publication date           2022 Dec.
MS instrument              timsTOF Pro 2
=========================  =============================================================================================================================

:Scheme 1: 

=========================  =============================================================================================================================
Name                       
Frames per cycle           20
MS2 spectra per frame      927 (100 ms TIMS ramp time)
Covered m/z range          121-1535 m/z
MS2 window m/z size        36 m/z
Demultiplexing region m/z  12 m/z
Quadrupole shift m/z       ~1.24 m/z ((1535 - 20 * 12 - 24 - 121) / 927)
Covered IM range (1/K0)    0.6-1.56 Vs/cm\ :sup:`2`
MS2 window IM size (1/K0)  ~7e-4 Vs/cm\ :sup:`2`
Injection times            1
Cycle time                 ~2.2 s
MS2 window features        Consecutive & fixed window size & intra-/inter-frame overlapping windows
=========================  =============================================================================================================================

