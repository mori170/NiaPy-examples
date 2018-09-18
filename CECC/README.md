# CEC Competitions on Constrained Real Parameter single objective optimization

## Requirements

- [Python](https://www.python.org/downloads/) >= 3.6 (should also work with version >= 2.7)
- [NiaPy](https://github.com/NiaOrg/NiaPy)

## Installation

1. Install [NiaPy](https://github.com/NiaOrg/NiaPy).
2. Clone or download [NiaPy-examples](https://github.com/NiaOrg/NiaPy-examples).
3. Navigate to one of the CEC competitions folders, e.g. to `cec2014` by running `cd cec2014`.
4. Build the library by running `make build`.
5. Shared library should be installed.
6. For a simple run, navigate `cd ..` and run `python run_cec.py -c 14`.
7. If build has been successful, simple run should output function values and coordinates.

## Program parameters

Following command line program parameters are applicable for [NiaPy-examples](https://github.com/NiaOrg/NiaPy-examples):
- `-c` or `--cec`: Set the year of CEC competition, options: `8, 13, 14, 15, 17, 18`, e.g. `-c 14`.
- `-f` or `--fnum`: Set the function number, options: unsigned integers, vary by the benchmark used, e.g. `-f 12`.
- `-sr` or `--srange`: Set the lower and upper limit of search space for selected function, options: positive and negative real numbers (first number lower than the second).
- `-d` or `--dim`: Set the number of dimensions, options: `10, 30, 50, 100`, e.g. `-d 10`.
- `-nr` or `--nFESreduc`: Set the number of evaluations reduction factor, options: `0.01, 0.02, 0.03, 0.05, 0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9, 1.0`.
- `-rn` or `--rnum`: Set the number of runs per selected function, options: unsigned integers.
- `-o` or `--wout`: Set the write generation of data to external file, options: set `True` by options `['true', 'True', 'TRUE', 'T', 'yes', 'Yes', 'YES', 'Y']`, if write generation desired, or set `False` otherwise.

## Run example

Run command: `python run_cec.py -a 'ASO' -D 10 -f 12 -r log`

Output of run command:
```
INFO:NiaPy.util.utility:nFES:1 nGEN:0 => [-43.16774167  55.01802883  16.3792441   71.67379508  44.52412048 54.14094173 -51.73239555  22.39064971  15.05879651 -65.19196055] -> 33956346353.41588
INFO:NiaPy.util.utility:nFES:2 nGEN:0 => [ 71.10589395 -94.03442653 -20.34664197   1.98581091  24.44662371 10.18942337  82.52507288  82.64043405  18.12440511 -13.39198912] -> 5689341897.671973
INFO:NiaPy.util.utility:nFES:18 nGEN:0 => [ 29.24655084   6.71162185 -29.27564081 -88.4029866   49.05360965  4.98174263  72.10299837  -9.15216408 -44.02410145  17.76610938] -> 5099360674.719728
INFO:NiaPy.util.utility:nFES:30 nGEN:0 => [ 87.23831592 -65.18322691 -48.0793461    1.50617376 -48.39579514 47.04167745  75.86802888  -1.17435463 -16.64123099  10.43891658] -> 4440634334.125184
INFO:NiaPy.util.utility:nFES:35 nGEN:0 => [  7.72778804 -67.67640048  72.16216724  15.71141878 -48.44888186 33.3484362   18.39212844  63.05774726  43.23933185  37.09263718] -> 3992440533.7200375
INFO:NiaPy.util.utility:nFES:40 nGEN:0 => [ 24.61829124 -83.55170216 -40.70300123   9.91099863  37.04265244 10.38923349  68.24442755 -19.0533952   16.48301851  71.90575062] -> 2909934717.222438
INFO:NiaPy.util.utility:nFES:132 nGEN:1 => [ 20.61019557 -65.18322691 -46.20031025   1.73696393 -50.36010464 47.57615218  74.50745667  -1.17435463 -16.64123099  10.43891658] -> 1332600549.440013
INFO:NiaPy.util.utility:nFES:276 nGEN:2 => [ 20.61019557 -67.67640048 -46.20031025  17.22339726 -48.44888186 33.3484362   18.39212844  63.05774726 -16.64123099  10.43891658] -> 1078538768.0886617
INFO:NiaPy.util.utility:nFES:627 nGEN:5 => [ 96.15615718   6.71162185  11.15418863 -57.44687467  -9.63652145  4.98174263 -17.52089717  28.67376596 -27.39655771  17.76610938] -> 920956024.5798184
INFO:NiaPy.util.utility:nFES:843 nGEN:7 => [ 43.32909543   7.29827743 -52.62680801  19.71437061 -30.86018932  4.98174263  72.10299837  -8.04625173  16.48301851  73.5003723 ] -> 661223304.3257633
INFO:NiaPy.util.utility:nFES:915 nGEN:7 => [ 30.09365806  64.66114508  89.40800108 -54.6379379  -48.2092377 20.55533764  -7.1147876    5.83438037  -7.14784697  27.22777548] -> 436087835.87833506
INFO:NiaPy.util.utility:nFES:987 nGEN:8 => [ 83.84869097 -56.85261928   6.06585611  45.15385647 -14.56154735 20.57159913   4.11988411  22.60136227  -8.03848425  52.30701471] -> 411486435.96406156
INFO:NiaPy.util.utility:nFES:1043 nGEN:8 => [ 30.09365806  64.66114508  89.40800108 -54.6379379  -48.2092377 20.55533764  -7.1147876    6.68988644  -6.34143326  27.22777548] -> 402839377.3892343
INFO:NiaPy.util.utility:nFES:1115 nGEN:9 => [ 83.84869097 -56.85261928   6.06585611  45.15385647 -11.87782256 20.25556556   3.85573919  22.60136227  -8.03848425  52.30701471] -> 379695429.2399805
INFO:NiaPy.util.utility:nFES:1173 nGEN:9 => [ 30.09365806  64.66114508 -94.39864504 -55.15706512 -14.36854008 19.35100886  57.40630954  23.1189682  -20.10121565  27.22777548] -> 305436823.92925876
INFO:NiaPy.util.utility:nFES:1671 nGEN:13 => [ 20.61019557  90.2852806  -51.70662555 -89.94149183 -50.29165183 21.29998304  56.96967348  22.39064971  -7.14784697  17.76610938] -> 166456401.97538912
INFO:NiaPy.util.utility:nFES:1799 nGEN:14 => [ 20.93009384  91.41309893 -50.32976208 -89.72739172 -50.29165183 21.29998304  56.96967348  22.39064971  -7.97852328  17.76610938] -> 164653330.74250296
INFO:NiaPy.util.utility:nFES:2057 nGEN:16 => [ 20.93009384  91.41309893 -48.9880964  -89.72739172 -50.29165183 21.29998304  56.7990824   22.39064971  -7.97852328  17.76610938] -> 164042191.83642435
INFO:NiaPy.util.utility:nFES:2315 nGEN:18 => [ 20.93009384  91.41309893 -48.9880964  -89.72739172 -50.29165183 21.29998304  55.63603747  22.39064971  -7.97852328  17.76610938] -> 160042017.91060525
INFO:NiaPy.util.utility:nFES:2406 nGEN:19 => [ 85.25323021 -15.40291663   4.7372178   48.8809688   -7.07883391 22.69381539 -16.62762454  23.2923205   -5.94929318  27.22777548] -> 17816308.223923806
INFO:NiaPy.util.utility:nFES:3423 nGEN:27 => [ 36.56079781 -31.91852905 -53.13188982 -64.92788043 -82.29400023  2.26102777 -57.39791901   2.06672817  36.23111267  73.5003723 ] -> 15357719.78580084
INFO:NiaPy.util.utility:nFES:3566 nGEN:28 => [ 82.60302107 -13.44817525   5.70160483  44.05798075  -8.7587571 23.66509599 -16.02186404  23.20414402  -5.07386087  27.22777548] -> 15307567.516827516
INFO:NiaPy.util.utility:nFES:3568 nGEN:28 => [ 85.25323021 -13.44817525   5.70160483  44.05798075  -8.7587571 23.66509599 -16.62762454  23.20414402  -5.94929318  27.22777548] -> 12131707.677725408
INFO:NiaPy.util.utility:nFES:3680 nGEN:29 => [ 36.53282588 -32.81637714 -53.12290564 -68.91644348 -82.29400023 1.27874245 -57.99680535   2.40878516  36.23111267  73.5003723 ] -> 10732163.907324154
INFO:NiaPy.util.utility:nFES:3809 nGEN:30 => [ 36.53282588 -32.81637714 -53.12290564 -68.91644348 -82.29400023 1.27874245 -56.94282212   2.40878516  36.23111267  73.5003723 ] -> 10079873.197230447
INFO:NiaPy.util.utility:nFES:4084 nGEN:32 => [ 87.26247246 -13.44817525   5.70160483  44.05798075  -8.7587571 24.88545984 -16.62762454  23.20414402  -6.4688086   27.22777548] -> 9915311.893479286
INFO:NiaPy.util.utility:nFES:4211 nGEN:33 => [ 87.26247246 -13.44817525   5.70160483  44.05798075  -8.60494291 24.88545984 -16.62762454  23.20414402  -6.4688086   27.22777548] -> 9587478.363003757
INFO:NiaPy.util.utility:nFES:4583 nGEN:36 => [ 3.65328259e+01 -3.14631366e+01 -5.20296680e+01 -6.79456609e+01 -8.22940002e+01  3.86427241e-02 -5.64351197e+01  2.84166811e+00 3.63551555e+01  7.35003723e+01] -> 6100994.847899254
INFO:NiaPy.util.utility:nFES:4985 nGEN:39 => [ 86.18669063  64.57227495   7.26842074  41.35161953  -7.01151937 7.42154167 -16.62762454  23.20414402  -6.4688086   27.22777548] -> 5245454.53943601
INFO:NiaPy.util.utility:nFES:7438 nGEN:58 => [ 86.18669063  64.57227495   7.94073075  40.25386016  -7.01151937 7.42154167 -17.0453594   23.20414402  -6.52790306  27.22777548] -> 5145265.1348766135
INFO:NiaPy.util.utility:nFES:7520 nGEN:58 => [ 71.58936263  60.00516209 -77.5807038  -38.34904881  -8.37590168 6.07531342  13.10586162  22.85495918  -7.68806029  28.67202685] -> 4074184.3482187847
INFO:NiaPy.util.utility:nFES:7909 nGEN:61 => [ 71.58936263 -30.98717792 -78.51423717  70.12581316  -9.38540003 6.07531342  11.39544115  22.85495918  -7.68806029  28.67202685] -> 3936654.7010732717
INFO:NiaPy.util.utility:nFES:8036 nGEN:62 => [ 71.58936263 -30.98717792 -78.51423717  70.12581316  -9.38540003 6.07531342  11.39544115  22.85495918  -6.6684219   28.67202685] -> 3533542.145993466
INFO:NiaPy.util.utility:nFES:8082 nGEN:63 => [ 87.13312482  64.57227495   9.86785745  40.25386016  -7.01151937 6.20013644 -17.0453594   24.48318048  -6.12517609  28.84835134] -> 1467478.0937885859
INFO:NiaPy.util.utility:nFES:8846 nGEN:69 => [ 33.90625295  46.64944041 -54.673065    25.18359199 -58.66103104 7.61430505  -6.99042223  25.14463581  -9.02855832  26.68275968] -> 1446960.826459867
INFO:NiaPy.util.utility:nFES:9175 nGEN:71 => [ 32.65706275 -11.03022952 -51.90262899  14.95251164 -61.83337437 0.11593587  -6.30630192  27.65838647 -14.73636282  23.09571086] -> 1439441.3097236762
INFO:NiaPy.util.utility:nFES:9362 nGEN:73 => [ 33.90625295  46.02723081 -53.80038573  25.18359199 -58.66103104 7.78463243  -6.7632788   25.14463581  -9.02855832  26.68275968] -> 1298824.6038914635
INFO:NiaPy.util.utility:nFES:9622 nGEN:75 => [ 33.90625295  46.02723081 -53.80038573  25.18359199 -58.66103104 7.78463243  -6.7632788   25.14463581  -9.46521599  26.68275968] -> 1168476.2654216695
INFO:NiaPy.util.utility:nFES:9749 nGEN:76 => [ 34.30779207  46.35280513 -53.79387727  25.18359199 -58.66103104 7.78463243  -6.7632788   25.14463581  -9.46521599  26.68275968] -> 656393.4653244294
INFO:NiaPy.util.utility:nFES:10817 nGEN:84 => [ 81.52806534 -72.67732702  15.49585433  11.94093646 -13.96059477 6.37269886 -20.1249368   24.51864551  -7.31691745  28.80846472] -> 279987.16440564074
INFO:NiaPy.util.utility:nFES:11206 nGEN:87 => [ 81.52806534 -72.67732702  15.49585433  11.94093646 -13.96059477 6.37269886 -20.02694896  24.51864551  -7.31691745  28.80846472] -> 274040.28021427593
INFO:NiaPy.util.utility:nFES:12460 nGEN:97 => [ 36.47216886  46.35280513 -53.79387727  27.81553475 -58.00264013 7.78463243  -7.73969571  25.42609831  -9.46521599  26.68275968] -> 91973.46618295947
INFO:NiaPy.util.utility:nFES:13232 nGEN:103 => [ 36.47216886  46.18595949 -53.79387727  27.81553475 -58.00264013 7.78463243  -7.73969571  25.42609831  -9.46521599  26.68275968] -> 91967.03291023677
INFO:NiaPy.util.utility:nFES:13621 nGEN:106 => [ 36.47216886  46.18595949 -53.79387727  87.46705669 -58.00264013 7.78463243  -7.73969571  25.42609831  -9.46521599  26.68275968] -> 91660.70832257405
INFO:NiaPy.util.utility:nFES:14910 nGEN:116 => [ 32.15816506  46.18595949 -53.39868514  87.46705669 -62.99649239 7.78463243  -8.48610814  25.42609831  -9.53877966  26.68275968] -> 68297.44505849422
INFO:NiaPy.util.utility:nFES:15167 nGEN:118 => [ 32.15816506  45.931732   -53.39868514  87.46705669 -62.99649239 7.78463243  -8.26331303  25.42609831  -9.53877966  26.68275968] -> 60557.1499980561
INFO:NiaPy.util.utility:nFES:16330 nGEN:127 => [ 32.15816506  45.931732   -20.4193586   87.46705669 -62.99649239 7.78463243  -8.26331303  25.42609831  -9.53877966  26.68275968] -> 59712.73434817474
INFO:NiaPy.util.utility:nFES:16715 nGEN:130 => [ 32.15816506  46.27858266 -20.4193586   86.14126836 -62.99649239 7.78463243  -8.26331303  25.42609831  -9.53877966  26.68275968] -> 59692.740618127966
INFO:NiaPy.util.utility:nFES:17681 nGEN:137 => [ 33.12299187 -11.32271641 -53.39868514  -3.67121275 -61.07891959 2.41098472  -6.46008221  13.20590003  15.78200791  51.30138857] -> 58780.83311514791
INFO:NiaPy.util.utility:nFES:17939 nGEN:139 => [ 33.12299187 -13.1603459  -53.39868514  -3.67121275 -61.07891959 2.41098472  -6.46008221  13.20590003  15.78200791  51.30138857] -> 58696.92921410378
INFO:NiaPy.util.utility:nFES:18713 nGEN:145 => [ 33.12299187 -13.1603459  -53.39868514  -3.67121275 -61.07891959 2.41098472  -6.68746091  13.20590003  15.77231857  51.30138857] -> 57856.24627350095
INFO:NiaPy.util.utility:nFES:19100 nGEN:148 => [ 33.12299187 -13.1603459  -54.92531815  -3.67121275 -61.07891959 2.41098472  -6.68746091  13.20590003  15.77231857  51.30138857] -> 57765.21890626749
INFO:NiaPy.util.utility:nFES:19747 nGEN:153 => [ 33.17834125 -13.1603459   25.12788654  -2.85646575 -61.07891959 2.41098472  -6.83010077  13.20590003  15.77231857  51.30138857] -> 56494.23602056541
INFO:NiaPy.util.utility:nFES:22454 nGEN:174 => [ 33.17834125 -13.1603459   25.12788654  -2.89497125 -61.07891959 2.41098472  -6.83010077  13.20590003  15.77231857  51.30138857] -> 56491.286120048884
INFO:NiaPy.util.utility:nFES:32905 nGEN:255 => [ 33.17834125 -13.1603459   25.12788654  -2.89497125 -61.07891959 2.41098472  -6.81476657  13.20590003  15.77231857  51.30138857] -> 56146.14486739578
INFO:NiaPy.util.utility:nFES:32927 nGEN:255 => [ 33.1910973   69.89945477  24.90396105  40.21909104 -62.00687898 2.3717096   -8.35435651  13.01747788  15.77231857  51.30138857] -> 44341.530265909256
INFO:NiaPy.util.utility:nFES:33445 nGEN:259 => [ 33.1910973   69.89945477  24.90396105  40.21909104 -62.00687898 2.3717096   -8.51311651  13.01747788  15.77231857  51.30138857] -> 41251.2326141535
INFO:NiaPy.util.utility:nFES:34446 nGEN:267 => [ 32.18333589 -11.51998764 -51.49685642  17.8012727  -62.46975308 0.65542397  -7.38434194  11.79857934  18.54991887  53.95296024] -> 36912.35100344157
INFO:NiaPy.util.utility:nFES:34947 nGEN:271 => [ 33.1910973  -31.00988332 -14.86926086  43.76052424 -62.03254822 0.3926579   -8.51311651   3.12635981  36.67556054  71.43261603] -> 26370.937989043938
INFO:NiaPy.util.utility:nFES:35334 nGEN:274 => [ 33.1910973   63.75128891 -76.59722592  43.32134143 -62.03254822 0.3926579   -8.51311651   3.12635981  36.67556054  71.43261603] -> 25627.592440332326
INFO:NiaPy.util.utility:nFES:36625 nGEN:284 => [ 33.1910973  -61.77084277 -76.59722592  80.40858876 -62.03254822 0.3926579   -8.51311651   3.12635981  36.67556054  71.43261603] -> 25194.864697481855
INFO:NiaPy.util.utility:nFES:42944 nGEN:333 => [ 33.1910973  -61.77084277 -77.20894516  80.40858876 -62.03254822 0.37724004  -8.59767275   3.12635981  36.67556054  71.43261603] -> 24137.28430108069
INFO:NiaPy.util.utility:nFES:46042 nGEN:357 => [ 33.1910973  -61.77084277 -76.66807123  80.40858876 -62.03254822 0.37724004  -8.59767275   3.12635981  36.67556054  71.43261603] -> 24131.86775912764
INFO:NiaPy.util.utility:nFES:48235 nGEN:374 => [ 33.1910973  -61.77084277 -76.66807123  80.40858876 -62.09990298 0.37724004  -8.59767275   3.12635981  36.67556054  71.43261603] -> 24072.841931338808
INFO:NiaPy.util.utility:nFES:48751 nGEN:378 => [ 33.1910973  -61.77084277 -77.72387315  80.40858876 -62.09990298 0.37724004  -8.79888634   3.12635981  36.67556054  71.43261603] -> 23888.764957597552
INFO:NiaPy.util.utility:nFES:50085 nGEN:388 => [ 33.1910973  -14.88214627 -24.9108862   23.65139848 -62.13831553 2.18777847  -8.79888634  13.02711077  16.13830506  51.57392175] -> 22932.91402839638
INFO:NiaPy.util.utility:nFES:50731 nGEN:393 => [ 33.1910973  -14.88214627 -25.79654474  23.65139848 -62.13831553 2.18580049  -8.79888634  13.02711077  16.13830506  51.57392175] -> 22889.295626019135
INFO:NiaPy.util.utility:nFES:51787 nGEN:402 => [ 34.09215831  48.80820088  22.03497727  19.82711977 -61.77692142 0.93867203  -9.82749742  11.94507099  18.21185485  53.56908928] -> 21562.901211486533
INFO:NiaPy.util.utility:nFES:52690 nGEN:409 => [ 34.09215831  48.80820088  22.03497727  19.82711977 -61.77692142 0.93867203 -10.05803774  11.94507099  18.21185485  53.5454872 ] -> 18494.963610212624
INFO:NiaPy.util.utility:nFES:53335 nGEN:414 => [ 34.09215831  48.80820088  23.0860946   18.49690893 -61.77692142 0.93867203 -10.05803774  11.94507099  18.21185485  53.5454872 ] -> 18395.714492637257
INFO:NiaPy.util.utility:nFES:53507 nGEN:415 => [ 35.43788655   4.267251   -76.21823978  32.17122785 -60.76173983 9.80682314 -11.04203351  11.20351345  19.95486227  55.24762481] -> 13866.685853681902
INFO:NiaPy.util.utility:nFES:55960 nGEN:434 => [ 35.43788655   4.267251   -76.21823978  32.52022398 -60.76173983 9.80682314 -10.9977719   11.20351345  19.95486227  55.24762481] -> 13148.992776191832
INFO:NiaPy.util.utility:nFES:56087 nGEN:435 => [ 35.43788655   4.267251   -77.49837522  32.52022398 -60.76173983 9.80682314 -10.9977719   11.20351345  19.95486227  55.24762481] -> 13111.444448132346
INFO:NiaPy.util.utility:nFES:58282 nGEN:452 => [ 35.43788655   4.267251   -77.49837522  31.33044872 -60.76173983 9.80682314 -10.9977719   11.20351345  19.95486227  55.24762481] -> 13097.828195105654
INFO:NiaPy.util.utility:nFES:58927 nGEN:457 => [ 35.43788655   4.90924078 -77.49837522  31.33044872 -60.76173983 9.80682314 -10.9977719   11.20351345  19.95486227  55.24762481] -> 13087.92957298424
INFO:NiaPy.util.utility:nFES:69632 nGEN:540 => [ 35.43788655   5.27932801 -77.49837522  31.33044872 -60.76173983 9.80682314 -10.9977719   11.20351345  19.95486227  55.24762481] -> 13086.925508871136
INFO:NiaPy.util.utility:nFES:78280 nGEN:607 => [ 33.65594195 -15.18590877 -78.84803874  22.29239374 -62.99649239 28.35215977 -11.33909898  25.6562184  -10.41351018  25.85062389] -> 12694.967416893094
INFO:NiaPy.util.utility:nFES:79719 nGEN:618 => [ 32.17855897   5.08324675 -21.81943692  29.613224   -63.95728425 12.18777847 -10.12651901  12.98169352  16.13830506  51.57392175] -> 10104.145282880356
INFO:NiaPy.util.utility:nFES:84106 nGEN:652 => [ 32.18333589   5.08324675 -21.81943692  30.43058579 -63.95728425 12.18777847 -10.12651901  12.98169352  16.13830506  51.57392175] -> 10022.777674140572
INFO:NiaPy.util.utility:nFES:92747 nGEN:719 => [ 32.18333589   5.08324675 -21.1258268   30.08495631 -63.95728425 12.18777847 -10.12651901  12.98169352  16.13830506  51.57392175] -> 9996.117513270421
INFO:NiaPy.util.utility:nFES:92876 nGEN:720 => [ 32.18333589   4.4248772  -21.1258268   30.08495631 -63.95728425 12.18777847 -10.12651901  12.98169352  16.13830506  51.57392175] -> 9956.021932716263
INFO:NiaPy.util.utility:nFES:95560 nGEN:741 => [ 33.69332748 -20.37548944 -80.70183326  40.89875688 -62.99649239 2.67972979 -11.33909898   5.54972325  31.69666465  66.63366771] -> 7412.29436929744
INFO:NiaPy.util.utility:nFES:99172 nGEN:769 => [ 33.69332748 -18.99282884 -80.70183326  41.24976397 -62.99649239 2.67972979 -11.33909898   5.54972325  31.69666465  66.63366771] -> 7406.53675319922
INFO:examples:[ 33.69332748 -18.99282884 -80.70183326  41.24976397 -62.99649239 2.67972979 -11.33909898   5.54972325  31.69666465  66.63366771] 7406.53675319922
```