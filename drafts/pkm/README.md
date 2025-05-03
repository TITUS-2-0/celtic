# Dataset 'The Mabinogion'

![Static Badge](https://img.shields.io/badge/TEI_validation-passing-green)

This is a TEI port of a [TITUS dataset](http://titus.uni-frankfurt.de/texte/etcs/celt/mcymr/pkm/pkm.htm).

* URL: https://github.com/TITUS-2-0/celtic/tree/main/drafts/pkm/
* version: unreleased
* date: 2025-01-15

## Citation
```text
Digital version of The Mabinogion (draft version). By: Jost Gippert, Florian Matter, Elena Parina. In: Carling, Gerd & Jost Gippert (2025). TITUS 2.0. Frankfurt: Goethe University. (URL: https://github.com/TITUS-2-0/celtic/tree/main/drafts/pkm/, visited on <insert date>)
```

## TEI encoding


### Unit Mapping
The TITUS 1 structural units are mapped onto TEI as follows:

| Source Unit | TEI Mapping | Notes |
|-------------|-------------|-------|
| Chapter | `div@chapter` | Automatically translated into named div |
| Ms. page | `pb@manuscript` |  |
| Page of edition | `pb@edition[main=yes]` |  |
| Line | `lb@edition` |  |

### Structural overview
```text
text (@xml:lang=wlm-Latn)
  body
    div (@data-level=1, @n, @type=chapter, @xml:id) (multiple)
      head (multiple)
      p (@xml:id) (multiple)
        [lb (@n, @type=edition) (multiple)]
        [pb (@n, @type=manuscript) (multiple)]
        [pb (@main=yes, @n, @type=edition) (multiple)]
        [note (@xml:id) (multiple)]
          [foreign (@xml:lang=cym-Latn | und-Latn-x-general) (multiple)]
        [pb (@break=no, @n, @type=manuscript) (multiple)]
        [lb (@break=no, @n, @type=edition) (multiple)]
        [pb (@type=manuscript)]
      [pb (@main=yes, @n, @type=edition) (multiple)]
      [pb (@n, @type=manuscript)]
```

### Structure Example

```xml
<div xmlns="http://www.tei-c.org/ns/1.0" n="PPD" xml:id="chapter-1" type="chapter" data-level="1">
				<pb main="yes" type="edition" n="1"/>
				<pb type="manuscript" n="1"/>
				<head>Pwyll Pendeuic Dyuet</head>
				<p xml:id="chapter-1-p-1">
					<lb type="edition" n="1"/>PWYLL, Pendeuic Dyuet, a oed yn arglwyd ar seith<lb type="edition" n="2"/>cantref Dyuet. A threigylgweith yd oed yn<lb type="edition" n="3"/>Arberth, prif lys idaw, a dyuot yn y uryt ac yn y<lb type="edition" n="4"/>uedwl uynet y hela. Sef kyueir o'y gyuoeth a uynnei y<lb type="edition" n="5"/>hela, Glynn Cuch. Ac ef a gychwynnwys y nos honno<lb type="edition" n="6"/>o Arberth, ac a doeth hyt ym Penn Llwyn Diarwya, ac<lb type="edition" n="7"/>yno y bu y nos honno. A thrannoeth yn ieuengtit y<lb type="edition" n="8"/>dyd kyuodi a oruc, a dyuot y Lynn Cuch i ellwng e<lb type="edition" n="9"/>gwn dan y coet. A chanu y gorn a dechreu dygyuor yr<lb type="edition" n="10"/>hela, a cherdet yn ol y cwn, ac ymgolli a'y gydymdeithon.<lb type="edition" n="11"/>Ac ual y byd yn ymwarandaw a llef yr<lb type="edition" n="12"/>erchwys, ef a glywei llef erchwys arall, ac nit oedynt<lb type="edition" n="13"/>unllef, a hynny yn dyuot yn erbyn y erchwys ef. Ac ef<lb type="edition" n="14"/>a welei lannerch yn y coet o uaes guastat; ac ual yd oed<lb type="edition" n="15"/>y erchwys ef yn ymgael ac ystlys y llannerch, ef a welei<lb type="edition" n="16"/>carw o ulaen yr erchwys arall. A pharth a pherued y<lb type="edition" n="17"/>lannerch, llyma yr erchwys a oed yn y ol yn ymordiwes<lb type="edition" n="18"/>ac ef, ac yn y uwrw y'r llawr.<lb type="edition" n="19"/>Ac yna edrych ohonaw ef ar liw yr erchwys, heb<lb type="edition" n="20"/>hanbwyllaw edrych ar y carw. Ac o'r a welsei ef o<lb type="edition" n="21"/>helgwn y byt, ny welsei cwn un lliw ac wynt. Sef lliw<lb type="edition" n="22"/>oed arnunt, claerwyn<pb type="manuscript" n="2"/>llathreit, ac eu clusteu yn<lb type="edition" n="23"/>gochyon. Ac ual y llathrei wynnet y cwn, y llathrei<lb type="edition" n="24"/>cochet y clusteu. Ac ar hynny at y cwn y doeth ef, a<pb main="yes" type="edition" n="2"/>
					<lb type="edition" n="1"/>gyrru yr erchwys a ladyssei y carw e ymdeith, a llithyaw<lb type="edition" n="2"/>y erchwys e hunan ar y carw.<lb type="edition" n="3"/>Ac ual y byd yn llithiau y cwn, ef a welei uarchauc<lb type="edition" n="4"/>yn dyuot yn ol yr erchwys y ar uarch erchlas mawr; a<lb type="edition" n="5"/>chorn canu am y uynwgyl, a gwisc o urethyn llwyt tei<lb type="edition" n="6"/>amdanaw yn wisc hela. Ac ar hynny y marchawc a<lb type="edition" n="7"/>doeth attaw ef, a dywedut ual hynn wrthaw, "A unben,"<lb type="edition" n="8"/>heb ef, "mi a wnn pwy wytti, ac ny chyuarchaf i well it."<lb type="edition" n="9"/>"Ie," heb ef, "ac atuyd y mae arnat o anryded ual nas<lb type="edition" n="10"/>dylyei." "Dioer," heb ef, "nyt teilygdawt uy anryded<lb type="edition" n="11"/>a'm etteil am hynny." "A unben," heb ynteu, "beth<lb type="edition" n="12"/>amgen?" "Y rof i a Duw," hep ynteu, "dy anwybot<lb type="edition" n="13"/>dy hun a'th ansyberwyt." "Pa ansyberwyt, unben, a<lb type="edition" n="14"/>weleist ti arnaf i?" "Ny weleis ansyberwyt uwy ar<lb type="edition" n="15"/>wr," hep ef, "no gyrru yr erchwys a ladyssei y carw e<lb type="edition" n="16"/>ymdeith, a llithiau dy erchwys dy hun arnaw; hynny,"<lb type="edition" n="17"/>hep ef, "ansyberwyt oed: a chyn nyt ymdialwyf a thi,<lb type="edition" n="18"/>y rof i a Duw," hep ef, "mi a wnaf o anglot itt guerth<lb type="edition" n="19"/>can carw."<lb type="edition" n="20"/>
					<pb type="manuscript" n="3"/>"A unbenn," hep ef, "o gwneuthum gam, mi a<lb type="edition" n="21"/>brynaf dy gerennyd." "Pa delw," hep ynteu, "y<lb type="edition" n="22"/>pryny di?" "Vrth ual y bo dy anryded, ac ny wnn i<lb type="edition" n="23"/>pwy wytti." "Brenhin corunawc wyf i yn y wlat yd<lb type="edition" n="24"/>hanwyf oheni." "Arglwyd," heb ynteu, "dyd da itt;<lb type="edition" n="25"/>a pha wlat yd hanwyt titheu oheni?" "O Annwuyn,"<lb type="edition" n="26"/>heb ynteu. "Arawn urenhin Annwuyn wyf i."<lb type="edition" n="27"/>"Arglwyd," heb ynteu, "pa furyf y caf i dy gerennyd<lb type="edition" n="28"/>di?" "Llyma wyd <note xml:id="chapter-1-p-1-note-1">wyd, <foreign xml:lang="und-Latn-x-general">W.,</foreign> yr wed, <foreign xml:lang="und-Latn-x-general">R.</foreign>
					</note> y kyffy," heb ynteu. "Gwr yssyd<pb main="yes" type="edition" n="3"/>
					<lb type="edition" n="1"/>gyferbyn y gyuoeth a'm kyuoeth inheu yn ryuelu arnaf<lb type="edition" n="2"/>yn wastat. Sef yw hwnnw, Hafgan urenhin o Annwuyn.<lb type="edition" n="3"/>Ac yr guaret gormes hwnnw y arnaf, a hynny a elly yn<lb type="edition" n="4"/>haut, y keffy uygherennyd." "Minnheu awnaf hynny,"<lb type="edition" n="5"/>heb ynteu, "yn llawen. A manac ditheu y mi pa furyf<lb type="edition" n="6"/>y gallwyf hynny." "Managaf," heb ynteu. "Llyna<lb type="edition" n="7"/>ual y gelly; mi a wnaf a thi gedymdeithas gadarn. Sef<lb type="edition" n="8"/>ual y gwnaf, mi a'th rodaf di y'm lle i yn Annwuyn, ac a<lb type="edition" n="9"/>rodaf y wreic deccaf<pb type="manuscript" n="4"/>a weleist eiroet y gyscu gyt a thi<lb type="edition" n="10"/>beunoeth, a'm pryt innheu a'm ansawd arnat ti, hyt na<lb type="edition" n="11"/>bo na guas ystauell, na swydawc, na dyn arall o'r a'm<lb type="edition" n="12"/>canlynwys i yroet, a wyppo na bo miui uych ti. A<lb type="edition" n="13"/>hynny," heb ef, "hyt ym penn y ulwydyn o'r dyd auory.<lb type="edition" n="14"/>Ac kynnadyl yna yn y lle hon." "Ie," heb ynteu,<lb type="edition" n="15"/>"kyt bwyf i yno hyt ympenn y ulwydyn, pa gyuarwyd a<lb type="edition" n="16"/>uyd ymi o ymgael a'r gwr a dywedy di?" "Blwydyn,"<lb type="edition" n="17"/>heb ef, "y heno, y mae oet y rof i ac ef, ar y ryt. A<lb type="edition" n="18"/>byd di i'm rith yno," heb ef. "Ac un dyrnaut a rodych<lb type="edition" n="19"/>di idaw ef; ny byd byw ef o hwnnw. A chyt archo ef<lb type="edition" n="20"/>yti rodi yr eil, na dyro, yr a ymbilio a thi. Yr a rodwn<lb type="edition" n="21"/>i idau ef hagen, kystal a chynt yd ymladei a mi drannoeth."<lb type="edition" n="22"/>"Ie," heb y Pwyll, "beth a wnaf i y'm<lb type="edition" n="23"/>kyuoeth?" "Mi a baraf," hep yr Arawn, "na bo i'th<lb type="edition" n="24"/>gyuoeth na gwr na gwreic a wyppo na bo tidi wwyf i.<lb type="edition" n="25"/>A miui a af i'th le di." "Yn llawenn," hep y Pwyll, "a<lb type="edition" n="26"/>miui a af ragof." "Dilesteir uyd dy hynt ac ny russya<lb type="edition" n="27"/>dim ragot, yny delych y'm kyuoeth i: a mi a uydaf<lb type="edition" n="28"/>hebryngyat arnat."<pb main="yes" type="edition" n="4"/>
					<lb type="edition" n="1"/>
					<pb type="manuscript" n="5"/>Ef a'y hebryghaud yny welas y llys a'r kyuanned.<lb type="edition" n="2"/>"Llyna," hep ef, "y llys a'r kyuoeth i'th uedyant. A<lb type="edition" n="3"/>chyrch y llys. Nit oes yndi nep ni'th adnappo; ac wrth<lb type="edition" n="4"/>ual y guelych y guassanaeth yndi, yd adnabydy uoes y<lb type="edition" n="5"/>llys." Kyrchu y llys a oruc ynteu. Ac yn y llys ef a<lb type="edition" n="6"/>welei hundyeu ac yneuadeu, ac ysteuyll, a'r ardurn teccaf<lb type="edition" n="7"/>a welsei neb o adeiladeu. Ac y'r neuad y gyrchwys y<lb type="edition" n="8"/>diarchenu. Ef a doeth makwyueit a gueisson ieueinc<lb type="edition" n="9"/>diarchenu, a phaup ual y delynt kyuarch guell a wneynt<lb type="edition" n="10"/>idaw. Deu uarchauc a doeth i waret i wisc hela y<lb type="edition" n="11"/>amdanaw, ac y wiscaw eurwisc o bali amdanaw.<lb type="edition" n="12"/>A'r neuad a gyweirwyt. Llyma y guelei ef teulu ac<lb type="edition" n="13"/>yniueroed, a'r niuer hardaf a chyweiraf o'r a welsei neb<lb type="edition" n="14"/>yn dyuot y mywn, a'r urenhines y gyt ac wynt, yn deccaf<lb type="edition" n="15"/>gwreic o'r a welsei neb, ac eurwisc amdanei o bali<lb type="edition" n="16"/>llathreit. Ac ar hynny, e ymolchi yd aethant, a chyrchu<lb type="edition" n="17"/>y bordeu a orugant, ac eisted a wnaethant ual hynn -- y<lb type="edition" n="18"/>urenhines o'r neill parth idaw ef, a'r iarll, deby-<pb type="manuscript" n="6" break="no"/>gei ef,<lb type="edition" n="19"/>o'r parth arall. A dechreu ymdidan a wnaeth ef a'r<lb type="edition" n="20"/>urenhines. Ac o'r a welsei eiryoet wrth ymdidan a hi,<lb type="edition" n="21"/>dissymlaf gwreic a bonedigeidaf i hannwyt a'y hymdidan<lb type="edition" n="22"/>oed. A threulaw a wnaethant bwyt a llynn a cherdeu a<lb type="edition" n="23"/>chyuedach. O'r a welsei o holl lyssoed y dayar, llyna<lb type="edition" n="24"/>y llys diwallaf o uwyt a llynn, ac eur lestri, a theyrn<lb type="edition" n="25"/>dlysseu.<lb type="edition" n="26"/>Amser a doeth udunt e uynet e gyscu, ac y gysgu<lb type="edition" n="27"/>yd aethant, ef a'r urenhines. Y gyt ac yd aethant yn<lb type="edition" n="28"/>guely ymchwelut e weneb at yr erchwyn a oruc ef, a'y<pb main="yes" type="edition" n="5"/>
  ...
```
