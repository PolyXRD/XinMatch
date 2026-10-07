# The Reference Pattern Database

## The Reference Pattern Database
Match! identifies phases in a sample by comparing its powder diffraction pattern to
reference patterns of known phases. Hence, it needs a so-called "reference database"
in which these reference patterns are provided. The reference databases are managed in the
so-called "Reference Database Library" dialog.
There are several options for obtaining a reference database:
- A free-of-charge reference database called "COD" is by default
installed automatically along with Match!; it can
be used straight away after the installation. This reference database contains powder diffraction
patterns calculated from crystal structure data taken from the
"Crystallography Open Database" (COD), which itself provides crystal structure data published by the
IUCr journals, the
"American Mineralogist Crystal Structure Database"
(AMCSD), and various other sources.
In this context, we would like to thank Pete Strickland (IUCr), Armel Le Bail (COD)
and Bob Downs (AMCSD) for their kind permission to download and distribute their data
free-of-charge!
All entries of the "COD" reference database contain atomic coordinates, based on
which the corresponding powder
diffraction patterns have been calculated. Besides this, for all entries, I/Ic-values
have been calculated, so that a semi-quantitative analysis
can be carried out.
You can download additional or updated reference databases free-of-charge from
https://www.crystalimpact.de/match/download.htm#refdb
- The classical reference pattern database is the so-called "Powder Diffraction
File (PDF)" database provided by ICDD (International Centre for
Diffraction Data, 12 Campus Boulevard, Newtown
Square, PA 19073-3273, U.S.A. Phone: +1-610-325-9814; Fax: +1-610-325-9823; E-mail:
info@icdd.com, Internet: http://www.icdd.com). There are several PDF database products available
(e.g. PDF-2, PDF-5+, PDF-4/Axiom, PDF-4/Minerals), all of which can be used with
Match!. According to our knowledge, the PDF is the largest and most comprehensive source of reference
diffraction patterns.
- You can use a previous ICSD/Retrieve version (release 1993-2002)}
that you might have available. Match! can import the ICSD/Retrieve entries
into a normal Match! user database and calculate reference powder
diffraction patterns in a single step; please follow these instructions if you would like to do so.
Note: Of course, you must have a valid licence for ICSD/Retrieve!
Please contact FIZ Karlsruhe (Germany) (e-mail: crysdata@fiz-karlsruhe.de) if you
are in doubt whether your licence is still valid!
- Many users also have diffraction patterns of own compounds which are not
(yet) present in the COD or PDF databases. Hence, it is desirable to use
these patterns in phase analysis in addition to the "normal" patterns. This can be achieved using the
so-called "user database".
You cannot only use one or the other of the above-mentioned reference databases but also combinations
of them. For example, you can combine diffraction patterns of your own compounds with the COD database
that is installed with Match!.
Please note:
- We recommend to use an ICDD PDF database as reference database (if you have it available), either stand-alone or in combination with the COD database that is installed along with Match!. The background why we recommend the PDF compared to the COD is that we have found that at least in case of natural samples (e.g. minerals, rocks etc.), the PDF sometimes gives better qualitative analysis results than the COD. This seems to be caused by the fact that certain phases show a certain variation of peak positions and intensities, e.g. caused by the insertion or replacement of atoms (leading to different unit cell parameters and hence peak positions) or preferred-orientation effects (causing the intensities of certain peaks to be different from the ones calculated just from the given crystal structure).
In contrast to the COD (which only contains calculated powder diffraction patterns), the PDF also contains a large variety of experimental patterns with very different origin and quality, some of which may also show the "variations" just mentioned. As a result, the probability that the PDF contains a reference pattern that is similar to the one of your sample maybe higher than when using the COD.
- When selecting your reference database, you should always keep in mind
that there may be unforeseen phases in your samples, in which case it is extremely
useful to have a large pattern database available in which even diffraction
patterns of "strange" phases are present.
- If you are using the
normal Match! demoversion, only data from the "Inorganics" subset of the COD are installed.
You can e.g. download
and install the full COD reference database from the Match! download page,
or from a Crystal Impact DVD distributed at various meetings, e.g. the ECM- or IUCr-conferences.