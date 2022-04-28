Everybody needs a little help at one time or another. In this exercise we will check how you can get help on powershell and how you can find interesting commands following your needs.

* Open a PowerShell session in your terminal
* type Get-Help

TOPIC
    Windows PowerShell Help System

SHORT DESCRIPTION
    Displays help about Windows PowerShell cmdlets and concepts.

LONG DESCRIPTION
    Windows PowerShell Help describes Windows PowerShell cmdlets,
    functions, scripts, and modules, and explains concepts, including
    the elements of the Windows PowerShell language.

    Windows PowerShell does not include help files, but you can read the
    help topics online, or use the Update-Help cmdlet to download help files
    to your computer and then use the Get-Help cmdlet to display the help
    topics at the command line.

    You can also use the Update-Help cmdlet to download updated help files
    as they are released so that your local help content is never obsolete.

    Without help files, Get-Help displays auto-generated help for cmdlets,
    functions, and scripts.


  ONLINE HELP
    You can find help for Windows PowerShell online in the TechNet Library
    beginning at http://go.microsoft.com/fwlink/?LinkID=108518.

    To open online help for any cmdlet or function, type:

        Get-Help <cmdlet-name> -Online

  UPDATE-HELP
    To download and install help files on your computer:

       1. Start Windows PowerShell with the "Run as administrator" option.
       2. Type:

          Update-Help

    After the help files are installed, you can use the Get-Help cmdlet to
    display the help topics. You can also use the Update-Help cmdlet to
    download updated help files so that your local help files are always
    up-to-date.

    For more information about the Update-Help cmdlet, type:

       Get-Help Update-Help -Online

    or go to: http://go.microsoft.com/fwlink/?LinkID=210614


  GET-HELP
    The Get-Help cmdlet displays help at the command line from content in
    help files on your computer. Without help files, Get-Help displays basic
    help about cmdlets and functions. You can also use Get-Help to display
    online help for cmdlets and functions.

    To get help for a cmdlet, type:

        Get-Help <cmdlet-name>

    To get online help, type:

        Get-Help <cmdlet-name> -Online

    The titles of conceptual topics begin with "About_".
    To get help for a concept or language element, type:

        Get-Help About_<topic-name>

    To search for a word or phrase in all help files, type:

        Get-Help <search-term>

    For more information about the Get-Help cmdlet, type:

        Get-Help Get-Help -Online

    or go to: http://go.microsoft.com/fwlink/?LinkID=113316


  EXAMPLES:
      Save-Help              : Download help files from the Internet and saves
                               them on a file share.
      Update-Help            : Downloads and installs help files from the
                               Internet or a file share.
      Get-Help Get-Process   : Displays help about the Get-Process cmdlet.
      Get-Help Get-Process -Online
                             : Opens online help for the Get-Process cmdlet.
      Help Get-Process       : Displays help about Get-Process one page at a time.
      Get-Process -?         : Displays help about the Get-Process cmdlet.
      Get-Help About_Modules : Displays help about Windows PowerShell modules.
      Get-Help remoting      : Searches the help topics for the word "remoting."

  SEE ALSO:
      about_Updatable_Help
      Get-Help
      Save-Help
      Update-Help


* Find out what a command such as Get-Process does without looking on google
Handles  NPM(K)    PM(K)      WS(K)     CPU(s)     Id  SI ProcessName
-------  ------    -----      -----     ------     --  -- -----------
    498      29    22072      30040       0.50   4444   3 ApplicationFrameHost
    127       8     1608        356              4148   0 armsvc
    207      13    14684      19588     803.11  18248   0 audiodg
      0      55     1904       3684       0.19   6536   3 bash
      0      27     1908       3652       0.05  20544   3 bash
    258      12     4536       3272       0.17  18452   3 browserhost
   1206      36   313844     250228     393.38   1928   3 chrome
    268      15    39844      44824       5.52   4872   3 chrome
    220      14     8048       7748       1.00   9848   3 chrome
    378      19    62548     111836       3.20  11168   3 chrome
    325      18    47600      53864       5.45  11564   3 chrome
    194      11     2212       2156       0.03  12872   3 chrome
   1491      60   104956     146908     274.23  16592   3 chrome
    369      29    22364      32648     230.09  17976   3 chrome
    288      19     8216      11168     158.78  19804   3 chrome
    312      17    49712      87084      11.64  20380   3 chrome
    367      19    68904      95964      46.25  20484   3 chrome
    227      14    13120      29244       0.08  20536   3 chrome
     70       5     2356        212       0.00   8308   3 cmd
     70       5     2352        212       0.02  17532   3 cmd
    179      13    20608      74508       0.28   6264   3 Code
    288      16    12200      13992       2.19   7216   3 Code
    176      13    21516      19772       0.75   9092   3 Code
    180      13    20360      76216       0.19   9708   3 Code
    402      20    98480     107756      22.64   9724   3 Code
    703      28   181668     161168      20.14  10976   3 Code
    301      15    48984     106568       1.05  11348   3 Code
    293      15    48224     104136       1.52  11444   3 Code
    256      12    10212       5404       0.08  13736   3 Code
    179      13    20628      75208       0.20  14648   3 Code
    339      18    94344     138256       5.23  15080   3 Code
   1303      62    79440     115444      83.59  15488   3 Code
    307      15    57712     115360       1.36  17960   3 Code
    398      18    73320      74824      24.06  19224   3 Code
    448      21   168032     212108      10.28  19900   3 Code
    158      11     6740       1740              6760   0 conhost
    102       7     6244       1080              6992   0 conhost
    105       8     6332       1016       0.00   8584   3 conhost
    244      16    11092      21016       0.70   8812   3 conhost
    125      10     6700       1732       0.06   9912   3 conhost
    276      15     6044      18824       4.53  12696   3 conhost
    124      10     6776      13076       0.03  15420   3 conhost
    124      10     6708      12752       0.02  16440   3 conhost
    125      10     6712       1720       0.06  18204   3 conhost
    102       7     6244        768             18388   0 conhost
    192      13     7140      16772       0.09  20772   3 conhost
    971      31     2260       2328               816   0 csrss
    885      28     2892       3520             14284   3 csrss
    556      18     5364      12120      31.81    412   3 ctfmon
    169       9     1916        880             15972   0 DDVCollectorSvcApi
    368      24    25680      15040              4964   0 DDVDataCollector
    277      18    17940       5292              4108   0 DDVRulesProcessor
    872     110   127928      67276             15688   0 Dell.D3.WinSvc
    469      40    58240      26996       1.08  12940   3 DellMobileConnect
    713      40    81832      18476       1.08   2980   3 DellMobileConnectClient
   1427      82    83664      44368             15496   0 DellSupportAssistRemedationService
    268      16     4420       7680       0.84   9108   3 dllhost
    207      18     3960       3728             10872   0 dllhost
     96       8     1580       1368     100.28  10036   3 dptf_helper
    758      66   112536      91780             14536   0 Dsapi
   1456      54   158104     104792             17084   3 dwm
    132       7     2160       1952              4252   0 esif_uf
   4276     111   222276     152696     149.33  16736   3 explorer
    219      14     4876       8596       2.98   3604   3 FileCoAuth
    123       8     1312       7404             12824   0 fodhelper
     32       6     1900        316               892   0 fontdrvhost
     32       7     2560       2220             16636   3 fontdrvhost
     53       4      840        852              4728   0 GoodixSessionService
    176      10     1632       1372              4032   0 GoogleCrashHandler
    160       9     1672        528              8860   0 GoogleCrashHandler64
   1065      51    91360       1168       1.41   3508   3 HxOutlook
    661      29    12716      16340       0.64   2788   3 HxTsr
      0       0       60          8                 0   0 Idle
    206      11     2352       5696              2640   0 igfxCUIServiceN
    302      15     3796       3492       0.30  15448   3 igfxEMN
      0       8      200        232       0.00  12040   3 init
      0      13      200        232       0.00  16488   3 init
      0       8      564        768       0.63  21168   3 init
    441      28    44404       7928              4356   0 IntelAudioService
    128       7     1212        556              2020   0 IntelCpHDCPSvc
    137       8     1292        492              5976   0 jhi_service
    211      10     3040       1756              4488   0 LMS
    590      29    41836      53000       0.78   1976   3 LockApp
   2075      32    12748      19108               536   0 lsass
    701      53    56336       7204       1.05  16748   3 mcafee-security
    289      14     3524       2484       0.13  20692   3 mcafee-security-ft
    202      12     3264       2980              8940   0 mcapexe
    434      24     9544      13600             11288   0 McCSPServiceHost
    544      26    74988      34300      40.33  12632   0 mcshield
    439      34    10524      14460       0.38  15464   3 McUICnt
      0       0      608     180848              3060   0 Memory Compression
   1016      47    67464      52792              1600   0 MfeAVSvc
    226      17     4864       1592       0.14  20328   3 MfeBrowserHost
    481      29     8996      11964              4456   0 mfemms
    363      12     9004      11596              6644   0 mfevtps
    624      44    68352      57708       0.48  10108   3 Microsoft.Photos
   1661      62    41128      48752              6580   0 MMSSHOST
    497      25     7312       7376              4464   0 ModuleCoreService
   1007      75    56868      61404              6880   0 ModuleCoreService
    470      30    13232      19592       1.59  14572   3 ModuleCoreService
    239      14     3332       1116       0.17  21380   3 MusNotifyIcon
    235      13     2600       3184       0.69   9100   3 notepad
    276      15     3036       3724       0.33  15888   3 notepad
    277      15     3060       3748       0.47  20548   3 notepad
    787      27    33548      23212              4184   0 OfficeClickToRun
    749      32    46028      10188              4216   0 OneApp.IGCC.WinService
    848      48    24252      38596     156.94   1108   3 OneDrive
    495     136    81436       7292              1424   0 PCHealthCheck
    406      29    18756      21672              4596   0 PEFService
    755      34    72612      96256       4.41   5464   3 powershell
    323      19     5040       5996              6804   0 ProtectedModuleHost
    217      15     3328       4880               980   0 QcShm
    307      12     8896      10940              6744   0 RAPS
    249      14    14784       1264              6588   0 RAPSService
      0      14    10020      28136               124   0 Registry
    154       9     1752        560              4736   0 RstMwService
    332      22     4656       4784              4720   0 RtkAudUService64
    333      21     3912       5124       0.11   7288   3 RtkAudUService64
    244      18     1844       2604             12612   3 RtkAudUService64
    304      16     3864       7384       0.48   1148   3 RuntimeBroker
    123       8     1516       1420       0.02   1816   3 RuntimeBroker
    291      14     3264       3404       0.17   2624   3 RuntimeBroker
    429      32     7356      15312       6.61   3048   3 RuntimeBroker
    896      42    16504      35432       7.53   3512   3 RuntimeBroker
    259      13     3048       3104       0.14   5212   3 RuntimeBroker
    249      14     3520       3760       1.28   8692   3 RuntimeBroker
    463      24    10880      27528       2.56   9052   3 RuntimeBroker
    321      17     5560      18920       0.25  11232   3 RuntimeBroker
    265      15     3260       7760       0.09  13148   3 RuntimeBroker
    292      17     6044       7860       1.94  16744   3 RuntimeBroker
    283      17    16436       1876              4752   0 SafeConnect.ServiceHost
    586      23    13052      12700       1.48   7988   3 SDXHelper
   1345     189   439128     439936      34.39  13536   3 SearchApp
   3407     154   251972     281780      41.16  17348   3 SearchApp
   1255      75    54376      47144              9648   0 SearchIndexer
    493      19     4560       7584              2076   0 SecurityHealthService
    162      10     1936       3548       0.03  11436   3 SecurityHealthSystray
    717      39    18956      21884             10452   0 servicehost
    880      13     6480       8272               520   0 services
   1751      52    59808      26552              1672   0 ServiceShell
    601      27    10316       9840      10.36  13264   3 SettingSyncHost
    105       8     5504       5420             13520   0 SgrmBroker
    630      29    41568      13672       6.50  13016   3 ShellExperienceHost
    684      20     8072      20988       6.22  11084   3 sihost
    118       7     1504        716              4744   0 SmartByteAnalyticsService
    511      21   118272      55024              4760   0 SmartByteNetworkService
    412      25    32456      15948     458.41   6112   3 SmartByteTelemetry
     53       3     1072        248               488   0 smss
    435      22     5628       4552              3832   0 spoolsv
    216      12     2360       2492       0.44  12208   3 SSScheduler
    733      34    55272      81080       3.14  12076   3 StartMenuExperienceHost
   1134      96   605508      62932             15216   0 SupportAssistAgent
    336      13     2788       2136               736   0 svchost
   1751      28    16032      24272               880   0 svchost
   1673      21    12436      16352              1200   0 svchost
    350      11     3288       4492              1264   0 svchost
    207      12     2668       3688              1448   0 svchost
    168      37    10576      10720              1512   0 svchost
    398      20     3172       4204              1640   0 svchost
    174       7     1748       1928              1648   0 svchost
    411      18     6752       9564              1692   0 svchost
    209      10     2056       4532              1708   0 svchost
    251      14     3824       5740              1752   0 svchost
    254      14     2736       2436              1764   0 svchost
    359       9     2092       4496              1772   0 svchost
    285      11     2920       3036              1916   0 svchost
    354      11     3244       6584              2004   0 svchost
    121       8     1556        936              2036   0 svchost
    453      15    17056      13728              2056   0 svchost
    185      10     2420       4364              2096   0 svchost
    142      10     1736       1848              2108   0 svchost
    187       9     2052       3528              2216   0 svchost
    187      10     1872       2736              2324   0 svchost
    276      16     4156      13232              2368   0 svchost
    145       9     1752       1436              2440   0 svchost
    228      15     2412       5424              2444   0 svchost
    405      17     5404       6592              2460   0 svchost
    248      13     2812      11400              2508   0 svchost
    206      13     3092       6600              2716   0 svchost
    484      14     3728       5972              2728   0 svchost
    246      11    10492      16168              2836   0 svchost
    193      12     2344       3516              2856   0 svchost
    330      16     4668       5716              2864   0 svchost
    290       7     1308       1444              2872   0 svchost
    238      17     4304       6820              2880   0 svchost
    317      21     7916       4452              2888   0 svchost
    170      10     2044       2796              3080   0 svchost
    437      16     4752       8508              3448   0 svchost
    140      11     1880       2624              3596   0 svchost
    561      26     8540      10664              3636   0 svchost
    259      15     3368       4576              3700   0 svchost
    309      18    13716       4636              3900   0 svchost
    436      34    10524      10776              3928   0 svchost
    182      11     2020       2636              3984   0 svchost
    384      20     6024      10624              4004   0 svchost
    367      25    41556      44204              4164   0 svchost
    410      27     5260       9912              4172   0 svchost
    555      26    18996      22860              4196   0 svchost
    261      14     2892       2892              4240   0 svchost
    695      19    14228      18960              4348   0 svchost
    397      22     9148       7828              4560   0 svchost
    369      17     7312      15908              4584   0 svchost
    208      12     2420       3892              4604   0 svchost
    213      13     2740       3328              4612   0 svchost
    130       9     1568       1136              4640   0 svchost
    363      13     5092      15628              4704   0 svchost
    125       8     1328        656              4804   0 svchost
    366      17     3168       3832              4836   0 svchost
    103       8     1432       1272              5140   0 svchost
    211      14     2508       2524              5228   0 svchost
    409      21     5308      11496              5316   0 svchost
    419      27     3764       3588              5924   0 svchost
    165      10     1916       2044              5944   0 svchost
    176     166     2920       2104              7884   0 svchost
    426      23     6168       6968              8064   0 svchost
    226      11     2308       4212              8124   0 svchost
    305       8     1756       3888              8180   0 svchost
    597      24     9172      16788       4.27   8244   3 svchost
    151      10     1824       3832              8368   0 svchost
    220      12     3060       5644              8388   0 svchost
    178      12     2296       5216              8548   0 svchost
    286      21     3176       3776              8844   0 svchost
    118       7     1412       2020              9180   0 svchost
    113       7     2744       8048              9772   0 svchost
    200      12     2844       5448             10048   0 svchost
    321      16     4208      15024       1.45  10704   3 svchost
    263      17     3296       4608             11684   0 svchost
    578      20     4848      10316             11860   0 svchost
    334      15     3776       4424             13192   0 svchost
    297      14     4836       5656             13248   0 svchost
    162      11     2260       2612             13620   0 svchost
    191      15     6360       3800             14860   0 svchost
    203      12     2332       5488             14888   0 svchost
    501      26     5848       5704       0.58  17064   3 svchost
    484      20    12088      20464      17.59  17884   3 svchost
    274      17     5020      17008             18040   0 svchost
    120       8     1608       7500             19372   0 svchost
    168       9     1760       7416             21248   0 svchost
   7435       0      192         32                 4   0 System
    889      43    49420       5008       0.42  19500   3 SystemSettings
    334      17     4136       8780       3.03   4268   3 TabTip
    323      35     8300      10960       1.17   6104   3 taskhostw
    567      25    38976      14116      19.94  17556   3 TextInputHost
    166      58    24556      31712             19408   0 TiWorker
    127       8     1916       7732             16496   0 TrustedInstaller
    151      10     1744       8640       0.00   8560   3 ubuntu2004
    147       9     1692       8600       0.03  16700   3 ubuntu2004
    615      36    18084      13128      11.91  17300   3 uihost
    139      10     2312       4584       0.08   1324   3 UserOOBEBroker
    134      10     1996        976             19112   0 UserOOBEBroker
    719      39    46212        752       0.47   4304   3 Video.UI
    133      12     3040       1804              5024   0 vmnat
     83       8     7764       1224              5032   0 vmnetdhcp
    623      62    56012      27012      23.81  12284   3 vmware
    232      17     3844       1044              4884   0 vmware-authd
    195      17     3800       1824       0.14  15396   3 vmware-tray
    280      23     7664       2128       0.34  21140   3 vmware-unity-helper
    238      14     3208       2680              5016   0 vmware-usbarbitrator64
    578      33    62896     758844      56.63  19200   3 vmware-vmx
    288      13    13140       4068              5040   0 WavesAudioService
    788      23     6664      11616      64.11  18376   3 WavesSvc64
    529      20     6004      10076              8392   0 WavesSysSvc64
    168      11     1728        516               984   0 wininit
    283      12     2752       5524             18848   3 winlogon
    120       7     1320       1896             18368   0 wlanext
    386      23    15044      20300              9188   0 WmiPrvSE
    497      24    16292      23816             10052   0 WmiPrvSE
    258      13     2696        504              5168   0 WMIRegistrationService
    121       7     1284       6724       0.00   4968   3 wsl
    120       7     1264       6744       0.05  12236   3 wsl
    116       7     1232       6532       0.02  10876   3 wslhost
    112       7     1156       6456       0.03  15572   3 wslhost
    280      10     4200       2940              1028   0 WUDFHost
   1320      16    17732       7112              1164   0 WUDFHost
    472      21    14104      16476              1436   0 WUDFHost
    826      52    59012      47892       1.08   1860   3 YourPhone

* Now try with the -online parameter
It will redirect to the help directory
Get-Help Get-Help -online

* What does Get-command?
It will display all the alias command, functions and the cmdlet commands. 

