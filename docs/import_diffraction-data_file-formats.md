# Diffraction Data File Formats

## Diffraction Data File Formats
Match! is able to read (import) the following diffraction data file formats of diffractometer manufacturers:
- Bruker/Siemens raw data (*.raw)
- Bruker/Siemens DIFFRAC AT peak (dif) data (*.dif)
- Bruker AXS BRML raw data (*.brml)
- DRON-3
- G670 raw data (*.gdf)
- GNR raw data (formerly Ital Structures raw data) (*.esg)
- GSAS raw data (*.raw, *.gsas)
- INEL raw data (*.dat)
- Jade/MDI/SCINTAG raw data (*.mdi)
- JEOL ASCII Export raw data (*.txt)
- PANalytical/Philips raw data (*.rd)
- PANalytical/Philips raw data (*.udf)
- PANalytical/Philips peak data (*.udi)
- Rigaku RAS raw data (*.ras)
- Rigaku raw data (*.raw)
- SCINTAG raw data (*.raw, *.rd)
- Seifert
- Shimadzu raw data (*.raw)
- Siemens raw data (*.uxd)
- Sietronics XRD scan data (*.cpi)
- Stoe Raw data (*.raw)
- Stoe Peak File (*.pks)
- TXRD text export (*.txt)
- XPowder raw data (*.plv)
- XRDML Scan raw data (*.xrdml)
Besides this, the following "free" formats can be imported as well:
- DBWS Raw data (*.rfl, *.dat)
- ASCII profile (start, step, end, intensities; *.dat)
- ASCII profile (start, step, intensities; *.pro)
- ASCII profile (2 columns: 2theta/d intensity; *.dat)
- ENDEAVOUR peak list (2 columns: 2theta/d intensity; *.dif)
Please note: Match! cannot import diffraction data files that contain the old Mac line endings (CR only). Please make sure to convert the line endings either to LF or CR/LF in your text editor, then try again!
Please contact Crystal Impact if the file format you are using is not yet supported!
In order to read/import a diffraction data file, please select the "Diffraction data"
command from the "File/Import" menu. Match! is capable of identifying all
currently supported diffraction data file formats automatically (at least if you select "All files (automatic detection) (*.*)" at the
bottom of the "Select diffraction data" dialog). Simply select the directory and the
file you would like to import, then press "Open". Depending on the selected file format, a new
dialog may open in which you can e.g. define the wavelength of the radiation. Afterwards,
the diffraction pattern import is finished; the pattern will be displayed.
The "free" formats mentioned above are now described in detail:
DBWS Raw data (*.rfl, *.dat): Files in the DBWS format (file extension usually *.rfl or *.dat) are ASCII files an can be edited using any
conventional text editor. Match! uses the following format: In the first line,
the 2theta start, step and final value as well as a title are given. In the following
lines, the intensity values for each step are given in Fortran 8F7 format. Example:
5.293   0.030  42.523    1003
600     600     600     600     600     600     600     600
600     600     600     600     600     600     600     600
603     603     603     603     603     603     604     604
604     604     604     604     604     606     606     606
606     606     607     607     607     609     609     609
610     612     612     613     615     616     617     619
620     623     626     629     633     638     644     651
661     673     690     713     752     822     961    1227
1665    2247    2777    2876    2446    1848    1353    1034
858     770     725     697     678     664     654     646
(...)
ASCII profile (start, step, end, intensities; *.dat): This is a common ASCII file format for raw (profile) data; files in this format can be
edited using any conventional text editor. Match! expects the following format:
In the first line, the 2theta start, step and final value are given. In the following
lines, the intensity values for each step are given. The number of intensity values
per line may vary. Example:
5.000   0.020  77.000
3410    3537    3406    3278    3425    3446    3430    3395    3346
3485    3285    3222    3323    3269    3276    3238    3172    3223
3129    3238    3137    3211    3075    3139    3098    3068    2978
2984    2968    2998    2971    3035    2954    3003    2928    2797
2831    2920    2907    2949    2769    2768    2798    2775    2833
(...)
ASCII profile (start, step, intensities; *.pro): This is another common ASCII file format for raw (profile) data; files in this format can be
edited using any conventional text editor. Match! expects the following format:
In the first line, the 2theta start and step value are given. In the following
lines, the intensity values for each step are given. The number of intensity values
per line may vary. Example:
3.201   0.029
272   257   250   280   225   268   258   270   285   265
272   261   272   254   261   260   243   254   242   266
259   278   227   273   280   266   259   311   292   303
(...)
ASCII profile (2 columns: 2theta/d intensity; *.dat): This is also a common ASCII file format for raw (profile) data; files in this format
can be edited using any conventional text editor.
Match! expects the following format: Each line contains a 2theta or d-value and
the corresponding intensity separated by space(s) (commas will be ignored). You can
also enter comment lines (which are ignored, too). Example:
# This is a comment line.
# And here come the data:
10.000000,  685.562866
10.010000,  629.170715
10.020000,  637.972717
10.030000,  616.176697
10.040000,  612.602234
10.050000,  629.820190
10.060000,  630.793823
10.070000,  631.725220
10.080000,  618.113525
10.090000,  627.071289
(...)
Endeavour peak list (2 columns: 2theta/d intensity; *.dif): Peak lists that can be imported to or exported from Endeavour are simple two-column ASCII files (file extension *.dif).
They can also be created or edited using any conventional text editor. Match!
expects a line for each individual peak, containing the 2theta or d-value and
the intensity (separated by one or more spaces): Example:
9.804231    42.6
8.207172    88.0
7.314649    17.3
6.254809    19.6
5.768748    35.6
5.424906    15.8
5.167478    24.2